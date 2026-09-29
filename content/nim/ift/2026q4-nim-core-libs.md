---
title: 2026q4 Nim Core Libraries
tags:
  - "2026q4"
  - "nim"
  - "ift"
draft: false
description: Maintain Nim core libraries, integrate NimTortoise improvements, expand IDE support for IFT projects, and upgrade major projects to Nim 2.4.x.
---

`ift-ts:nim:ift:2026q4-nim-core-libs`

## Description

Maintain and document the foundational Nim libraries used by IFT teams.
Improve nimlangserver by integrating useful NimTortoise changes into mainstream nimlangserver and following the separation of protocol handling, JSON serialization, and protocol data models used by nim-web3.
Extend nimlangserver and nimsuggest support to more IFT projects, tackling one project at a time, and upgrade major IFT projects to Nim 2.4.x.

## Task List

### Documentation Improvement

* fully qualified name: `ift-ts:nim:ift:2026q4-nim-core-libs:docs-improvement`
* owner: Constantine
* status: not started
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Continue improving documentation for Nim core libraries, including missing API guidance, runnable examples, and integration notes needed by downstream teams.
Improve documentation tooling where it helps keep package documentation accurate and maintainable.

#### Deliverables

- Documentation PRs covering identified gaps and downstream usage examples.
- Documentation tooling improvements and validation of the updated examples or builds.

### Maintenance

* fully qualified name: `ift-ts:nim:ift:2026q4-nim-core-libs:maintenance`
* owner: Constantine
* status: not started
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Provide ongoing maintenance and fixes across Nim core libraries.
Triage issues, address regressions and compatibility problems, support downstream consumers, and maintain tests and CI as dependencies and toolchains evolve.

#### Deliverables

- PRs fixing library defects and maintaining compatibility, tests, and CI.
- Tracked issues and verification results for downstream integration problems.

### Nimlangserver improvements

* fully qualified name: `ift-ts:nim:ift:2026q4-nim-core-libs:nimlangserver`
* owner: TBD
* status: not started
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Use AI-assisted analysis to identify the useful improvements and fixes in NimTortoise and merge them into mainstream nimlangserver, adapting changes where needed.
Integration is blocked by Esteban's major nimlangserver rewrite; coordinate with that work before merging the selected changes.
Identify the NimTortoise repository, source commits, and upstream target branch before selecting changes; these references remain to be specified.

Use the nim-web3 approach as the model for the LSP implementation:
- Keep JSON-RPC protocol handling in `nim-json-rpc`.
- Define an LSP-specific `nim-json-ser` flavor for interpreting and emitting protocol JSON, including null values, number formatting, and missing or extra fields.
- Represent the protocol data model with Nim objects that map directly to the [LSP 3.18 specification](https://microsoft.github.io/language-server-protocol/specifications/lsp/3.18/specification/), starting with the messages and structures used by nimlangserver today.
- Make additional protocol objects straightforward to add using the same model. Generating objects from the specification is optional; the task does not require implementing every LSP feature.
- Add regression tests for imported fixes and serialization tests for the supported protocol objects and edge cases.

#### Deliverables

- An AI-assisted NimTortoise review identifying source commits, target branch, selected fixes, and deferred changes.
- PRs integrating selected NimTortoise fixes and improvements into mainstream nimlangserver after coordination with Esteban's rewrite.
- An LSP JSON serialization flavor and Nim protocol objects for the currently used messages and structures.
- Regression and serialization tests, plus guidance for adding further protocol objects.

### Nimlangserver and nimsuggest support for IFT projects

* fully qualified name: `ift-ts:nim:ift:2026q4-nim-core-libs:ift-project-ide-support`
* owner: TBD
* status: not started
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Fix nimlangserver and nimsuggest for more IFT projects.
Build on the successful focus on Constantine and nimbus-eth1: tackle one project at a time, reproduce its tooling problems, and deliver fast, visible improvements before moving to the next project.
Validate fixes against each project's real codebase and workflows.

#### Deliverables

- Issues and PRs fixing nimlangserver and nimsuggest problems in additional IFT projects.
- Regression tests and project-level validation results for the fixes.
- A record of supported projects, resolved problems, and remaining follow-ups.

### Nim 2.4.x upgrades for IFT projects

* fully qualified name: `ift-ts:nim:ift:2026q4-nim-core-libs:nim-2-4-upgrades`
* owner: TBD
* status: not started
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Upgrade major IFT projects, including Nimbus and nim-libp2p, to Nim 2.4.x.
Coordinate with project owners, resolve compatibility issues, and validate builds and tests on the supported platforms.
Aim to benefit from incremental compilation and other applicable Nimony-related improvements, verifying their availability and practical benefit in the adopted toolchain.

#### Deliverables

- PRs upgrading the selected IFT projects and their CI toolchains to Nim 2.4.x.
- Compatibility fixes and passing build and test results for each upgraded project.
- Validation of available incremental-compilation and related toolchain improvements, with adoption notes for downstream teams.
