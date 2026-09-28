---

title: Experimental QUIC Encrypted ClientHello
tags:
  - "2026q4"
  - "p2p"
  - "ift"
draft: false
description: Investigate backend support and implement experimental ECH for QUIC

---

`ift-ts:p2p:ift:2026q4-nimlibp2p-quic-ech`

## Description

Investigate and implement Encrypted ClientHello for QUIC using the proposal
referenced in [libp2p/specs#730](https://github.com/libp2p/specs/pull/730).
ECH can hide the libp2p ALPN signal in the TLS handshake. Assess lsquic backend
support, configuration rotation, and retry behavior, then implement the spec
behind an experimental opt-in or compile flag.

Working on this commitment requires the spec to have been reviewed and observations
fixed as it is still on an early stage.

## Task List

### Backend Feasibility

* fully qualified name: `ift-ts:p2p:ift:2026q4-nimlibp2p-quic-ech:feasibility`
* owner: not assigned yet
* status: not started
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Evaluate ECH support in lsquic and its TLS backend. Identify binding or backend
changes needed for the proposal, including configuration distribution, rotation,
and retry handling.

#### Deliverables

- Documented backend support and implementation requirements
- Feasibility results for configuration rotation and retries


### Experimental Implementation And Validation

* fully qualified name: `ift-ts:p2p:ift:2026q4-nimlibp2p-quic-ech:implementation`
* owner: not assigned yet
* status: not started
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Implement the ECH handshake integration and required backend bindings. Validate
configuration rotation and retry behavior, and verify that an accepted ECH
handshake hides the libp2p ALPN signal in the outer ClientHello.

#### Deliverables

- Experimental ECH implementation and configuration documentation
- Handshake tests covering accepted ECH, rotation, and retry behavior
- Recorded interoperability results and any remaining backend limitations
