# Contributing to the Docs

If you're reading this, you want to contribute to the docs. That's great! Take
a second to pat yourself on the back, then go [read the guide][]. We'll wait.

... OK, cool.

Once you've read the guide, you should be able to comfortably answer why we're
writing docs here, what sort of docs we write, and how we go about writing
them. If you're unclear on any of that, [open an issue][] with questions!

This document exists to walk you through the process of how contributions work
in this repo – including [some assertions][] about what we expect you to be
able to claim about your work, and [some guidelines][] for how to interact with
others while you're here. This document will address five goals:

1. "I want to [**change** a doc][]!"
2. "I want to [**write** a doc][]!"
3. "I want to [**join** the team][]!"
4. "I want to [**review** a doc][]!"
5. "I want to [**merge** changes][]!"

What's common to all of them is the process to expect on the tracker:

1. The author submits a change to the repository in the form of a PR.
2. A reviewer will review the changes and may make suggestions.
3. Once a reviewer has given the work a "LGTM" stamp of approval,
  1. if the author has the ability to merge, they may merge the work at this
  point.
  2. if the author does not have access, the reviewer should merge the work.

If you have questions at **any point** – whether it's about this process or
about a specific doc – [open an issue on the tracker][]. Remember, you're doing
the project a **favor** by asking questions – other people might have the same
question in mind, and this gives the docs team a chance to see how effective
the documentation is.

## To **change** a document:

1. *Fork* the appropriate repository to your account.
  1. This is usually <https://github.com/nodejs/node>.
2. *Clone* your fork.
3. Make your changes locally.
4. *Commit* your changes to a new branch.
5. *Push* that branch to your repository.
6. *Open* a PR.
  1. Make sure you include a description of *why* you're making the changes.
7. Respond to feedback by making edits and pushing them to your local branch.
  1. When you're done making requested edits, *comment* "Ready for review!" on
  the PR.
8. Once your reviewer comments "LGTM" your changes are ready to merge.
  1. Not all changes will be merge-able – don't be discouraged! Closed PRs
  are not "failed" PRs – they're valuable feedback, both for the submitter *and*
  the reviewer. Closed PRs help tell the project what it is just as much as
  merged PRs.
  2. Your PR will also be subject to the contribution rules of the repository
  you're making it on, so be mindful of them.

## To **write** a document:

1. *Open* an issue on this repository describing the sort of document you'd like
to write.
  1. Include details about what audience you're addressing,
  2. what idea you'd like to convey to that audience,
  3. where you'll put the document,
  4. and how other docs will relate to it.
  5. Consult [the guide][] for, er, guidance on what to write.
2. Gather feedback on your proposed document!
  1. If you're fairly confident that your proposed document is *relevant* and
  *helpful*, go ahead and start working on it.
  2. If you're unsure, note your uncertainty in the issue, and wait for feedback
  to see whether the document is needed before starting work on it.
3. To start work on your document, follow the [above process][] for **changing** a
document.

## To **join** the team:

If you'd like to join the documentation team, that's great! Note your interest
[on this issue][]. We'll get in contact with you shortly afterwards. Note that
as part of the team, you are expected to be an *exemplar* of the project's
values – both in making this specific project a welcoming place to contribute,
as well as in the larger community (other issue trackers, conferences, etc.)

The full details of membership access and responsibilities are listed in
[the `GOVERNANCE.md` file][docs-governance].

The description on membership or collaboratorship is in [GOVERNANCE.md][]

## To **review** a document:

1. If a PR already has an assigned team member, post a comment on the PR asking
that team member if it's okay for you to help.
  1. If the other team member says it's OK, then procede.
  2. Otherwise, if you still have concerns, contact the team member via email
  with your review-related concerns. If your concerns are team-member-related,
  direct them to the [nodejs/diversity working group][].
2. If the PR does not have an assigned member, feel free to assign yourself!
Once you are assigned to a PR, you are fully responsible for the success of it.
3. Begin the editing loop:
  1. Read the entire document.
  2. Make structural comments first.
  3. If you have no structural comments, make grammar and spelling comments.
  4. Once you are done reviewing,
    1. If you've commented, comment "review done."
      1. Once the author comments to the effect of "ready for review,"
      restart the editing loop.
    2. If you have no further comments, you may:
      1. Ask another team member to review. It's usually best to
         get two LGTMs before merging.
      2. Comment "LGTM", and:
        1. If the author is not a team member, [merge their changes][].
        2. If the author is a team member, they may merge their own changes.

Guidelines for commenting on work:

* Your goal as an editor is to make the documentation serve our audience
  better.
* Secondary to that, your goal is to make the review process a painless,
  successful experience for the author.
  * This means commenting on the *work*, not the *author*.
  * If the work does not make the documentation better for our audience overall,
    * Explain why it does not,
    * and suggest other avenues the author can follow to achieve their goal.
  * "Success" means the author felt their effort was valued, not necessarily
    that the PR was ultimately merged.
* Respect the author's time and effort. Be kind.
* Speak objectively, and try to back up your comments with examples.
* If you don't agree with the author, consider that you might
  not understand their point of view. Try to get them to explain further, or in
  different terms, so that you might better understand them.
* Avoid condescension (and the appearance of condescension.) Communicate as
  equals.

## To **merge** changes:

For this repository, once a PR has a LGTM, any team member in full standing may
merge it. Team members under mentorship may merge with the permission of their
mentor.

Patches may be merged using the big green GitHub merge button if there are no
conflicts.

If there are conflicts, the PR should be updated to resolve any conflicts, and
should be briefly re-reviewed before merging.

For other repositories, their processes for merging apply.

## Developer's Certificate of Origin 1.0

By making a contribution to this project, I certify that:

* (a) The contribution was created in whole or in part by me and I
  have the right to submit it under the open source license indicated
  in the file; or
* (b) The contribution is based upon previous work that, to the best
  of my knowledge, is covered under an appropriate open source license
  and I have the right under that license to submit that work with
  modifications, whether created in whole or in part by me, under the
  same open source license (unless I am permitted to submit under a
  different license), as indicated in the file; or
* (c) The contribution was provided directly to me by some other
  person who certified (a), (b) or (c) and I have not modified it.


## Code of Conduct

Before jumping into the rest of the Code of Conduct, it is important to note
that the values of this project are derived from the values of the Node.js
project at-large. As those change, so ours will change to reflect them.

Once they are documented, they will be linked to from here.

This Code of Conduct is adapted from [Rust's wonderful
CoC](http://www.rust-lang.org/conduct.html).

* We are committed to providing a friendly, safe and welcoming
  environment for all, regardless of gender, sexual orientation,
  disability, ethnicity, religion, or similar personal characteristic.
* Please avoid using overtly sexual nicknames or other nicknames that
  might detract from a friendly, safe and welcoming environment for
  all.
* Please be kind and courteous. There's no need to be mean or rude.
* Respect that people have differences of opinion and that every
  design or implementation choice carries a trade-off and numerous
  costs. There is seldom a right answer.
* Please keep unstructured critique to a minimum. If you have solid
  ideas you want to experiment with, make a fork and see how it works.
* We will exclude you from interaction if you insult, demean or harass
  anyone.  That is not welcome behaviour. We interpret the term
  "harassment" as including the definition in the [Citizen Code of
  Conduct](http://citizencodeofconduct.org/); if you have any lack of
  clarity about what might be included in that concept, please read
  their definition. In particular, we don't tolerate behavior that
  excludes people in socially marginalized groups.
* Private harassment is also unacceptable. No matter who you are, if
  you feel you have been or are being harassed or made uncomfortable
  by a community member, please contact one of the channel ops or any
  of the TC members immediately with a capture (log, photo, email) of
  the harassment if possible.  Whether you're a regular contributor or
  a newcomer, we care about making this community a safe place for you
  and we've got your back.
* Likewise any spamming, trolling, flaming, baiting or other
  attention-stealing behaviour is not welcome.
* Avoid the use of personal pronouns in code comments or
  documentation. There is no need to address persons when explaining
  code (e.g. "When the developer")

[nodejs/diversity working group]: https://github.com/nodejs/diversity
[read the guide]: GETTING-STARTED.md
[open an issue]: https://github.com/nodejs/docs/issues/new
[some assertions]: #developers-certificate-of-origin-10
[some guidelines]: #code-of-conduct
[**change** a doc]: #to-change-a-document
[**write** a doc]: #to-write-a-document
[**join** the team]: #to-join-the-team
[**review** a doc]: #to-review-a-document
[**merge** changes]: #to-merge-changes
[open an issue on the tracker]: https://github.com/nodejs/docs/issues/new
[the guide]: GETTING-STARTED.md
[above process]: #to-change-a-document
[on this issue]: https://github.com/nodejs/docs/issues/2
[nodejs/diversity working group]: https://github.com/nodejs/diversity
[merge their changes]: #to-merge-changes
[GOVERNANCE.md]: GOVERNANCE.md
[docs-governance]: ./GOVERNANCE.md
