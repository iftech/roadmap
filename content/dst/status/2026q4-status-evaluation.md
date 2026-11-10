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
* status: in progress (99%)
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
    - [status-im/status-go#8036](https://github.com/status-im/status-go/issues/8036) [Epic] Optimizing messaging pipeline
    - Replaced the receiver’s sliding debounce with a fixed batch window; the first fix reduced median delivery from about 120 seconds to 17 seconds.
- Documents:
    - Identified a light-node rate-limiter timing mismatch causing valid messages to remain pending in MVDS and arrive minutes late.
    - Identified a feedback loop in which delayed processing delays acknowledgements, triggers MVDS retransmissions, and increases the processing backlog.
    - [Status delay investigation](https://discord.com/channels/1210237582470807632/1555207381355597915/1565418895873941606).
    - Measured initial p95 delivery of 31 seconds and maximum delivery of 35 seconds, down from 197 and 226 seconds; arrival-to-processing time fell from 122 seconds to 0.7 seconds.
    - Identified incoming rate-limit drops of acknowledgements and online-notification delays as causes of MVDS retries and duplicate messages.
    - Reduced median delivery from 130 seconds to 1.4 seconds, p95 from 197 seconds to 2.11 seconds, and maximum from 226 seconds to 3.45 seconds in the latest experiment.
    - Recorded no deliveries over 10 seconds in 38,000 messages, compared with 7,556 of 7,600 previously, and reduced MVDS retransmissions from thousands to zero.
    - [Status delivery latency investigation](https://discord.com/channels/1210237582470807632/1555207381355597915/1567195622635733054)

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
