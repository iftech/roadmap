---
title: Source Code Level QA
tags:
  - "2026q4"
  - "qa"
  - "logos"
draft: false
description: Prototype an AI code analysis system for bug discovery, independent review, precise classification, and reproducible findings.
---

`ift-ts:qa:logos:2026q4-source-code-level-qa`

## Description

Build an AI code analysis system prototype that helps discover new bugs quickly and turns findings into actionable issues.
Use a second agent to independently review candidate findings and reduce false positives, then provide precise classifications and fix proposals.
Generate proofs or exploit reproductions for high-severity issues and regression tests where possible.

## Task List

### System prototype

* fully qualified name: `ift-ts:qa:logos:2026q4-source-code-level-qa:system-prototype`
* owner: Roman
* status: in progress (75%)
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Prototype an AI code analysis workflow covering:
- Fast discovery of new bugs through agent-assisted code analysis.
- Independent cross-review by a second agent to challenge findings and reduce false positives.
- Precise issue classification, including impact, severity, affected scope, supporting code evidence, and a proposed fix. Use [LEZ issue #866](https://github.com/logos-blockchain/logos-execution-zone/issues/866) as an example of the expected reporting detail.
- Proof or exploit generation to reproduce and demonstrate high-severity findings.
- Regression test creation where possible, so confirmed bugs can be detected automatically in future changes.

#### Deliverables

- A working prototype and documentation for the discovery, cross-review, and reporting workflow.
- Classified findings with supporting evidence, second-agent review results, and fix proposals.
- Reproducible proofs or exploits for high-severity findings, with any reproduction limitations recorded.
- Regression test PRs where feasible, with remaining test coverage gaps documented.
- Ran two rounds of security and specification-compliance scanning on [LEZ Atomic Swaps](https://github.com/gateway-fm/lez-atomic-swaps), using manual prompts and the Bork prototype with structured input.
- Added configurable Claude/Codex model support to Bork.
- Sent Gateway the [LEZ Atomic Swaps v0.2.4 RFP compliance and test-coverage report](https://zealous-polka-dc7.notion.site/v0-2-4-3e58f96fb65c805d8c96d63df98f8a7a).
- Added Bork workflows `audit-spec-test-case-coverage` and `audit-milestone-test-case-coverage`.
- Sent Gateway the [LEZ Atomic Swaps v0.2.5 RFP compliance and test-coverage report](https://zealous-polka-dc7.notion.site/v0-2-5-3ed8f96fb65c804086d9ebaaacae48bc).
- Clarified and fixed CODE-5 for [LEZ Atomic Swaps v0.2.5](https://discord.com/channels/973324189794697286/1526145461025505360/1557941455362719854).
- [iftech/bork#1](https://github.com/iftech/bork/pull/1) feat: workflow files, composed audits, and the findings history
- Added third-party application support, including Notion, to the source-code QA prototype.
- Completed 21 of 53 parts of the [Logos Blockchain v0.3.0 specification audit](https://app.notion.com/p/v0-3-0-3fb8f96fb65c81b29b0af74f0c8a3de0).
- [iftech/bork#2](https://github.com/iftech/bork/pull/2) feat: cron jobs, the tick, and the triggers that keep a PR green
- [iftech/bork#3](https://github.com/iftech/bork/pull/3) feat: bork top, a full-screen view over one shared snapshot
- [iftech/bork#4](https://github.com/iftech/bork/pull/4) fix: source as a bundle, claimed briefs and collects, delivery by stage
- [iftech/bork#5](https://github.com/iftech/bork/pull/5) feat: per-session model and an effort knob
- [logos-blockchain/logos-blockchain#3911](https://github.com/logos-blockchain/logos-blockchain/issues/3911) Validation rule "ZkSignature by `public_key` over `mantle_txhash`" is never checked. (F-dd99b3f2)
- Added concurrent Bork input consoles and jobs; tested two consoles and two jobs, limited by available hardware.
