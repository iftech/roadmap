---

title: Early Multiplexer Negotiation
tags:
  - "2026q4"
  - "p2p"
  - "ift"
draft: false
description: Negotiate the multiplexer during the security handshake

---

`ift-ts:p2p:ift:2026q4-nimlibp2p-early-muxer-negotiation`

## Description

Reduce TCP/WebSocket connection establishment by one network round trip by
selecting the multiplexer during the security handshake. Extend the Noise
handshake payload and connection upgrader so compatible peers can avoid the
separate multistream-select exchange that follows the security handshake.

## Task List

### Handshake Negotiation And Upgrade

* fully qualified name: `ift-ts:p2p:ift:2026q4-nimlibp2p-early-muxer-negotiation:implementation`
* owner: Richard
* status: done
* start-date: 2026/10/01
* end-date: 2026/10/13

#### Description

Add multiplexer negotiation to the Noise handshake and pass the selection to
the muxed upgrader. Preserve the separate negotiation path when peers do not
support early negotiation or no early selection is available.

#### Deliverables
- [iftech/nim-libp2p#3216](https://github.com/iftech/nim-libp2p/pull/3216) feat(noise): negotiate muxers during handshake
- [iftech/nim-libp2p#3225](https://github.com/iftech/nim-libp2p/pull/3225) feat(dialer): select known protocols optimistically
- [iftech/nim-libp2p#3217](https://github.com/iftech/nim-libp2p/pull/3217) feat(multistream): add optimistic protocol selection


### Connection Setup Validation

* fully qualified name: `ift-ts:p2p:ift:2026q4-nimlibp2p-early-muxer-negotiation:validation`
* owner: not assigned yet
* status: not started
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Exercise TCP and WebSocket connections with early negotiation enabled and with
legacy peers. Verify that successful early selection removes the separate
multiplexer negotiation round trip and establishes usable streams.

#### Deliverables

- Interop coverage for early and legacy negotiation paths
- Connection traces or measurements confirming the saved round trip
