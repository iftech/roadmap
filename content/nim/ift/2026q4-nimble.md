---
title: 2026q4 Nimble
tags:
  - "2026q4"
  - "nim"
  - "ift"
draft: false
description: Continue Nimble development and review its integration into Messaging, Storage, and Nimbus CI workflows.
---

`ift-ts:nim:ift:2026q4-nimble`

## Description

Continue improving Nimble as a reliable package and build tool for downstream teams.
Build on the Q3 development track and review how Messaging, Storage, and Nimbus use Nimble in CI, identifying integration gaps and coordinating fixes with each team.

## Task List

### Nimble development

* fully qualified name: `ift-ts:nim:ift:2026q4-nimble:development`
* owner: Juan/Constantine
* status: in progress (50%)
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Continue Nimble development, stabilization, and issue resolution from Q3.
Prioritize outstanding development goals, dependency resolution and lockfile reliability, package installation, and build behavior needed by downstream projects.
Add regression coverage for fixes and update usage documentation when behavior changes.

#### Deliverables
- [nim-lang/nimble#1879](https://github.com/nim-lang/nimble/pull/1879) Warn when updating nimble from a nimble in a different path
- [nim-lang/nimble#1878](https://github.com/nim-lang/nimble/pull/1878) Resolve the version of a named package instead of reusing its cached…
- [nim-lang/nimble#1880](https://github.com/nim-lang/nimble/pull/1880) Docs: Add a note about when to use lock files.
- [nim-lang/nimble#1884](https://github.com/nim-lang/nimble/pull/1884) Refactor: Split dependency resolution into nimblesolver, nimblesat and nimblepubgrub
- [nim-lang/nimble#1883](https://github.com/nim-lang/nimble/pull/1883) Parse each version once in PubGrub instead of on every comparison
- [nim-lang/nimble#1882](https://github.com/nim-lang/nimble/pull/1882) Add --solver:pubgrub
- [nim-lang/nimble#1899](https://github.com/nim-lang/nimble/pull/1899) Fix cached version discovery hiding newer untagged HEAD versions
- [nim-lang/nimble#1898](https://github.com/nim-lang/nimble/pull/1898) bump 0.26.1
- [nim-lang/nimble#1897](https://github.com/nim-lang/nimble/pull/1897) bump chronos
- [nim-lang/nimble#1896](https://github.com/nim-lang/nimble/pull/1896) Fix shell and option injection in VCS commands
- [nim-lang/nimble#1895](https://github.com/nim-lang/nimble/pull/1895) Fix NimScript dependency paths and bootstrap exception handling
- [nim-lang/nimble#1893](https://github.com/nim-lang/nimble/pull/1893) Bumps the nim used to build nimble
- [nim-lang/nimble#1891](https://github.com/nim-lang/nimble/pull/1891) Read taskRequires in any spelling and only for the root package (fixes #1889)
- [nim-lang/nimble#1890](https://github.com/nim-lang/nimble/pull/1890) Keep lock file pins within one PubGrub solve instead of trying them one by one
- [nim-lang/nimble#1887](https://github.com/nim-lang/nimble/pull/1887) Fix nimlangserver tests
- [nim-lang/nimble#1886](https://github.com/nim-lang/nimble/pull/1886) Prefer the system Nim within one PubGrub solve instead of pinning and re-solving

### CI integration review

* fully qualified name: `ift-ts:nim:ift:2026q4-nimble:ci-integration-review`
* owner: TBD
* status: not started
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Review Nimble integration into the CI workflows of Logos Messaging, Logos Storage, and Nimbus.
For each project, inspect the current integration, dependency and lockfile handling, toolchain selection, caching, and build/test execution on its supported CI platforms.
Identify gaps or failures, agree follow-up work with the project owners, and contribute Nimble or workflow fixes where needed.

#### Deliverables

- A review for each of Messaging, Storage, and Nimbus documenting current integration, findings, and recommended changes.
- Issues or PRs addressing integration gaps, with ownership for remaining follow-ups.
- CI validation results for changes made during the review.
