# StudioCMS Ecosystem Roadmap

## Overview

- [Glossary](#glossary)
- [Stage 1: Proposal](#stage-1-proposal)
- [Stage 2: Accepted Proposal](#stage-2-accepted-proposal)
- [Stage 3: RFC \& Development](#stage-3-rfc--development)
- [Stage 4: Ship it!](#stage-4-ship-it)

## Glossary

> **Proposal Champion:** A proposal is more likely to move forward in this process if it has a **champion** attached to it. This role is self-nominated and open to anyone (both maintainers and community members are welcome to volunteer). It may be the original proposal author, or someone who joins later. The responsibility of a champion is to help shepard the proposal through the later parts of this process, including: writing the detailed RFC, responding to and incorporating feedback, and eventually implementing the proposal in code.
>
> **You are not alone as a champion!** If this is your first time writing an RFC or design document, our maintainer team is expected to work with you and guide you through this process.

## Stage 1: Proposal

### Existing project / Import into StudioCMS Ecosystem

**Goal:** Have a project you feel would help benefit the StudioCMS Ecosystem? Already have a start on the project or a working project you wish to join into the main project org?

**Requirements:** All you have to do is, [open a new issue](https://github.com/withstudiocms/roadmap/issues) using our [existing project template]().

**Location:** GitHub Issues [(see current/past issues).](https://github.com/withstudiocms/roadmap/issues)

### New Ideas / projects

**Goal:** Unstructured, low-friction conversations on ideas and improvements to Astro. Useful for gathering early feedback and gauging interest with the community and maintainers.

**Requirements:** None! To suggest an improvement, [create a new Discussion](https://github.com/withstudiocms/roadmap/discussions) using our (completely optional) [proposal template]().

**Location:** GitHub Discussions [(see all open proposals).](https://github.com/withstudiocms/roadmap/discussions) The StudioCMS Discord channel `#contribute` can also be used to throw an idea out for quick initial feedback, but be warned that chat is short-lived and not designed for longer-lived discussion.

## Stage 2: Accepted Proposal

**Goal:** Confirm proposal feasibility with StudioCMS Maintainers ( [@withstudiocms/revered](https://github.com/orgs/withstudiocms/teams/revered) and [@withstudiocms/exalted](https://github.com/orgs/withstudiocms/teams/exalted) )

**Requirements:** An existing proposal (Stage 1). In addition, a proposal is more likely to be accepted if it is detailed and well thought-out, can demonstrate community interest, has at least one champion volunteer, has a Maintainer ([@withstudiocms/revered](https://github.com/orgs/withstudiocms/teams/revered) or above) acting as a champion, and has buy-in/interest from StudioCMS maintainer(s).

**Location:** GitHub Issues [(see all accepted proposals).](https://github.com/withstudiocms/roadmap/issues)

**What to Expect:** A proposal reaches this stage (aka "is accepted") during an [RFC Meeting/Vote](#rfc-meetings-and-votes) with Maintainers and Core Team ( [@withstudiocms/revered](https://github.com/orgs/withstudiocms/teams/revered) and [@withstudiocms/exalted](https://github.com/orgs/withstudiocms/teams/exalted) ), following our existing [RFC voting](#voting-rfc-proposals) process.

When a proposal is accepted, a maintainer (@withstudiocms/revered or above) will create a new GitHub Issue summarizing the original proposal using our official template. (Or flagging the issue with the label `Accepted proposal`)

The proposal's original author will be given a chance to volunteer to be its champion. If they refuse, someone else can volunteer for the position by posting in the GitHub Issue. An accepted proposal will remain an open issue until a champion is confirmed by Core Team. Once confirmed, the champion is free to advance the proposal to the next stage.

In some cases, a proposal may be explicitly rejected by Core Team if it is known to be infeasible, or go against some existing goals/mission of the project. In the event of an explicit rejection, a Core Team member will comment on to the proposal explaining the reasoning for rejection.

A stale, accepted proposal can be removed (rejected after a previous acceptance) at any time following the same, existing [RFC Proposal](#voting-rfc-proposals) voting process.

## Stage 3: RFC & Development

**Goal:** Begin development! Gather implementation feedback and work with maintainers during development.

**Requirements:** An accepted proposal (Stage 2) and a proposal champion to author and implement the RFC.

**Location:** GitHub Pull Requests [(see all in-progress RFCs)](https://github.com/withstudiocms/roadmap/pulls) [(see all finished RFCs)](https://github.com/studiocms/roadmap/tree/main/proposals)

**What to Expect:** To create an RFC for an already-accepted proposal, the proposal champion must use our [`stage-3--rfc-template.md`]() RFC template in the repo. The initial sections of the RFC template should be copy-pasted from the the accepted proposal (they match 1:1). All remaining sections are left for the champion to complete with the implementation and tradeoff details of the RFC.

When a Stage 3 RFC is opened, the Stage 2 RFC should be closed with a comment that links to the Stage 3 RFC pull request.

You do not need to get an RFC approved before beginning development! One of the best ways to validate your RFC is to prototype, so early prototyping and parallel development alongside the RFC is strongly encouraged. The RFC is a living document during this stage, and is most useful for gathering feedback as you build. An RFC will not be accepted and merged until it's PR is also ready to merge.

The proposal champion can request feedback on their RFC at any point, either asynchronously in Discord (inside the `#contribute`/`#ptal` channel). Maintainers are expected to provide timely feedback at this stage so that the RFC author is never blocked.

## Stage 4: Ship it!

An RFC is ready to be approved and finalized once it's Pull Request is ready for its final review. When a champion thinks the RFC is ready he can ask for a call for consensus.

At this time, some member of the core team will motion for a final comment period (FCP). This follows our existing [RFC Proposal](#voting-rfc-proposals) voting process. Once the final comment period has elapsed the RFC will be merged if there are no objections.

## RFC Meetings and Votes

RFCs advance through the stages during RFC meetings/votes with the Core team and Maintainers. Voting follows the [RFC proposal](#voting-rfc-proposals) voting process.

Meetings occur ad hoc rather than on a scheduled basis. They are called for when a proposal author or champion feels it is ready to advance to the next stage. The author or champion can ask for a meeting by contacting the [Core team](https://github.com/orgs/withstudiocms/teams/exalted) to schedule a time.

All maintainers are invited to the meeting/vote. If consensus is reached, the RFC advances to the next stage. See [RFC proposal](#voting-rfc-proposals) documentation for full details.

## Voting: RFC Proposals

Astro features are discussed using a model called [Consensus-seeking decision-making](https://en.wikipedia.org/wiki/Consensus-seeking_decision-making). This model attempts to achieve consensus on all significant changes to Astro, but has a fallback voting procedure in place if consensus appears unattainable.

**Who can vote:** All Core members and Maintainers.

1. Anyone can submit an RFC to suggest changes to Astro.
2. A trivial change can be discussed and approved entirely within the RFC GitHub issue, as long as there are no objections from Core or Maintainer members. This is not considered a formal vote.
3. A non-trivial, significant change should be discussed within the RFC and approved during an RFC meeting call/vote. In some cases, an RFC may be approved outside of an RFC meeting using Pull Request reviews as a proxy for votes.
4. During an RFC meeting/vote, the person leading the call/vote will attempt to achieve consensus on the RFC proposal.
5. **If consensus is reached:** the RFC is approved.
6. **If consensus is not reached:** The RFC author and Core members must make all reasonable attempts to resolve issues and reach consensus in GitHub or a follow-up RFC meeting. The process of reaching consensus can take time, and should not be rushed as long as all participants are making a reasonable effort to respond.
7. **If consensus still cannot be reached:** The Core team may invoke [rough consensus](https://en.wikipedia.org/wiki/Rough_consensus) to resolve an RFC that has not achieved absolute consensus, as described below (borrowed from the [IETF](https://datatracker.ietf.org/doc/html/rfc2418)):

> Working groups make decisions through a "rough consensus" process. Astro consensus does not require that all participants agree although this is, of course, preferred. In general, the dominant view of the TSC shall prevail. (However, "dominance" is not to be determined on the basis of volume or persistence, but rather a more general sense of agreement). Consensus can be determined by a show of hands, humming, or any other means on which the TSC agrees (by rough consensus, of course). Note that 51% of the TSC does not qualify as "rough consensus" and 99% is better than rough. It is up to the project Steward to determine if rough consensus has been reached.

---

#### Prior Art / Special Thanks

This process is adopted based on [Astro's RFC/proposal process](https://github.com/withastro/roadmap) which is based on [Remix's Open Development process](https://remix.run/blog/open-development), which had been based on the RFC processeses of the Vue, React, Rust, and Ember projects.
