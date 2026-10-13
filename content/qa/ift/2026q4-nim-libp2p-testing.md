---
title: Nim Libp2p Testing
tags:
  - "2026q4"
  - "qa"
  - "ift"
draft: false
description: Add dial ranking and backoff coverage and maintain nim-libp2p test reliability.
---

`ift-ts:qa:ift:2026q4-nim-libp2p-testing`

## Description

Continue nim-libp2p QA with coverage for opt-in dial ranking and backoffs carried over from Q3.
Maintain existing tests as the library evolves and investigate regressions and flaky scenarios.

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
