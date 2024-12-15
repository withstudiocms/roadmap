<!--
  Community members who would like to propose an idea or feature should begin
  by creating a GitHub Discussion. See the repo README.md for more info.

  To use this template: create a new, empty file in the repo under `proposals/${ID}.md`.
  Replace `${ID}` with the official accepted proposal ID, found in the GitHub Issue
  of the accepted proposal.
-->

**If you have feedback and the feature is released as experimental, please leave it on the Stage 3 PR. Otherwise, comment on the Stage 2 issue (links below).**

- Start Date: <!-- today's date, YYYY-MM-DD -->
- Reference Issues: <!-- related issues, otherwise leave empty -->
- Implementation PR: <!-- leave empty -->
- Stage 2 Issue: <!-- fill in -->
- Stage 3 PR: <!-- related roadmap PR, leave it empty if you don't have a PR yet -->

# Summary

A brief, one or two sentence explanation of the proposal.

# Example

If the proposal involves a new or changed API, then include a basic code example.
Otherwise, omit this section if it's not applicable.

# Background & Motivation

Include any useful background detail that that explains why this RFC is important.
What are the problems that this RFC sets out to solve? Why now? Be brief!

It can be useful to illustrate your RFC as a user problem in this section.
(ex: "Users have reported that it is difficult to do X in Astro today.")

# Goals

A **concise, bulleted-list** outlining the intended goals of this RFC.

- What are the exact problems that you are trying to solve with this RFC?
- Separate these goals from the solution that you will outline below.
- If this RFC isn't approved, these goals can be used to develop alternative solutions.

# Non-Goals

A **concise, bulleted-list** outlining anything intentionally left out of this RFC:

- Non-goal: A goal that is intentionally not addressed in this RFC.
- Out-of-scope: A goal that is related, but intentionally avoided here.
- Future: A goal that is related, but left to be addressed in the future.

This gives the reader the correct context on what is intentionally left out of scope.
It is okay to leave this section empty.

# Detailed Design

This is the bulk of the RFC. Explain the design in enough detail for somebody
familiar with StudioCMS to understand, and for somebody familiar with the
implementation to implement. This should get into specifics and corner-cases,
and include examples of how the feature is used. Any new terminology should be
defined here.

# Testing Strategy

How will this feature's implementation be tested? Explain if this can be tested with
unit tests or integration tests or something else. If relevant, explain the test
cases that will be added to cover all of the ways this feature might be used.

# Drawbacks

Why should we _not_ do this? Please consider:

- Implementation cost, both in term of code size and complexity.
- Whether the proposed feature can be implemented in user space.
- Impact on teaching people StudioCMS.
- Integration of this feature with other existing and planned features
- Cost of migrating existing StudioCMS applications (_is it a breaking change?_)

There are tradeoffs to choosing any path. Attempt to identify them here.

# Alternatives

What other designs have been considered? What is the impact of not doing this?

# Adoption strategy

Please consider:

- If we implement this proposal, how will existing StudioCMS developers adopt it?
- Is this a breaking change? Can we write a codemod?
- Can we provide a runtime adapter library for the original API it replaces?
- How will this affect other projects in the StudioCMS ecosystem?

# Unresolved Questions

Optional, but suggested for first drafts.
What parts of the design are still to be determined?
