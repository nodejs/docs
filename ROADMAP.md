# Docs WG Roadmap

## Jan 2016 → Apr 2016 (Q1)

This is the first of the quarterly roadmaps that this Working Group will
produce, so it will be structured a bit differently than subsequent ones. Since
this is a brand-new process, an explanation of **what it is** and **why it's
necessary** follows.

This roadmap outlines the priorities for the Docs working group for the
quarter. These tasks can be as broadly or narrowly defined as is useful. They
are not necessarily staffed — as folks step up to do the work, we'll link
tracking issues to the tasks for them to self-organize. Every quarter we'll
revisit this roadmap, adding a quick postmortem of how things went, and
creating a new set of priorities for the ensuing quarter.

That brings us to why a roadmap is necessary: the Node.js documentation is a
relatively confined space to work within, and there are many interested
parties: there are groups that consume the documentation as output, like the
[website working group][wg-website], there are groups concerned with ensuring
the [content addresses the needs of diverse audiences][wg-inclusivity], there are
[groups that are required][wg-ctc] to produce API documentation as a
pre-requisite to merging their primary work, there are contributors who wish to
help in a _technical_ fashion, there are contributors who wish to contribute
_editorially_, and there are the readers of the docs. All of these
contributions overlap, so in order to make measurable progress without stepping
on each other's feet, we have to:

* **Set clear priorities** — if two contributions conflict, it should be
  straightforward to determine which contribution should take precedence.
* **Message these priorities well in advance** — with this many stakeholders,
  we should mention repeatedly, loudly, and clearly what our intentions are.
  The Docs WG should aspire to avoid surprise.
* **Make the best use of donated time** — we want to ensure that if someone is
  donating their time to improve the documentation, it will be well-spent, and
  directed at driving the documentation towards this WG's [stated goals][goals].

[Our goals][goals] can be summarized thusly:

> Node.js should be in friendly competition for "Best Docs in OSS," with docs
> that address the needs of a wide variety of audiences — across skill levels,
> goals, and languages.

### Tasks

Tasks for this quarter were drawn from [responses to this issue][issue-roadmap].
They are divided between three major areas:

* **Content** — the actual content of the docs
* **Features** — reader-focused features, like version metadata or autolinking.
* **Tooling** — author-focused features, like doc linting or html generation.

Since **content** is the ultimate product of this WG, it will usually be the
highest priority. However, when **content** systemically fails audiences, it
may point to a need for better **features** or **tooling**.

**Right now, our features and tooling are lacking, and the content is suffering
for it.**

#### :one: Pulling Guides into [nodejs/node][repo-nodejs]

**This is our highest priority over the next two months.**

Right now the documentation is split between the [website repo][wg-website] and
the [core repo][wg-ctc]. We wish to bring the [guide documentation][guide-docs]
into the core repo.

The existing [node doctool][ref-doctool] is specifically built to _only_
generate API docs. Until we can build the guide docs with Node.js' `make doc`
command, guide documentation will be copied from the website repo into the core
repo, but not *removed* from the website repo.

As a result, we are investigating using [remark][ref-remark] to build the
docs. The stages of this project are as follows:

1. Use remark to build just the guides alongside the existing doctool.
2. Remove the guides from the website repository.
3. Identify and install the necessary remark plugins to faithfully render the
   API documentation.
4. Generate all documentation using remark. Fix lint issues pointed out by
   `remark-lint`.
5. Once no linting issues remain, wire up docs linting as part of Node.js'
   `make test`.

Once this project is complete, all doc style rules will be handled by remark,
which includes line lengths, code samples (via eslint), markdown bullet and
emphasis styles, and link checking. We will have a solid basis on which to add
spelling and grammar checkers in the future, making it easier to maintain the
docs going forward.

##### Subtasks

Want to pitch in? Look here! If someone's already working on the task, see
if they need help.

* Identifying Remark plugins — **@qard**, others! [nodejs/docs#61](https://github.com/nodejs/docs/issues/61)
* Initial Remark integration — **@qard** [nodejs/node#4866](https://github.com/nodejs/node/pull/4866)
* Codify linting rules
  * Apply linting rules across API docs
* HTML layout for guide docs
* HTML layout update for API docs to include refs to guide docs

#### :two: Guide and Topic Docs

A _very_ close second to the work on the documentation tooling is the work on
identifying and creating new guides and topic documentation. These two terms
come up a lot, to clarify what they mean, here's an except from our [getting
started][ref-getting-started] guide:

> 1. **Guide** documents explain processes to help the reader learn a concept
> in service of their larger goal. Usually a guide has the reader build
> something — a little webserver, or CLI — and explains the concept it's trying
> to convey using examples from the readers experience with that code. Guides
> are great for introducing new concepts in a comfortable way, by letting the
> reader "simulate" the process of what development will be like using those
> concepts.
> 2. **Topic** documents explain concepts to help the reader make a decision.
> They are a great place for "deep dive" information, and to handle anything
> that's fairly intricate.
> 3. **Reference** documents explain capabilities to help the reader achieve
> their goal. API documentation is the primary example of this.

Node.js currently has **reference** documentation, but because of the lack of
**topic** and **guide** documentation, it ends up having to repeat itself a
lot. Sometimes the lack of a dedicated place for this kind of documentation
means that reference docs will attempt to include guides or topic docs inline —
this usually doesn't end up working well in the long run.

The Docs WG has identified and created a few guides already, some of which are
the subject of the [first](#one-pulling-guides-into-nodejsnode) task.
*However*, we need help filling in the gaps — both in identifying needed docs,
as well as in executing on them.

It's important to note that this documentation applies as much to topics
*internal* to the project as it does to our externally facing API — we need
guides and overviews for the architecture of Node, as well as how to
collaborate on the project.

##### Subtasks

Want to pitch in? Look here! If someone's already working on the task, see
if they need help.

* Overviews:
  * "Encoding", to be used by the Buffer and FS docs.
  * "Blocking vs. non-blocking."
  * Syscall documentation, to be used primarily by FS, but throughout the codebase.
  * Internal: Node.js Architecture — **@eljefedelrodeodeljefe** [#71](https://github.com/nodejs/docs/issues/71)
  * Internal: Initialization process — **@thealphanerd** [#73](https://github.com/nodejs/docs/issues/73)
  * Internal: Timers
  * Internal: Event loop — **@DavidTPate** [#74](https://github.com/nodejs/docs/issues/74)
  * Internal: Signals
  * Internal: Docs WG Process — **@chrisdickinson**
* Guides:
  * Internal: New Collaborator guide — **@nodejs/inclusivity**, **@ashleygwilliams** [nodejs/inclusivity#96](https://github.com/nodejs/inclusivity/issues/96)
  * Internal: Move "cutting releases" into these guides — **@thealphanerd** [#75](https://github.com/nodejs/docs/issues/75)
  * Streams: For Authors
  * Streams: For Consumers — **@bengl**
  * Walkthroughs for each module
* Reference:
  * Glossary of terms, to be used by all docs.
  * Streams: remove guide content from API doc once guides have been written.
  * Streams: Descriptive spec — **@nodejs/streams** [nodejs/readable-stream#181](https://github.com/nodejs/readable-stream/issues/181)
* Identifying other docs to create 

#### :three: Improving API Metadata

One of the most common requests we've received is that the API docs start
including relevant version information alongside methods. This information
should include the version the API was introduced in, when it was last changed,
and when it was deprecated, if applicable. Second to that, we've received
requests to automatically link types of parameters to the appropriate MDN or
Node.js documentation sections, and note what (if any) errors an API will
generate, and how it will propagate them.

This points to the need to standardize tooling around this metadata, and then
execute against that tooling.

This task should track the work being done in task #1 — that is to say, this
metadata should be tracked by remark plugins in as much as is possible.

##### Subtasks

* Per-section YAML — **@qard**, **@tflanagan** [nodejs/node#3867](https://github.com/nodejs/node/pull/3867)
* Noting 'version introduced' on each API — **@tflanagan**
  * Ideally this should link to the CHANGELOG for that release.
* Standardizing API method signature documentation
  * Type annotation — **@fansworld-claudio** [nodejs/node#4741](https://github.com/nodejs/node/pull/4741)
    * (This will have to be brought into the Remark work as well.)
  * Error generation
* Automatically linking `syscall(2)`-format terms to the appropriate docs.
* Allow authors to pick a simpler anchor for headings in addition to the
  autogenerated anchor.

### Notably Missing

There are a few things notably missing from this list — this is not because
they are not important to us, but because we are primarily constrained by time
and the size of the content we are working within. Foremost among the missing
pieces is an internationalization strategy. This task cannot be approached
lightly, and will likely include touching *all* of the docs in a single PR.
While we welcome discussion on how to approach this issue, we will not be
executing on it until after March 2016. Likewise, search is an extant issue
that we do not have the resources to work on at present.

### Pitching In

If you would like to help out with the Docs, you can:

* Find a subtask above and raise your hand on the associated issue or create
  an issue on the [docs issue tracker][docs-tracker].
* Raise your hand [here][weekly-review] to help with the weekly docs review
  load.

[docs-tracker]: https://github.com/nodejs/docs/issues/new
[goals]: https://github.com/nodejs/node/blob/master/WORKING_GROUPS.md#documentation
[guide-docs]: https://github.com/nodejs/nodejs.org/tree/master/locale/en/docs/guides
[issue-roadmap]: https://github.com/nodejs/docs/issues/59
[ref-doctool]: https://github.com/nodejs/node/tree/master/tools/doc
[ref-getting-started]: ./GETTING-STARTED.md
[ref-remark]: https://www.npmjs.com/package/remark
[repo-nodejs]: https://github.com/nodejs/node
[weekly-review]: https://github.com/nodejs/docs/issues/69
[wg-ctc]: https://github.com/nodejs/node
[wg-inclusivity]: https://github.com/nodejs/inclusivity/
[wg-website]: https://github.com/nodejs/nodejs.org/
