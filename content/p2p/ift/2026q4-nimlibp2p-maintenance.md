---

title: Nim-libp2p Maintenance
tags:
  - "2026q4"
  - "p2p"
  - "ift"
draft: false
description: Maintain nim-libp2p and evaluate open code review tooling

---

`ift-ts:p2p:ift:2026q4-nimlibp2p-maintenance`

Maintain nim-libp2p through improvements, bug fixes, and user support

## Description

Continue supporting and maintaining the nim-libp2p repository through ongoing improvements, refactoring, and bug fixes.
This includes a range of ad-hoc tasks critical to sustaining code quality, overall stability, correct functionality,
and performance of the project.
Additionally, it provides a platform for addressing small developer requests,
ensuring that nim-libp2p remains functional and usable for its primary users — Nimbus and Waku — helping to meet their evolving needs."


## Task List

### General Maintenance

* fully qualified name: `ift-ts:p2p:ift:2026q4-nimlibp2p-maintenance:maintenance`
* owner: Richard/Vlado/Gabe
* status: in progress (4%)
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Maintain nim-libp2p through ongoing bug fixes, improvements, and user support
as issues arise during the quarter.

#### Deliverables
- [Release v2.3.6](https://github.com/iftech/nim-libp2p/releases/tag/v2.3.6)
- [Release v2.4.0](https://github.com/iftech/nim-libp2p/releases/tag/v2.4.0)
- [logos-messaging/logos-delivery#4376](https://github.com/logos-messaging/logos-delivery/pull/4376) chore: update Python bindings submodule for HTTPS fetches
- [logos-messaging/logos-delivery-python-bindings#10](https://github.com/logos-messaging/logos-delivery-python-bindings/pull/10) fix: fetch Delivery submodule over HTTPS
- [iftech/nim-boringssl#24](https://github.com/iftech/nim-boringssl/pull/24) ci: select GCC 14 before Nim setup
- [status-im/nim-secp256k1#75](https://github.com/status-im/nim-secp256k1/pull/75) Bump version to 0.7.0.8.0 and document version numbering
- [iftech/nim-boringssl#21](https://github.com/iftech/nim-boringssl/pull/21) ci: drop Linux i386 support
- [iftech/nim-libp2p#3173](https://github.com/iftech/nim-libp2p/pull/3173) fix(pubsub): release removed timedcache entries and preserve list links
- [iftech/nim-libp2p#3149](https://github.com/iftech/nim-libp2p/pull/3149) feat(quic): expose engine configuration
- [iftech/nim-libp2p#3202](https://github.com/iftech/nim-libp2p/pull/3202) refactor(Service): remove `setup` method
- [iftech/nim-libp2p#3207](https://github.com/iftech/nim-libp2p/pull/3207) test(discovery): hardening assertion
- [iftech/nim-libp2p#3198](https://github.com/iftech/nim-libp2p/pull/3198) test: add `expectMsg` and `expectMsgContains`
- [iftech/nim-lsquic#176](https://github.com/iftech/nim-lsquic/pull/176) ci(review): fix workflow link
- [iftech/nim-libp2p#3204](https://github.com/iftech/nim-libp2p/pull/3204) fix(WsTransport): WSS without static TLS credentials now raises `TransportStartError` unless AutoTLS is configured
- [iftech/nim-libp2p#3205](https://github.com/iftech/nim-libp2p/pull/3205) chore(PeerInfo): ensure `expandAddrsLock` is initialized before using it
- [iftech/nim-libp2p#3200](https://github.com/iftech/nim-libp2p/pull/3200) fix(AddressManager): re-entrant deadlock in reachability notifications
- [iftech/nim-libp2p#3193](https://github.com/iftech/nim-libp2p/pull/3193) chore(autotls): public IP addres set when issuing cert
- [iftech/nim-libp2p#3183](https://github.com/iftech/nim-libp2p/pull/3183) fix(autotls): fail to start WS transport when cert is not ready
- [iftech/nim-libp2p#3182](https://github.com/iftech/nim-libp2p/pull/3182) fix(autotls): expiry parsing using RFC 3339
- [iftech/nim-libp2p#3181](https://github.com/iftech/nim-libp2p/pull/3181) fix(autotls): bearer reissue path
- [iftech/nim-libp2p#3186](https://github.com/iftech/nim-libp2p/pull/3186) fix(connmanager): retry watermark trims on a timer
- [iftech/nim-libp2p#3196](https://github.com/iftech/nim-libp2p/pull/3196) fix(test): make gossipsub invalid-message scoring test immune to extra heartbeats
- [iftech/nim-libp2p#3189](https://github.com/iftech/nim-libp2p/pull/3189) feat(cbind): add kad_wait_bootstrap
- [iftech/nim-libp2p#3185](https://github.com/iftech/nim-libp2p/pull/3185) fix(kad): restore liveness loop fix reverted by #3179
- [iftech/nim-libp2p#3180](https://github.com/iftech/nim-libp2p/pull/3180) fix(kad): let probed peers rotate full buckets
- [logos-co/logos-libp2p-module#111](https://github.com/logos-co/logos-libp2p-module/pull/111) chore: shrink flake.lock from 450k to 17k lines
- [iftech/roadmap#536](https://github.com/iftech/roadmap/pull/536) feat(p2p): nimbus downstream CI commitment for 2026q4

