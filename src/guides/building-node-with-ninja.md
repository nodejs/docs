# Building Node with Ninja

The purpose of this guide is to show how to build Node.js using [Ninja][], as doing so can be much quicker than using `make`. Please see [Ninja's site][Ninja] for installation instructions (unix only).

To build Node with ninja, there are 4 steps that must be taken:
1. Configure the project via `./configure` as usual.
2. Make `tools/gyp_node.py` produce Ninja output.
3. Run Ninja in `out/Release` to produce release output.
4. Link `out/Release/node` to `./node`.

Those 4 steps can be achieved with the following commands:
1. `./configure` (regular configure based on OS)
2. `tools/gyp_node.py -f ninja` (passes `-f ninja` to `gyp`)
3. `ninja -C out/Release` (run `ninja` within the `out/Release` directory, where ninja instructions were put)
4. `ln -fs out/Release/node node` (create a link to `./node`, using `-f` to overwrite and `-s` to make a symlink)

When running `ninja -C out/Release` you will see similar output if the build has succeeded:
```
ninja: Entering directory `out/Release`
[4/4] LINK node, POSTBUILDS
```

The bottom line will change while building, showing the progress as `[finished/total]` build steps.
This is useful output that `make` does not produce and is one of the benefits of using Ninja.
Also, Ninja will likely compile much faster than even `make -j8` (or `-j<number of processor threads on your machine>`).

## Considerations

Ninja builds vary slightly from `make` builds. If you wish to run `make test` after, `make` will likely still need to rebuild some amount of Node. However, it is likely still faster. To get around this, be sure to always run `make` with `-j<number of threads>`.

## Alias

`alias nnode='./configure && tools/gyp_node.py -f ninja && ninja -C out/Release && ln -fs out/Release/node node'`

## Producing a debug build

The above alias can be modified slightly to produce a debug build, rather than a release build as shown below:
`alias nnodedebug='./configure && tools/gyp_node.py -f ninja && ninja -C out/Debug && ln -fs out/Debug/node node_g'`


[Ninja]: https://martine.github.io/ninja/
