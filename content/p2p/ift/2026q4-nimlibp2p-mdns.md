---

title: mDNS Peer Discovery
tags:
  - "2026q4"
  - "p2p"
  - "ift"
draft: false
description: Discover local-network libp2p peers through mDNS

---

`ift-ts:p2p:ift:2026q4-nimlibp2p-mdns`

## Description

Implement mDNS discovery so libp2p peers on the same local network can find one
another without manually exchanging addresses or relying on Internet bootstrap
services. Cover discovery lifecycle, interface changes, record and address
handling, expiration, peerstore integration, and application-controlled dialing.

## Task List

### Discovery Lifecycle And Records

* fully qualified name: `ift-ts:p2p:ift:2026q4-nimlibp2p-mdns:discovery`
* owner: not assigned yet
* status: not started
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Implement discovery startup and shutdown, interface handling including network
changes, and record processing. Validate discovered addresses and expire stale
records so discovery follows the current local network.

#### Deliverables

- mDNS discovery with interface-change handling
- Record validation, address processing, and expiration
- Tests for shutdown, network changes, and stale records


### Peerstore And Connection Policy

* fully qualified name: `ift-ts:p2p:ift:2026q4-nimlibp2p-mdns:peerstore-policy`
* owner: not assigned yet
* status: not started
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Integrate discovered peers and addresses into the peerstore, following the
existing Kademlia integration pattern where applicable. Expose an overridable
connection policy so applications decide whether to dial discovered peers.

#### Deliverables

- Peerstore integration for discovered peers
- Application-controlled dialing policy and usage example


### Cross-Implementation Interoperability

* fully qualified name: `ift-ts:p2p:ift:2026q4-nimlibp2p-mdns:interop`
* owner: not assigned yet
* status: not started
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Verify local-network discovery and connection establishment with other libp2p
implementations, including address updates and record expiration.

#### Deliverables

- Reproducible cross-implementation mDNS tests
- Interoperability results for discovery, address updates, and expiration
