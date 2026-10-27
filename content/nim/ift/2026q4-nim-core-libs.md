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
* status: in progress (25%)
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Provide ongoing maintenance and fixes across Nim core libraries.
Triage issues, address regressions and compatibility problems, support downstream consumers, and maintain tests and CI as dependencies and toolchains evolve.

#### Deliverables

- PRs fixing library defects and maintaining compatibility, tests, and CI.
- Tracked issues and verification results for downstream integration problems.
- [nim-lang/Nim#26281](https://github.com/nim-lang/Nim/pull/26281) Feature: Control Nimsuggest's memory consumption cap with runtime flag
- [status-im/nim-stew#291](https://github.com/status-im/nim-stew/pull/291) `recordFields`: fix false `--styleCheck` error for a field named like its type
- [status-im/nim-stew#279](https://github.com/status-im/nim-stew/pull/279) `toHex`: faster vectorized version
- [status-im/nim-stew#281](https://github.com/status-im/nim-stew/pull/281) Fix #85; Add `validateUtf8` to `utfutils`
- [nim-lang/Nim#26443](https://github.com/nim-lang/Nim/pull/26443) Add a line about `nim book` to the `--fullhelp`.
- [nim-lang/langserver#489](https://github.com/nim-lang/langserver/pull/489) CI: Start MCP publish after GitHub Release.
- [status-im/nim-taskpools#75](https://github.com/status-im/nim-taskpools/pull/75) Fix #67; "Allow GC type task result" regression
- [status-im/nim-taskpools#76](https://github.com/status-im/nim-taskpools/pull/76) CI speed up
- [status-im/nim-taskpools#77](https://github.com/status-im/nim-taskpools/pull/77) Workaround data race in `example` thread join
- [status-im/nimbus-common-workflow#37](https://github.com/status-im/nimbus-common-workflow/pull/37) Add `nim/doc` & `nim/tools` to cache
- [status-im/nim-chronos#730](https://github.com/status-im/nim-chronos/pull/730) Fix doc examples.

### Nimlangserver improvements

* fully qualified name: `ift-ts:nim:ift:2026q4-nim-core-libs:nimlangserver`
* owner: Juan/Esteban/Constantine
* status: in progress (30%)
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
- [nim-lang/langserver#484](https://github.com/nim-lang/langserver/pull/484) Run macOS CI on Apple Silicon (macos-latest)
- [nim-lang/langserver#483](https://github.com/nim-lang/langserver/pull/483) bumps setup-nimble-action from v1 to v2
- [nim-lang/langserver#482](https://github.com/nim-lang/langserver/pull/482) Build macOS amd64 binary with an explicit x86_64 target
- [nim-lang/langserver#448](https://github.com/nim-lang/langserver/pull/448) Avoid some dangling nimsuggests
- [status-im/nim-json-rpc#300](https://github.com/status-im/nim-json-rpc/pull/300) Add `lastError` to `RpcConnection`
- [status-im/nim-json-rpc#302](https://github.com/status-im/nim-json-rpc/pull/302) Pipes transport
- [status-im/nim-json-rpc#296](https://github.com/status-im/nim-json-rpc/pull/296) Stdio transport
- [nim-lang/langserver#454](https://github.com/nim-lang/langserver/pull/454) Docs: Explain multi-entry-point project mapping
- [nim-lang/langserver#479](https://github.com/nim-lang/langserver/pull/479) Add nimsuggestMaxMemory config value to complement nimsuggest's new `--maxMemory` option.
- [nim-lang/langserver#488](https://github.com/nim-lang/langserver/pull/488) Bump to v1.16.0
- [nim-lang/langserver#473](https://github.com/nim-lang/langserver/pull/473) Transport v2
- [nim-lang/langserver#486](https://github.com/nim-lang/langserver/pull/486) Cancel nimsuggestInit on shutdown
- [nim-lang/Nim#26438](https://github.com/nim-lang/Nim/pull/26438) nimsuggest: add `outline2`, a parse-only outline
- [nim-lang/Nim#26447](https://github.com/nim-lang/Nim/pull/26447) nimsuggest: save up to 250ms for every query on +v3
- [nim-lang/langserver#491](https://github.com/nim-lang/langserver/pull/491) Disable auto chk file by default
- [nim-lang/langserver#492](https://github.com/nim-lang/langserver/pull/492) Fix progress token
- [nim-lang/langserver#490](https://github.com/nim-lang/langserver/pull/490) Use nimsuggest `outline2` when possible
- [nim-lang/langserver#487](https://github.com/nim-lang/langserver/pull/487) Remove process monitor
- [nim-lang/langserver#496](https://github.com/nim-lang/langserver/pull/496) Check project after external edit
- [nim-lang/langserver#495](https://github.com/nim-lang/langserver/pull/495) Fix restart nimsuggest on configuration changes
- [nim-lang/langserver#494](https://github.com/nim-lang/langserver/pull/494) Await workspace configuration
- [nim-lang/langserver#493](https://github.com/nim-lang/langserver/pull/493) Avoid showing chk file result for an old file edit

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

### Nim lint

* fully qualified name: `ift-ts:nim:ift:2026q4-nim-core-libs:nim-lint`
* owner: Constantine
* status: in progress (25%)
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Develop a Nim static-analysis linter with a unified API for pluggable, configurable rules that enforce coding conventions and best practices beyond `nim check` and formatting.
Provide initial rules for IFT projects, such as flagging `asyncSpawn`, with severity levels and inline ignores; support community rules and CI/PR reporting.

#### Deliverables
- Linter engine, initial rules, and documentation for adding rules and integrating checks into CI.
- Wrote the second nim-lint specification after feedback on the first prototype.
