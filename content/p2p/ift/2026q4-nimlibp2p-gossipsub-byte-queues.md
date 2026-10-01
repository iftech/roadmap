---

title: Byte-Aware GossipSub Queues
tags:
  - "2026q4"
  - "p2p"
  - "ift"
draft: false
description: Bound GossipSub queued bytes as well as message counts

---

`ift-ts:p2p:ift:2026q4-nimlibp2p-gossipsub-byte-queues`

## Description

Queue-length limits already exist, but equal message counts can retain very
different amounts of memory. Add byte limits alongside count limits to bound
queued GossipSub data when message sizes vary.

## Task List

### Byte Accounting And Limits

* fully qualified name: `ift-ts:p2p:ift:2026q4-nimlibp2p-gossipsub-byte-queues:byte-limits`
* owner: not assigned yet
* status: not started
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Track retained bytes through enqueue, dequeue, drop, and cleanup. Enforce byte
budgets alongside existing count limits while preserving the intended overflow
behavior of each queue priority.

#### Deliverables

- Byte accounting and configurable byte limits for GossipSub queues
- Defined overflow behavior when either count or byte limits are reached


### Queue Pressure Validation

* fully qualified name: `ift-ts:p2p:ift:2026q4-nimlibp2p-gossipsub-byte-queues:validation`
* owner: not assigned yet
* status: not started
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Exercise mixed message sizes, large bursts, and slow peers. Verify that queue
cleanup releases accounted bytes and existing priority behavior remains correct.

#### Deliverables

- Tests for mixed-size traffic and count/byte boundary conditions
- Resource-use measurements under queue pressure
- Real life network tests ensuring no regressions are introduced