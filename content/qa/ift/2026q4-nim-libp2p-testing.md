---
title: Nim Libp2p Testing
tags:
  - "2026q4"
  - "qa"
  - "ift"
draft: false
description: Validate new nim-libp2p protocol features, assess Logos module coverage, move reusable interop tests to unified-testing, and maintain test reliability.
---

`ift-ts:qa:ift:2026q4-nim-libp2p-testing`

## Description

Continue nim-libp2p QA with coverage for opt-in dial ranking and backoffs carried over from Q3.
Maintain existing tests as the library evolves and investigate regressions and flaky scenarios.
Cover the protocol features below and move reusable interoperability tests into unified-testing.

## Task List

### Opt-in Dial Ranking and Backoffs Testing

* fully qualified name: `ift-ts:qa:ift:2026q4-nim-libp2p-testing:opt-in-dial-ranking-and-backoffs`
* owner: radek
* status: not started
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Implement tests for opt-in dial ranking and backoff behavior.
Cover address and transport preference, concurrent dial cancellation, failed-address backoffs, and compatibility when the feature is disabled, in coordination with the P2P team.

#### Deliverables

- PRs adding unit and integration tests for dial ranking and backoffs.
- Tracked defects and coverage gaps found during validation.

### Maintenance

* fully qualified name: `ift-ts:qa:ift:2026q4-nim-libp2p-testing:maintenance`
* owner: Radek
* status: in progress (25%)
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Provide ongoing QA maintenance for nim-libp2p, including regression fixes, flaky-test investigation, and test updates required by upstream changes.
Handle issue-driven validation that does not require a separate feature-specific task.

#### Deliverables
- [iftech/nim-libp2p#3237](https://github.com/iftech/nim-libp2p/issues/3237) gossipsub: no IHAVE for a subscribed topic once PRUNE empties its mesh
- [iftech/nim-libp2p#3236](https://github.com/iftech/nim-libp2p/issues/3236) gossipsub: a peer that restarts within pruneBackoff is penalised for its GRAFT and kept out of the mesh
- [iftech/nim-libp2p#3238](https://github.com/iftech/nim-libp2p/pull/3238) test: bug reproductions for #3236 and #3237

### GossipSub Topic Streams

* fully qualified name: `ift-ts:qa:ift:2026q4-nim-libp2p-testing:gossipsub-topic-streams`
* owner: Radek
* status: not started
* start-date: 2026/11/03
* end-date: 2026/12/31

#### Description

Test GossipSub topic streams ([stack 3274](https://github.com/iftech/nim-libp2p/stack/3274)).

#### Deliverables

- PRs adding topic-stream tests.

### GossipSub Byte Queues

* fully qualified name: `ift-ts:qa:ift:2026q4-nim-libp2p-testing:gossipsub-byte-queues`
* owner: Radek
* status: not started
* start-date: 2026/11/03
* end-date: 2026/12/31

#### Description

Test GossipSub byte queues and queue limits ([PR 3255](https://github.com/iftech/nim-libp2p/pull/3255)).

#### Deliverables

- PRs adding byte-queue tests.

### Waggle

* fully qualified name: `ift-ts:qa:ift:2026q4-nim-libp2p-testing:waggle`
* owner: Radek
* status: not started
* start-date: 2026/11/03
* end-date: 2026/12/31

#### Description

Test Waggle protocol behavior and interoperability ([stack 3352](https://github.com/iftech/nim-libp2p/stack/3352)).

#### Deliverables

- PRs adding Waggle tests.

### Early Negotiation and Optimistic Protocol Selection

* fully qualified name: `ift-ts:qa:ift:2026q4-nim-libp2p-testing:early-negotiation-and-optimistic-selection`
* owner: Radek
* status: not started
* start-date: 2026/11/03
* end-date: 2026/12/31

#### Description

Test early negotiation and optimistic protocol selection ([PR 3216](https://github.com/iftech/nim-libp2p/pull/3216), [PR 3225](https://github.com/iftech/nim-libp2p/pull/3225)).

#### Deliverables

- PRs adding negotiation and protocol-selection tests.

### Logos Libp2p Module Coverage Assessment

* fully qualified name: `ift-ts:qa:ift:2026q4-nim-libp2p-testing:logos-libp2p-module-coverage`
* owner: Radek
* status: not started
* start-date: 2026/11/03
* end-date: 2026/12/31

#### Description

Identify missing test coverage in [logos-libp2p-module](https://github.com/logos-co/logos-libp2p-module).

#### Deliverables

- A coverage-gap report and follow-up issues.

### Unified Testing Migration

* fully qualified name: `ift-ts:qa:ift:2026q4-nim-libp2p-testing:unified-testing-migration`
* owner: Radek
* status: not started
* start-date: 2026/11/03
* end-date: 2026/12/31

#### Description

Move reusable test code from test-plans into unified-testing.

#### Deliverables

- PRs migrating tests and updating CI references.

### Focused Unit and In-Memory Test Refactoring

* fully qualified name: `ift-ts:qa:ift:2026q4-nim-libp2p-testing:focused-test-refactoring`
* owner: Radek
* status: not started
* start-date: 2026/11/03
* end-date: 2026/12/31

#### Description

Replace unnecessary network setup with unit or in-memory tests ([issue 3326](https://github.com/iftech/nim-libp2p/issues/3326)).

#### Deliverables

- PRs simplifying tests while preserving coverage.
