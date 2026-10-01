---

title: Experimental QUIC Datagrams
tags:
  - "2026q4"
  - "p2p"
  - "ift"
draft: false
description: Add negotiated application datagrams over QUIC

---

`ift-ts:p2p:ift:2026q4-nimlibp2p-quic-datagrams`

## Description

Implement negotiated application datagrams using QUIC unreliable delivery,
following the draft proposal referenced in
[libp2p/specs#680](https://github.com/libp2p/specs/pull/680). This supports transient
presence, live state, or telemetry where retransmitting obsolete data is
undesirable. Keep the feature experimental behind an opt-in or compile flag.

## Task List

### Negotiation And Datagram API

* fully qualified name: `ift-ts:p2p:ift:2026q4-nimlibp2p-quic-datagrams:implementation`
* owner: not assigned yet
* status: not started
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Implement capability negotiation and application send/receive support through
nim-lsquic and nim-libp2p. Define unsupported-peer behavior and expose the
unreliable delivery semantics to callers.

#### Deliverables

- Experimental negotiated QUIC datagram support
- Documented application API and unsupported-peer behavior


### Datagram Validation

* fully qualified name: `ift-ts:p2p:ift:2026q4-nimlibp2p-quic-datagrams:validation`
* owner: not assigned yet
* status: not started
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Verify datagram exchange, negotiated size limits, loss behavior, and connection
cleanup. Check that datagram use can coexist with reliable streams.

#### Deliverables

- Tests for negotiation, datagram delivery, limits, and cleanup
- Example demonstrating transient application data alongside reliable streams
