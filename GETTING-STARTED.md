# Node Documentation

Welcome to the Node.js Documentation Guide — or less formally, the docs on
docs. If you're here, you're likely looking for guidance on how to write
documentation for the project. You're in luck! This is where we house all of
that information.

This guide is divided into sections for **why** we're writing docs, **what** we
want to write, and **how** we write it.

* If you're new here, start from the top with the [Why We Write Docs section][]
and go down.
* If you're ready to write some docs but don't know what to write, look at the
[What We Write section][].
* If you have a formatting or grammar question, look at the
[How We Write section][].

## Why We Write Docs

Documentation serves many audiences in many different ways — and we recognize
that. For some, the docs are their introduction to Node, and they want to know
what all the fuss is about. Others might be learning to program for the first
time. Still others may simply use the reference documentation we provide as a
sort of cache for information otherwise available in the source code of the
project.

We write docs because we want to include people from each of these audiences in
our community, we want to make their lives better, and we want them to walk
away from the docs with a positive attitude about the Node community. We want
this not just out of empathy for our fellow human beings, but also out of
self-preservation: the health of Node hinges on how useful it is, and how
useful it is depends on how easy it is for folks to use it! If folks can't
figure out how to use Node, they walk away from it, and then we have to start
writing for a different platform which might not be nearly [as fun][].

To summarize:

* Our audiences are **diverse** and have **different goals** coming into the
docs.
* We write docs so that our audiences can have a **positive experience** with
Node.
* We want them to have a positive experience with Node out of **empathy** and
**self-preservation**.

## What We Write

A solid strategy around structure is key to building good documentation.
Authors must know where to put a topic before they can start writing it — they
need to know the larger context of how the reader will get to that document.
Misplaced documentation won't be found, or, more disastrously, will appear
interleaved in other documentation, which is hugely confusing!

For that reason, we split our writing into three categories:

1. **Guide** documents explain processes to help the reader learn a concept in
service of their larger goal. Usually a guide has the reader build something —
a little webserver, or CLI — and explains the concept it's trying to convey
using examples from the readers experience with that code. Guides are great for
introducing new concepts in a comfortable way, by letting the reader "simulate"
the process of what development will be like using those concepts.
[Django's getting started guide][] is a great example of this, though it doesn't
necessarily have to be aimed at beginners.
2. **Topic** documents explain concepts to help the reader make a decision.
They are a great place for "deep dive" information, and to handle anything
that's fairly intricate.
3. **Reference** documents explain capabilities to help the reader achieve
their goal. API documentation is the primary example of this.

Every document we author should address **one primary audience** and describe
**one complete idea**. If a document starts to address two audiences or ideas,
it can quickly become confusing and hard to maintain. Documents that start to
transform in this way should be **split up**. When a document about a topic
starts to describe two ideas, the core concept of both should become a
directory that documents for both ideas are put into. For example:

    topics/streams.md ->
      topics/streams/using-a-stream.md      # for users of streams
      topics/streams/writing-a-stream.md    # for authors of streams
      topics/streams/index.md               # links to both of the above

In other cases, in order to explain an API, reference documentation may need to
describe a larger topic. In that case, the topic should be described
separately, as a document in `topics/`, and linked to from the reference in
`references/`. This is especially true when multiple references need to
describe the same topic!

We believe good documentation is fractal. Guides, topics, and reference may all
repeat that organization internally, so long as it does not interfere with the
communication of the core idea of the document. For example, it's good to add
links to reference materials at the end of topic docs, but it would be unwise
to enumerate a module's entire list of methods inside that same doc. Another
example: it's great to include *brief* example code in the reference
documentation, but it is not so great to include a full program there.

To summarize:

* Structure is of paramount importance.
* Decide on an **audience** and an **idea** you want to convey to that
audience.
* If the reader is to follow a process to get to a goal, it's a **guide.**
* If what you're writing conveys a concept to help the reader in decision
making, it's a **topic.**
* When the reader is consulting your document to find a specific piece of
information, it's **reference.**
* Each document should clearly convey *one* idea to *one* audience. All
strategies are in service of that goal.

## How We Write

Please adhere, as best as possible, to the [style guide][].

### Tone

The tone of your writing should change in service of the goal of the document.
For example, *guides* may be warm and whimsical in order to make the reader
comfortable and pique their interest. *Reference material* should adopt a
terser, more clinical tone, in order to more efficiently convey information to
the reader. *Topics* are halfway between the two — a more neutral tone may be
adopted, but it's okay to mix some humanity in as well!

### Introducing Changes

To introduce changes, open a PR to this repository. One "LGTM" comment from
another team member is sufficient to merge a change. When describing your
change, make sure to note why you are making the change in the description. If
you are writing a new doc, please include a one-to-three sentence paragraph
explaining the idea you are attempting to convey and the audience you are
targeting. For more information on this, see [CONTRIBUTING.md][].

[as fun]: https://twitter.com/izs/status/187639633641865216
[CONTRIBUTING.md]: CONTRIBUTING.md
[style guide]: STYLE-GUIDE.md
[Why We Write Docs section]: #why-we-write-docs
[What We Write section]: #what-we-write
[How We Write section]: #how-we-write
[Django's getting started guide]: https://docs.djangoproject.com/en/1.8/intro/tutorial01/
