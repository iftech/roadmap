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
* status: in progress (20%)
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
- [status-im/nimbus-eth2#9240](https://github.com/status-im/nimbus-eth2/pull/9240) chore: bump nim-lsquic
- [iftech/nim-libp2p#3229](https://github.com/iftech/nim-libp2p/pull/3229) fix(mplex): await reset writes during channel cleanup
- [iftech/nim-lsquic#178](https://github.com/iftech/nim-lsquic/pull/178) chore(lsquic): update vendored dependency
- [iftech/nim-lsquic#179](https://github.com/iftech/nim-lsquic/pull/179) test(lsquic): cover client address migration
- [logos-co/logos-libp2p-module#120](https://github.com/logos-co/logos-libp2p-module/pull/120) fix: bump nim-libp2p for duplicate DNS responses
- [iftech/nim-libp2p#3224](https://github.com/iftech/nim-libp2p/pull/3224) fix(nameresolving): tolerate duplicate DNS responses
- [status-im/nimbus-eth2#9204](https://github.com/status-im/nimbus-eth2/pull/9204) chore: bump nim-lsquic
- [iftech/nim-boringssl#20](https://github.com/iftech/nim-boringssl/pull/20) ci: check generated BoringSSL bindings before merging
- [iftech/nim-libp2p#3223](https://github.com/iftech/nim-libp2p/pull/3223) test: reduce timeouts
- [iftech/nim-libp2p#3222](https://github.com/iftech/nim-libp2p/pull/3222) chore(autotls): propagate cert load  error
- [iftech/nim-libp2p#3214](https://github.com/iftech/nim-libp2p/pull/3214) test: hardening assertion
- [iftech/nim-libp2p#3209](https://github.com/iftech/nim-libp2p/pull/3209) test: add suite timeout
- [iftech/nim-libp2p#3241](https://github.com/iftech/nim-libp2p/pull/3241) test(dialer): improve cancellation test
- [iftech/nim-libp2p#3239](https://github.com/iftech/nim-libp2p/pull/3239) chore(builders): return error result insted of Defect
- [iftech/nim-libp2p#3232](https://github.com/iftech/nim-libp2p/pull/3232) feat(autotls): certificate renewal propagation
- [iftech/nim-libp2p#3234](https://github.com/iftech/nim-libp2p/pull/3234) fix(autotls): using PEM leaf certificate’s X.509 notAfter for expiry time
- [iftech/nim-libp2p#3249](https://github.com/iftech/nim-libp2p/pull/3249) fix(kad): close inbound RPC streams on shutdown
- [iftech/nim-libp2p#3244](https://github.com/iftech/nim-libp2p/pull/3244) ci: bump workflow timeout
- [iftech/nim-libp2p#3240](https://github.com/iftech/nim-libp2p/pull/3240) fix: mapper-removal races in PeerInfo and AddressManager
- [iftech/nim-libp2p#3242](https://github.com/iftech/nim-libp2p/pull/3242) chore(Switch): adds convenience overloads
- [iftech/lsquic#3](https://github.com/iftech/lsquic/pull/3) fix(conn): send keepalive PINGs when no stream is open - #2
- [iftech/nim-lsquic#181](https://github.com/iftech/nim-lsquic/pull/181) fix: keep QUIC connections without streams alive
- [iftech/nim-libp2p#3245](https://github.com/iftech/nim-libp2p/pull/3245) fix(upgrade): export chronicles from muxedupgrade
- [iftech/nim-libp2p#3212](https://github.com/iftech/nim-libp2p/pull/3212) chore(dial): benchmark dial time against stalled addresses
- [iftech/nim-libp2p#3228](https://github.com/iftech/nim-libp2p/pull/3228) test(transports): cancel tests for upgrade, memory and tor
- [iftech/nim-libp2p#3230](https://github.com/iftech/nim-libp2p/pull/3230) test(crypto): malformed DER for minasn1, ecnist and rsa
- [iftech/nim-libp2p#3227](https://github.com/iftech/nim-libp2p/pull/3227) test(multiformat): cover decode error paths
- [iftech/nim-libp2p#3226](https://github.com/iftech/nim-libp2p/pull/3226) test: malformed protobuf and key protobuf decoding
- [iftech/nim-libp2p#3211](https://github.com/iftech/nim-libp2p/pull/3211) chore(metrics): dial race and backoff metrics
- [iftech/nim-libp2p#3210](https://github.com/iftech/nim-libp2p/pull/3210) chore(rsa): delete uncompilable hex-string `init`
- [iftech/nim-libp2p#3201](https://github.com/iftech/nim-libp2p/pull/3201) feat(service-disco): advertise caller-supplied XPRs, not the node's own record
- [iftech/nim-lsquic#183](https://github.com/iftech/nim-lsquic/pull/183) fix(endpoint): normalize mapped IPv4 peers when draining UDP
- [iftech/nim-lsquic#182](https://github.com/iftech/nim-lsquic/pull/182) chore: bump version from 0.11.0 to 0.11.1
- [iftech/nim-libp2p#3265](https://github.com/iftech/nim-libp2p/pull/3265) chore(quic): bump nim-lsquic to v0.11.2
- [status-im/nimbus-eth2#9283](https://github.com/status-im/nimbus-eth2/pull/9283) chore: bump nim-lsquic
- [iftech/nim-libp2p#3260](https://github.com/iftech/nim-libp2p/pull/3260) test: consolidate redundant unit test fixtures
- [iftech/nim-libp2p#3261](https://github.com/iftech/nim-libp2p/pull/3261) chore(ci): remove Codecov integration
- [iftech/nim-lsquic#184](https://github.com/iftech/nim-lsquic/pull/184) ci: review workflow update
- [iftech/nim-libp2p#3277](https://github.com/iftech/nim-libp2p/pull/3277) chore: fix broken links
- [iftech/nim-libp2p#3266](https://github.com/iftech/nim-libp2p/pull/3266) chore: remove minprotobuf
- [iftech/nim-libp2p#3264](https://github.com/iftech/nim-libp2p/pull/3264) test: bump timeout for gossipsub heartbeat component test
- [iftech/nim-libp2p#3043](https://github.com/iftech/nim-libp2p/pull/3043) fix(gossipsub): track in-flight IWANT requests
- [iftech/nim-libp2p#3016](https://github.com/iftech/nim-libp2p/pull/3016) fix(gossipsub): cancel a queued relay when the peer already has the message
- [iftech/nim-libp2p#3213](https://github.com/iftech/nim-libp2p/pull/3213) fix(pubsub): record PRUNE backoff outside the mesh and for backoff 0
- [iftech/nim-libp2p#3231](https://github.com/iftech/nim-libp2p/pull/3231) test: fault-stream helper for kad and service discovery error paths
- [iftech/nim-lsquic#180](https://github.com/iftech/nim-lsquic/pull/180) fix(engine): disable the lsquic no-progress timeout by default
- [iftech/nim-libp2p#3243](https://github.com/iftech/nim-libp2p/pull/3243) fix(multistream): allow reads after half-close on optimistic streams
- [iftech/nim-libp2p#3258](https://github.com/iftech/nim-libp2p/pull/3258) fix(service-discovery): no .get() on an optional ticket wait
- [iftech/nim-libp2p#3257](https://github.com/iftech/nim-libp2p/pull/3257) fix(crypto): reject an empty EC public key
- [iftech/nim-libp2p#3281](https://github.com/iftech/nim-libp2p/pull/3281) fix(kad): narrow getProviders raises to CancelledError
- [iftech/nim-libp2p#3263](https://github.com/iftech/nim-libp2p/pull/3263) fix(identify): send the configured proto version
- [iftech/nim-libp2p#3165](https://github.com/iftech/nim-libp2p/pull/3165) fix(pubsub): retry a failed send stream open
- [iftech/nim-libp2p#3282](https://github.com/iftech/nim-libp2p/pull/3282) chore(kad): return LPResult from ping
- [iftech/nim-libp2p#3285](https://github.com/iftech/nim-libp2p/pull/3285) chore(result): const error causes
- [iftech/nim-libp2p#3286](https://github.com/iftech/nim-libp2p/pull/3286) chore(result): TLS certificate parse returns Result
- [iftech/roadmap#542](https://github.com/iftech/roadmap/pull/542) fix(p2p): Result PR list, end-date and nim-libp2p repo links
- [iftech/nim-libp2p#3251](https://github.com/iftech/nim-libp2p/pull/3251) chore(results): one shape for every err call site
