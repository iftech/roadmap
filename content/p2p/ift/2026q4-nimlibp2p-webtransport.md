---

title: nim-libp2p WebTransport
tags:
  - "2026q4"
  - "p2p"
  - "ift"
draft: false
description: Accept browser libp2p connections through a native Nim WebTransport endpoint

---

`ift-ts:p2p:ift:2026q4-nimlibp2p-webtransport`

## Description

Build a native Nim WebTransport endpoint using nim-lsquic so browser libp2p
clients can connect to nim-libp2p. Expand the HTTP/3 and session integration
needed for this server endpoint and verify browser interoperability.

## Task List

### nim-lsquic Endpoint Support

* fully qualified name: `ift-ts:p2p:ift:2026q4-nimlibp2p-webtransport:endpoint`
* owner: not assigned yet
* status: not started
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Extend the nim-lsquic bindings and HTTP/3 integration needed to accept
WebTransport sessions. Implement session establishment, stream events, and
cleanup for rejected or closed sessions.

#### Deliverables

- Native WebTransport session acceptance through nim-lsquic
- Tests for session establishment, rejection, and cleanup


### libp2p Transport Integration

* fully qualified name: `ift-ts:p2p:ift:2026q4-nimlibp2p-webtransport:transport`
* owner: not assigned yet
* status: not started
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Expose accepted WebTransport sessions through nim-libp2p connection and stream
abstractions. Handle endpoint addressing, peer authentication, and connection
shutdown so browser clients can use libp2p protocols over the transport.

#### Deliverables

- WebTransport endpoint integrated with nim-libp2p
- Documented endpoint and browser connection configuration


### Browser Interoperability

* fully qualified name: `ift-ts:p2p:ift:2026q4-nimlibp2p-webtransport:interop`
* owner: not assigned yet
* status: not started
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Connect browser libp2p clients to the native Nim endpoint and exercise
bidirectional protocol traffic, disconnects, and reconnects.

#### Deliverables

- Reproducible browser-to-Nim interoperability tests
- Example browser connection and results covering stream and session lifecycle
