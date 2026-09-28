---

title: GossipSub Duplicate Suppression Validation
tags:
  - "2026q4"
  - "p2p"
  - "ift"
draft: false
description: Validate GossipSub duplicate suppression on Nimbus mainnet nodes

---

`ift-ts:p2p:ift:2026q4-nimlibp2p-gossipsub-duplicate-suppression`

## Description

Test [nim-libp2p#3043](https://github.com/vacp2p/nim-libp2p/pull/3043),
[nim-libp2p#3016](https://github.com/vacp2p/nim-libp2p/pull/3016) and 
[nim-libp2p#3165](https://github.com/vacp2p/nim-libp2p/pull/3165) against their
original requirements. Use Nimbus libp2p nodes on mainnet to establish that the
behavior is desirable and stable over time. Local testnets alone are insufficient
to assess Internet conditions, memory leaks, or isolated mesh islands.

## Task List

### Requirements And Regression Coverage

* fully qualified name: `ift-ts:p2p:ift:2026q4-nimlibp2p-gossipsub-duplicate-suppression:regression-coverage`
* owner: not assigned yet
* status: not started
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Translate the requirements behind both changes into checks for duplicate
suppression and message delivery. Establish a baseline for comparison during
mainnet monitoring.

#### Deliverables

- Requirement-to-test mapping for both PRs
- Regression coverage and baseline measurements


### Sustained Mainnet Validation

* fully qualified name: `ift-ts:p2p:ift:2026q4-nimlibp2p-gossipsub-duplicate-suppression:mainnet-validation`
* owner: not assigned yet
* status: not started
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Run the changes on Nimbus fleet and/or home nodes on mainnet and monitor them
over an extended period. Compare resource use, message delivery, and mesh
connectivity against the baseline, checking for leaks, isolated islands, and
other unexpected peer-to-peer behavior.

#### Deliverables

- Mainnet monitoring results covering stability and resource use over time
- Evidence that duplicate suppression meets its requirements without delivery or mesh regressions
- Documented findings and fixes for regressions discovered during monitoring
