---

title: Reachability And Relay Lifecycle Integration
tags:
  - "2026q4"
  - "p2p"
  - "ift"
draft: false
description: Integrate AutoNAT v2 with hole punching and correct relay lifecycle behavior

---

`ift-ts:p2p:ift:2026q4-nimlibp2p-reachability-relay-lifecycle`

## Description

Complete reachability integration so hole punching can use AutoNAT v2 instead
of remaining coupled to AutoNAT v1. Address relay reservation tasks surviving
stop/restart, stale relay addresses, and service advertisements retaining old
addresses.

## Task List

### AutoNAT v2 Hole-Punching Integration

* fully qualified name: `ift-ts:p2p:ift:2026q4-nimlibp2p-reachability-relay-lifecycle:autonat-v2`
* owner: not assigned yet
* status: not started
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Connect hole-punching decisions to AutoNAT v2 reachability information and
validate behavior as reachability changes.

#### Deliverables

- Hole-punching integration with AutoNAT v2
- Tests for reachable, unreachable, and changing reachability states


### Relay And Advertisement Cleanup

* fully qualified name: `ift-ts:p2p:ift:2026q4-nimlibp2p-reachability-relay-lifecycle:lifecycle`
* owner: not assigned yet
* status: not started
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Ensure relay reservation tasks stop with their service and do not survive or
duplicate across restarts. Remove stale relay addresses and refresh service
advertisements when advertised addresses change.

#### Deliverables

- Correct reservation task cancellation and restart behavior
- Relay addresses and service advertisements reflecting current addresses
- Regression tests for stop/restart, reservation loss, and address changes
