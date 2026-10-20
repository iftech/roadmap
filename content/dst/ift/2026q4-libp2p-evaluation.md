---
title: Libp2p Evaluation
tags:
  - "2026q4"
  - "dst"
  - "ift"
draft: false
description: "Test libp2p on each new version or feature
and look for regressions,
learn scaling properties and run scaling studies."
---

`ift-ts:dst:ift:2026q4-libp2p-evaluation`


## Description

Test libp2p on each new version or requested feature
and look for regressions,
learn scaling properties and run scaling studies,
understand the limits of Waku and its behaviour.
Deliver reports and actionable insights.
Do this monthly, reliably, with documentation of findings.

The scope of this commitment depends on the P2P team
work and improvements, and it is subjected to change.

## Task list

### Regression testing (recurring)

* fully qualified name: `ift-ts:dst:ift:2026q4-libp2p-evaluation:regression-testing`
* owner: Alan
* status: in progress (25%)
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description
Run different scenarios
and collect evidence and data
of libp2p's behaviour.

Test for known regressions
that have occurred in the past
and ensure they don't happen again.

#### Deliverables

- Code:
    - [iftech/10ksim#418](https://github.com/iftech/10ksim/pull/418) Connection cap and bootstrap image options for the nim-libp2p nodes
    - [iftech/10ksim#419](https://github.com/iftech/10ksim/pull/419) Partition analysis: phases from each message's publish record
- Reports:
    - Tested Kademlia liveness-loop and bucket-rotation changes and updated the [nim-libp2p v2.4.0 regression report](https://app.notion.com/p/3dd8f96fb65c81c194b8ce51ea753a52).
- Other:
    - Confirmed with a controlled rerun that the lower publish rate explains the v2.3.0 bandwidth gap; ran four v2.4.0 repeats to measure variation.


### Interop at scale

* fully qualified name: `ift-ts:dst:ift:2026q4-libp2p-evaluation:interop-at-scale`
* owner: TBD
* status: not started
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description
Run different scenarios
and collect evidence and data
of libp2p's behaviour using 
different implementations.


#### Deliverables
- Code:
- Reports:


### Automatic reporting

* fully qualified name: `ift-ts:dst:ift:2026q4-libp2p-evaluation:automatic-reporting`
* owner: Alan
* status: in progress (60%)
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description
Make use of the main tools available in the main repository to perform automatic analysis and reporting for
libp2p team, either by commit, each X amount of time or triggered manually.


#### Deliverables
- Code:
    - [iftech/10ksim#443](https://github.com/iftech/10ksim/pull/443) Run nodes from any image, triggered manually from GitHub
    - [iftech/10ksim#445](https://github.com/iftech/10ksim/pull/445) run-nodes: self-terminating groups, node failures as results
    - [iftech/10ksim#446](https://github.com/iftech/10ksim/pull/446) run-nodes: allow count 0 to skip a group
- Reports:
