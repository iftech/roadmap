---
title: Messaging Evaluation
tags:
  - "2026q4"
  - "dst"
  - "logos"
draft: false
description: "Test Messaging on each new version or requested feature
and look for regressions,
learn scaling properties and run scaling studies."
---

`ift-ts:dst:logos:2026q4-messaging-evaluation`

## Description
Test Messaging on each new version or requested feature
and look for regressions,
learn scaling properties and run scaling studies,
understand the limits of Messaging and its behaviour.
Deliver reports and actionable insights.
Do this monthly, reliably, with documentation of findings.

## Task list

### Regression testing (recurring)

* fully qualified name: `ift-ts:dst:logos:2026q4-messaging-evaluation:regression-testing`
* owner: Alan
* status: in progress (10%)
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description
Run different scenarios
and collect evidence and data
of Messaging's behaviour.

Test for known regressions
that have occurred in the past
and ensure they don't happen again.

#### Deliverables
- Code:
    - [iftech/10ksim#415](https://github.com/iftech/10ksim/pull/415) Full logos delivery experiment
    - [iftech/10ksim#416](https://github.com/iftech/10ksim/pull/416) Subscribe the filter clients in full logos delivery and keep them subscribed
    - [iftech/10ksim#417](https://github.com/iftech/10ksim/pull/417) Check each store node's archive in full logos delivery
    - [iftech/10ksim#411](https://github.com/iftech/10ksim/pull/411) Delivery latency per path and resources per node type for logos delivery runs
- Reports:
    - Completed a full relay, lightpush, filter, and store run for [Logos Messaging PR 4347](https://app.notion.com/p/3ea8f96fb65c812a9ae2dc71ef28860e).


### load metric

* fully qualified name: `ift-ts:dst:logos:2026q4-messaging-evaluation:load-metric`
* owner: TBD
* status: not started
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description
Include new metric (`event_loop_accumulated_lag_secs`) for load in logos-delivery experiments introduced in https://github.com/logos-messaging/logos-delivery/pull/3833

#### Deliverables
- Code:
- Reports:


### Scalable Data Sync
> *Note*: This needs more input from project
* fully qualified name: `ift-ts:dst:logos:2026q4-messaging-evaluation:scalable-data-sync`
* owner: TBD
* status: not started
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

TBD

#### Deliverables
- Code:
- Reports:


### Reliable Channel API — General Availability
> *Note*: This needs more input from project
* fully qualified name: `ift-ts:dst:logos:2026q4-messaging-evaluation:reliable-channel-api`
* owner: TBD
* status: not started
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

TBD

#### Deliverables
- Code:
- Reports:


### RLN on Logos Blockchain
> *Note*: This needs more input from project
* fully qualified name: `ift-ts:dst:logos:2026q4-messaging-evaluation:rln-logos-blockchain`
* owner: TBD
* status: not started
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

TBD

#### Deliverables
- Code:
- Reports:
