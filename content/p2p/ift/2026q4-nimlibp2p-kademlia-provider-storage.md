---

title: Kademlia Provider Storage
tags:
  - "2026q4"
  - "p2p"
  - "ift"
draft: false
description: Allow applications to replace Kademlia record storage

---

`ift-ts:p2p:ift:2026q4-nimlibp2p-kademlia-provider-storage`

## Description

Value records, provider records, and locally provided keys use concrete
in-memory structures. Introduce a replaceable storage interface so downstream
applications can supply their own storage mechanism, including key/value
operations, expiration, and iteration.

## Task List

### Storage Interface

* fully qualified name: `ift-ts:p2p:ift:2026q4-nimlibp2p-kademlia-provider-storage:interface`
* owner: not assigned yet
* status: not started
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Define the operations required by value records, provider records, and locally
provided keys. Specify key/value access, deletion, expiration/TTL, and iteration
semantics, adding other operations only where existing DHT behavior requires them.

#### Deliverables

- Storage interface covering all three record categories
- Documented expiration and iteration semantics


### Integration And Backend Validation

* fully qualified name: `ift-ts:p2p:ift:2026q4-nimlibp2p-kademlia-provider-storage:integration`
* owner: not assigned yet
* status: not started
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Route Kademlia storage access through the interface and preserve an in-memory
backend. Demonstrate application-supplied storage and verify record lookup,
expiration, and locally provided key iteration across backends.

#### Deliverables

- Replaceable storage integrated into Kademlia
- In-memory backend preserving existing behavior
- Example custom backend and storage contract tests
