---
title: Status chat protocol benchmarks
tags:
  - "2026q4"
  - "dst"
  - "status"
draft: false
description: "Realize chat protocol benchmarks
of Status."
---

`ift-ts:dst:status:2026q4-status-evaluation`

## Description

TBD

### Background

TBD

## Task list

### Reliability

* fully qualified name: `ift-ts:dst:status:2026q4-status-evaluation:reliability`
* owner: Alberto
* status: in progress (95%)
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Compare results with old status-go.

#### Deliverables
- Github PRs:
    - Rebuilt Status develop commit `6fbaa6af0ee90100c93380f3b04fdd57433cd273` as a Docker image.
    - Adapted and redeployed Status benchmark utilities in the lab.
    - [iftech/status-benchmarks#45](https://github.com/iftech/status-benchmarks/pull/45) Updates
    - [iftech/status-benchmarks#47](https://github.com/iftech/status-benchmarks/pull/47) Add plots
    - [Status analysis branch](https://github.com/status-im/status-go/tree/dst-analysis).
- Documents:
    - Identified a light-node rate-limiter timing mismatch causing valid messages to remain pending in MVDS and arrive minutes late.
    - Identified a feedback loop in which delayed processing delays acknowledgements, triggers MVDS retransmissions, and increases the processing backlog.
    - [Status delay investigation](https://discord.com/channels/1210237582470807632/1555207381355597915/1565418895873941606).

### Logos delivery integration

* fully qualified name: `ift-ts:dst:status:2026q4-status-evaluation:logos-delivery-integration`
* owner: TBD
* status: not started
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Compare results with old status-go.

#### Deliverables
- Github PRs:
- Documents:
