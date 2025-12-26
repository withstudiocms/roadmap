<!--
  Community members who would like to propose an idea or feature should begin
  by creating a GitHub Discussion. See the repo README.md for more info.

  To use this template: create a new, empty file in the repo under `proposals/${ID}.md`.
  Replace `${ID}` with the official accepted proposal ID, found in the GitHub Issue
  of the accepted proposal.
-->

**If you have feedback and the feature is released as experimental, please leave it on the Stage 3 PR. Otherwise, comment on the Stage 2 issue (links below).**

- Start Date: 2025-12-17
- Reference Issues: 
- Implementation PR(s): 
  - [withstudiocms/studiocms PR #1081](https://github.com/withstudiocms/studiocms/pull/1081)
  - [withstudiocms/studiocms PR #1085](https://github.com/withstudiocms/studiocms/pull/1085)
  - [withstudiocms/studiocms PR #1086](https://github.com/withstudiocms/studiocms/pull/1086)
  - [withstudiocms/studiocms PR #1098](https://github.com/withstudiocms/studiocms/pull/1098)
  - [withstudiocms/studiocms PR #1099](https://github.com/withstudiocms/studiocms/pull/1099)
  - [withstudiocms/studiocms PR #1100](https://github.com/withstudiocms/studiocms/pull/1100)
  - [withstudiocms/studiocms PR #1101](https://github.com/withstudiocms/studiocms/pull/1101)
  - [withstudiocms/studiocms PR #1102](https://github.com/withstudiocms/studiocms/pull/1102)
  - [withstudiocms/studiocms PR #1106](https://github.com/withstudiocms/studiocms/pull/1106)
  - [withstudiocms/studiocms PR #1107](https://github.com/withstudiocms/studiocms/pull/1107)
  - [withstudiocms/studiocms PR #1108](https://github.com/withstudiocms/studiocms/pull/1108)
- Stage 2 Issue: [withstudiocms/roadmap #10](https://github.com/withstudiocms/roadmap/issues/10)
- Stage 3 PR: <!-- related roadmap PR, leave it empty if you don't have a PR yet -->

# Summary

Implement a Dynamic Media/Storage manager plugin system to be able to connect StudioCMS to different types of storage mediums such as S3.

# Example

# Background & Motivation

This proposal is inspired by the [Astro Cloudinary upload widget](https://astro.cloudinary.dev/clduploadwidget/basic-usage). The idea is providing a similar interface on the StudioCMS dashboard for the image url textboxes (and other places where media assets are involved). To keep things flexible, the plan is to introduce a new type of plugin which won't get involved with adding any custom routes and/or pages. For more details, please see the Goals section.

# Goals

- Introduce new Storage Manager plugin type:
  - Storage Manager will work similar to Astro Adapters in the way that under the hood they are just an integration with the same hooks but have a extra custom hook for specific adapter tasks
  - Storage managers will be responsible for providing the underlying API client while StudioCMS will handle providing the other parts of the API
- Introduce a new StorageFileBrowser component to handle interfacing with the new StorageManagerAPI
  - System will interface with StorageManagerAPI and tie to a input element and a trigger button on the dashboard
  - Optionally be able to function with just a trigger button for Storage Management for Admins
- Documenting the new plugin type structure and guides for adding new storage providers with code examples

# Prototyping
- https://github.com/Adammatthiesen/s3-interface-test
