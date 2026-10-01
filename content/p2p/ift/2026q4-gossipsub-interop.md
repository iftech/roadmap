---

title: GossipSub Interoperability Framework
tags:
  - "2026q4"
  - "p2p"
  - "ift"
draft: false
description: Expand continuous GossipSub interoperability testing across implementations

---

`ift-ts:p2p:ift:2026q4-gossipsub-interop`

## Description

Evolve the existing GossipSub test plan into a reusable unified-testing
framework, using [libp2p/test-plans#850](https://github.com/libp2p/test-plans/pull/850)
as a starting point. Cover Go, Rust, JS, Python, Nim, Zig, and future
implementations in mixed-language topologies across TCP, WebSocket, and native
QUIC. Use unified-testing for protocol and transport debugging.

Note that large-scale Shadow simulation seems to not work correctly with QUIC

## Task List

### Implementation And Transport Matrix

* fully qualified name: `ift-ts:p2p:ift:2026q4-gossipsub-interop:matrix`
* owner: not assigned yet
* status: not started
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Build an extensible test matrix that runs mixed-language topologies and
automatically exercises transport combinations. Ensure the framework can be
used continuously by maintainers across implementations.

#### Deliverables

- Mixed-language GossipSub scenarios across the listed implementations
- Automated TCP, WebSocket, and native QUIC combinations where supported
- Documented workflow for adding implementations and running tests


### Protocol Stability And Fault Injection

* fully qualified name: `ift-ts:p2p:ift:2026q4-gossipsub-interop:stability`
* owner: not assigned yet
* status: not started
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Validate scoring, mesh maintenance, IHAVE/IWANT behavior, duplicate suppression,
and consistent propagation. Run long-lived scenarios with joins, leaves,
disconnects, reconnects, and churn, plus delayed peers, partitions, intermittent
connectivity, and reconnect storms.

#### Deliverables

- Protocol behavior assertions across implementations
- Long-running mesh stability and fault-injection scenarios
- Reproducible failure reports for interoperability regressions


### Metrics And Dashboard

* fully qualified name: `ift-ts:p2p:ift:2026q4-gossipsub-interop:reporting`
* owner: not assigned yet
* status: not started
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Collect propagation latency, throughput, duplicate rate, and bandwidth use.
Present standardized results so maintainers can compare releases and identify
interoperability regressions.

#### Deliverables

- Comparable performance metrics from framework runs
- Standardized dashboard with release comparisons and regression visibility
