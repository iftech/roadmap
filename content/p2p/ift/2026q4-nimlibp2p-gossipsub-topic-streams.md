---

title: Experimental GossipSub Topic Streams
tags:
  - "2026q4"
  - "p2p"
  - "ift"
draft: false
description: Implement experimental per-topic GossipSub data streams

---

`ift-ts:p2p:ift:2026q4-nimlibp2p-gossipsub-topic-streams`

## Description

Implement the topic-stream proposal referenced in
[libp2p/specs#729](https://github.com/libp2p/specs/pull/729), separating application
data by topic and direction while retaining the ordinary GossipSub stream for
control messages. Treat this draft proposal as experimental and keep support
behind an explicit opt-in or compile flag.

## Task List

### Negotiation And Stream Lifecycle

* fully qualified name: `ift-ts:p2p:ift:2026q4-nimlibp2p-gossipsub-topic-streams:stream-lifecycle`
* owner: not assigned yet
* status: not started
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Implement capability negotiation and fallback for peers without topic-stream
support. Create, replace, and clean up streams for each topic and direction,
including subscription changes and peer disconnects.

#### Deliverables

- Experimental feature gate and legacy-peer fallback
- Topic stream creation, replacement, and cleanup
- Tests for mixed-capability peers and lifecycle transitions


### Delivery And Resource Budgets

* fully qualified name: `ift-ts:p2p:ift:2026q4-nimlibp2p-gossipsub-topic-streams:delivery-budgets`
* owner: not assigned yet
* status: not started
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Implement full-message and partial-message delivery with per-peer stream counts
and byte budgets. Verify delivery behavior and bounded resource use while
control messages continue to use the ordinary GossipSub stream.

#### Deliverables

- Full-message and partial-message delivery
- Per-peer stream and byte limits
- Tests for delivery, resource exhaustion, and control-stream behavior
- Ensure no regressions are introduced in a real life network deployment
