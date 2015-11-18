# Documentation Working Group

The Node.js Documentation group is jointly governed by a Working Group (WG)
which is responsible for high-level guidance of the project.

The WG has final authority over this project including:

* Technical direction
* Project governance and process (including this policy)
* Contribution policy
* GitHub repository hosting
* Conduct guidelines
* Maintaining the list of additional Collaborators

For the current list of WG members, see the project README.md.

## Collaborators

The Node.js Documenation WG GitHub repository is maintained by the WG and
additional Collaborators who are added by the WG on an ongoing basis.

Individuals making significant and valuable contributions are made Collaborators
and given commit-access to the project. These individuals are identified by the
WG and their addition as Collaborators is discussed over GitHub issues - at time
of writing, these individuals are encouraged to comment on [this specific
issue][].

Modifications of the contents of the Node.js Documentation WG repository are
made on a collaborative basis. Anybody with a GitHub account may propose a
modification via pull request and it will be considered by the project
Collaborators. All pull requests must be reviewed and accepted by a Collaborator
with sufficient expertise who is able to take full responsibility for the
change. In the case of pull requests proposed by an existing Collaborator, an
additional Collaborator is required participate and there is disagreement around
a particular modification. See _Consensus Seeking Process_ below for further
detail on the consensus model used for governance.

Collaborators may opt to elevate significant or controversial modifications, or
modifications that have not found consensus to the WG for discussion by
assigning the `wg-agenda` tag to a pull request or issue. The WG should serve as
the final arbiter where required.

For the current list of Collaborators, see the project `README.md`.

## WG Membership

WG seats are not time-limited.  There is no fixed size of the WG. However, the
expected target is between 6 and 12, to ensure adequate coverage of important
areas of expertise, balanced with the ability to make decisions efficiently.

There is no specific set of requirements or qualifications for WG membership
beyond these rules.

The WG may add additional members to the WG by unanimous consensus.

A WG member may be removed from the WG by voluntary resignation, or by unanimous
consensus of all other WG members.

Changes to WG membership should be posted in the agenda, and may be suggested as
any other agenda item (see "WG Meetings" below).

No more than 1/3 of the WG members may be affiliated with the same employer. If
removal or resignation of a WG member, or a change of employment by a WG member,
creates a situation where more than 1/3 of the WG membership shares an employer,
then the situation must be immediately remedied by the resignation or removal of
one or more WG members affiliated with the over-represented employer(s).

## WG Agenda

<!-- this part needs to be rewritten. Will follow up with another commit that has those edits. -->

Each week, an issue tagged `wg-weekly` will be created. It will be a sort of
weekly digest on what's happened within the docs WG. The `wg-weekly` posts will
contain links and descriptions to issues tagged with `wg-agenda`. The topics
links are to be discussed within their respective `wg-agenda` tagged issues, **not**
in the `wg-weekly` topics.

Items are tagged with `wg-agenda` which are considered contentious or are
modifications of governance, contribution policy, WG membership, or release
process.

The intention of the `wg-agenda` tag is not to seek approval or review all
patches proposed - that should happen continuously on GitHub and be handled by
the larger group of Collaborators.

Any community member or contributor can ask that issues be tagged with the
`wg-agenda` tag by asking in the respective GitHub Issue. Any Collaborator, WG
member or the moderator can add the item to the agenda by adding the `wg-agenda`
tag to the issue themselves.

The moderator is responsible for summarizing the discussion of each agenda item
and send it as a pull request after the meeting.

### Consensus Seeking Process

The WG follows a [Consensus Seeking][] decision making model.

When an agenda item has appeared to reach a consensus the moderator will ask
"Does anyone object?" as a final call for dissent from the consensus.

If an agenda item cannot reach a consensus a WG member can call for either a
closing vote or a vote to table the issue to the next meeting. The call for a
vote must be seconded by a majority of the WG or else the discussion will
continue. Simple majority wins.

Note that changes to WG membership require unanimous consensus.  See "WG
Membership" above.

[this specific issue]: https://github.com/nodejs/docs/issues/2
[Consensus Seeking]: http://en.wikipedia.org/wiki/Consensus-seeking_decision-making
