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

For the current list of WG members, see [the project README.md][nodejs-docs-].

## Membership

### Joining the WG

Membership may be extended by current WG members to individuals who have made
contributions to documentation in the Node or JavaScript communities who **have
expressed interest in membership**. Candidates for membership will be approved
or denied by existing WG members using the [Consensus Seeking
Process][consensus] process below. Individuals may express interest publicly on
the [sign-up issue][sign-up] or privately to any existing Docs WG member. Put
simply: **if you are a documentarian and are willing to fulfill the
[responsibilities of membership][membership-responsibilities] to the best of
your ability, the Docs WG would be happy to receive your help.**

The Docs WG encourages prospective members to read the
[CONTRIBUTING.md][nodejs-doc-contributing] and
[GETTING-STARTED.md][nodejs-doc-getting-started] documents for an idea of how
the WG operates.

### Membership Access and Responsibilities

Membership in the Node.js Documentation WG entails the following access:

* Membership in the [Node.js Documentation Slack][nodejs-doc-slack].
* Membership in the **@nodejs/documentation** GitHub team.
* Collaboratorship on the [Node.js Documentation Repository][nodejs-doc-repo].

Members should prepare to take part in the following activities, to the best of
their abilities:

* Attend meetings in the form of Google Hangouts.
* Coordinate via [**nodejs/docs** issues][nodejs-doc-repo].
* Coordinate with WG members via [Slack][nodejs-doc-slack].
* Respond to pull requests, and issues on the **nodejs/node** tracker that:
  * are tagged with the `doc` label, OR
  * have cc'd **@nodejs/documentation**, OR
  * modify the `doc/` or `tools/docs` directory.
* Apply the [editing standards][nodejs-doc-standards] recommended by the WG to
  all documentation review.
* Keep the [goals][nodejs-doc-goals] set by the WG in mind when contributing
  documentation.

**The WG recognizes that this is largely a volunteer effort, and will endeavour
to adjust the time commitment of participation in the WG to reflect that.** If
you would like to contribute, but cannot participate in one or more of the
above tasks, please contact a WG member. The WG will attempt to make
accomodations for interested individuals. *Members are not required to be
collaborators on the `nodejs/node` repository.*

Members are expected to conduct themselves according to the [Docs WG Code of
Conduct][nodejs-doc-coc] as well as any Code of Conduct set by the larger Node
Foundation. The Code of Conduct is enforced by the [Moderation
WG][nodejs-moderation]. Any Docs WG member banned from the Node project by the
Moderation WG will also be removed from the Docs WG. To report a violation of
the Code of Conduct, please [follow the steps listed
here][nodejs-moderation-request].

### Membership Collaboration

#### Documentation Review and Copyediting

Follow the process outlined in [CONTRIBUTING.md][nodejs-doc-contributing].

#### Changes to Docs WG Guidelines and Process

Modifications of the contents of the Node.js Documentation WG repository are
made on a collaborative basis. Anybody with a GitHub account may propose a
modification via pull request and it will be considered by the project
Collaborators. All pull requests must be reviewed and accepted by a
Collaborator with sufficient expertise who is able to take full responsibility
for the change. In the case of pull requests proposed by an existing
Collaborator, an additional Collaborator is required participate if there is
disagreement around a particular modification. [See _Consensus Seeking Process_
below][consensus] for further detail on the consensus model used for
governance.

Collaborators may opt to elevate significant or controversial modifications, or
modifications that have not found consensus, to the WG for discussion by
assigning the `wg-agenda` tag to a pull request or issue. The WG should serve as
the final arbiter where required.

#### Additional Membership Constraints

WG seats are not time-limited. There is no fixed size of the WG. There is no
specific set of requirements or qualifications for WG membership beyond rules
set forth in this document.

The WG may add additional members to the WG by unanimous consensus.

A WG member may be removed from the WG by voluntary resignation, by unanimous
consensus of all other WG members, or by ruling from the Node.js Moderation WG.

Changes to WG membership should be posted in the agenda, and may be suggested as
any other agenda item (see "WG Meetings" below).

No more than 1/3 of the WG members may be affiliated with the same employer. If
removal or resignation of a WG member, or a change of employment by a WG member,
creates a situation where more than 1/3 of the WG membership shares an employer,
then the situation must be immediately remedied by the resignation or removal of
one or more WG members affiliated with the over-represented employer(s).

#### WG Meeting Agenda

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

A regular cadence will be determined for meetings by consent of the WG.

#### Consensus Seeking Process

The WG follows a [Consensus Seeking][external-consensus] decision making model.

When an agenda item has appeared to reach a consensus the moderator will ask
"Does anyone object?" as a final call for dissent from the consensus.

If an agenda item cannot reach a consensus a WG member can call for either a
closing vote or a vote to table the issue to the next meeting. The call for a
vote must be seconded by a majority of the WG or else the discussion will
continue. Simple majority wins.

Note that changes to WG membership require unanimous consensus.  See "WG
Membership" above.

[consensus]: #consensus-seeking-process
[sign-up]: https://github.com/nodejs/docs/issues/2
[membership-responsibilities]: #membership-access-and-responsibilities
[nodejs-doc-slack]: https://nodejs-docs.slack.com/
[nodejs-doc-repo]: https://github.com/nodejs/docs
[nodejs-doc-standards]: https://github.com/nodejs/docs/blob/master/GETTING-STARTED.md#how-we-write
[nodejs-doc-goals]: https://github.com/nodejs/docs/blob/master/GETTING-STARTED.md#why-we-write-docs
[nodejs-doc-coc]: https://github.com/nodejs/docs/blob/master/CONTRIBUTING.md#code-of-conduct
[nodejs-moderation]: https://github.com/nodejs/moderation
[nodejs-moderation-request]: https://github.com/nodejs/TSC/blob/master/Moderation-Policy.md#requesting-moderation
[nodejs-doc-contributing]: ./CONTRIBUTING.md
[nodejs-doc-getting-started]: ./GETTING-STARTED.md
[external-consensus]: http://en.wikipedia.org/wiki/Consensus-seeking_decision-making
