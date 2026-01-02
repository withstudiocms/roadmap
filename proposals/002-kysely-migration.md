<!--
  Community members who would like to propose an idea or feature should begin
  by creating a GitHub Discussion. See the repo README.md for more info.

  To use this template: create a new, empty file in the repo under `proposals/${ID}.md`.
  Replace `${ID}` with the official accepted proposal ID, found in the GitHub Issue
  of the accepted proposal.
-->

**If you have feedback and the feature is released as experimental, please leave it on the Stage 3 PR. Otherwise, comment on the Stage 2 issue (links below).**

- Start Date: 2025-12-01
- Reference Issues: <!-- related issues, otherwise leave empty -->
- Implementation PR: [withstudiocms/studiocms PR #991](https://github.com/withstudiocms/studiocms/pull/991)
- Stage 2 Issue: [withstudiocms/roadmap Issue #8](https://github.com/withstudiocms/roadmap/issues/8)
- Stage 3 PR: [withstudiocms/roadmap PR #9](https://github.com/withstudiocms/roadmap/pull/9)

# Summary

Migrate StudioCMS from AstroDB to Kysely with new custom packages for handling.

## Champion

- Adam Matthiesen ([@Adammatthiesen](https://github.com/Adammatthiesen))

# Background & Motivation

Currently we rely on AstroDB and drizzle-orm, which in their current configuration has some minor issues, but even once it technically supports multiple dialects there would be the issue of slight difference in the resulting drizzle client between dialects. This will make it difficult to properly support AstroDB once user's will be able to swap out their driver (since each table would need a different schema based on the current dialect).

Kysely on the other-hand, has support for all the same db dialects but with a single unified interface to work with that supports many different dialects with easy switching during initialization. Kysely also has a fairly similar interface but without all the extra helper imports needed to build a db query.

# Goals

- Introduce a new `@withstudiocms` scoped package that will include:
  - Kysely interfaces
  - shared public DB types and helpers
  - Migration and schema utilities
  - Utilize Effect for basic operations
- Implement CLI to manage migrations/db initialization in StudioCMS
  - Pull migrations and schemas from shared package
- Implement DB Client and replace drizzle-orm in StudioCMS SDK and CLI
  - Utilize utils & types from shared package
  - Will allow us to overhaul the current SDK and replace it with a even more dynamic system

# Non-Goals

- We could support more than just sqlite/libsql quickly
- If this goes, we would be able to skip a bunch of steps towards leaving beta versioning.