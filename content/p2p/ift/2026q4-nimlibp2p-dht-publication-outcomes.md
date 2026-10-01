---

title: Explicit DHT Publication Outcomes
tags:
  - "2026q4"
  - "p2p"
  - "ift"
draft: false
description: Expose local storage and remote publication results from putValue

---

`ift-ts:p2p:ift:2026q4-nimlibp2p-dht-publication-outcomes`

## Description

Make putValue results distinguish local storage from remote publication.
Aggregate remote write acknowledgements so callers can identify successful
peers, quorum failures, and partial or complete success. A mismatching
acknowledgement must be reflected in the result rather than only logged.

## Task List

### Publication Result Model

* fully qualified name: `ift-ts:p2p:ift:2026q4-nimlibp2p-dht-publication-outcomes:result-model`
* owner: not assigned yet
* status: not started
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Define results that expose whether local storage succeeded, whether publication
was attempted, which peers acknowledged the record, and whether the requested
quorum was met. Specify partial success and complete failure semantics.

#### Deliverables

- Documented publication result types and quorum semantics
- Caller-visible local storage, publication, and successful-peer information


### Acknowledgement Aggregation And Tests

* fully qualified name: `ift-ts:p2p:ift:2026q4-nimlibp2p-dht-publication-outcomes:aggregation`
* owner: not assigned yet
* status: not started
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Aggregate remote write outcomes into the final putValue result. Treat mismatching
acknowledgements as unsuccessful writes and cover local failures, no publication,
partial acknowledgements, quorum failure, and complete success.

#### Deliverables

- putValue implementation reporting aggregate publication outcomes
- Tests for mismatching acknowledgements and each result category
- Usage examples showing how callers interpret results
