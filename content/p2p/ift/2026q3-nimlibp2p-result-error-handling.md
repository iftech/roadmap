---

title: nim-libp2p Result Error Handling
tags:
  - "2026q3"
  - "p2p"
  - "ift"
draft: false
description: Replace expected exception paths with Result based errors

---

`ift-ts:p2p:ift:2026q3-nimlibp2p-result-error-handling`

Audit code paths that use exceptions for expected failures and replace them
with explicit `Result[T, error]` handling where practical.

## Description

Exceptions should remain available for cancellation and genuinely exceptional
conditions, but expected runtime failures are easier to reason about when they
are returned explicitly. This commitment moves selected nim-libp2p paths toward
`Result[T, error]` while preserving compatibility and avoiding broad churn.

## Task List

### Result Conversion

* fully qualified name: `ift-ts:p2p:ift:2026q3-nimlibp2p-result-error-handling:result-conversion`
* owner: Gabe
* status: done
* start-date: 2026/07/15
* end-date: 2026/10/15

#### Description
Convert to `Result[T, error]` wherever exceptions are used for expected failures, prioritizing
transport setup, address parsing, peer info parsing, protocol negotiation, Kademlia, discovery, 
and builder configuration. Keep `CancelledError` and other cancellation semantics intact.
Prefer to keep the public API unchanged if possible.

#### Deliverables
- Selected APIs return explicit result values for expected failures
- Error types preserve useful context and messages
- Existing callers updated to handle result values
- Tests cover success and expected failure paths
- Migration notes for changed APIs
- [iftech/nim-libp2p#3084](https://github.com/iftech/nim-libp2p/pull/3084) chore(errors): valueOrRaise and onErrorRaise helpers
- [iftech/nim-libp2p#3123](https://github.com/iftech/nim-libp2p/pull/3123) chore(result): multistream negotiation and PeerInfo.init return Result
- [iftech/nim-libp2p#3137](https://github.com/iftech/nim-libp2p/pull/3137) chore(result): tcp and tor transports return Result internally
- [iftech/nim-libp2p#3136](https://github.com/iftech/nim-libp2p/pull/3136) chore(result): upgrade managers and dialer return Result
- [iftech/nim-libp2p#3143](https://github.com/iftech/nim-libp2p/pull/3143) chore(result): quic transport
- [iftech/nim-libp2p#3142](https://github.com/iftech/nim-libp2p/pull/3142) chore(result): wstransport
- [iftech/nim-libp2p#3144](https://github.com/iftech/nim-libp2p/pull/3144) chore(result): connectivity clients
- [iftech/nim-libp2p#3160](https://github.com/iftech/nim-libp2p/pull/3160) chore(result): PeerIDAuth client
- [iftech/nim-libp2p#3157](https://github.com/iftech/nim-libp2p/pull/3157) chore(result): relay client and transport
- [iftech/nim-libp2p#3159](https://github.com/iftech/nim-libp2p/pull/3159) chore(result): rendezvous
- [iftech/nim-libp2p#3162](https://github.com/iftech/nim-libp2p/pull/3162) chore(result): AutoTLS service, JWS and utils
- [iftech/nim-libp2p#3163](https://github.com/iftech/nim-libp2p/pull/3163) chore(result): AutoTLS ACME API
- [iftech/nim-libp2p#3176](https://github.com/iftech/nim-libp2p/pull/3176) chore(result): dialer connect path and ConnManager store return Result
- [iftech/nim-libp2p#3177](https://github.com/iftech/nim-libp2p/pull/3177) chore(result): NATService, switch mount and builders
- [iftech/nim-libp2p#3179](https://github.com/iftech/nim-libp2p/pull/3179) chore(result): add LPResult alias for core and transports
- [iftech/nim-libp2p#3188](https://github.com/iftech/nim-libp2p/pull/3188) chore(result): use LPResult alias in protocols
- [iftech/nim-libp2p#3187](https://github.com/iftech/nim-libp2p/pull/3187) chore(result): add LPResultError type
- [iftech/nim-libp2p#3195](https://github.com/iftech/nim-libp2p/pull/3195) chore(result): purge mapErr
- [iftech/nim-libp2p#3226](https://github.com/iftech/nim-libp2p/pull/3226) test: malformed protobuf and key protobuf decoding
- [iftech/nim-libp2p#3227](https://github.com/iftech/nim-libp2p/pull/3227) test(multiformat): cover decode error paths
- [iftech/nim-libp2p#3197](https://github.com/iftech/nim-libp2p/pull/3197) chore(result): use LPResultError in LPResult
- [iftech/nim-libp2p#3230](https://github.com/iftech/nim-libp2p/pull/3230) test(crypto): malformed DER for minasn1, ecnist and rsa
- [iftech/nim-libp2p#3228](https://github.com/iftech/nim-libp2p/pull/3228) test(transports): cancel tests for upgrade, memory and tor
- [iftech/nim-libp2p#3239](https://github.com/iftech/nim-libp2p/pull/3239) chore(builders): return error result insted of Defect
- [iftech/nim-libp2p#3219](https://github.com/iftech/nim-libp2p/pull/3219) chore(result): one path from each err to R.err
- [iftech/nim-libp2p#3251](https://github.com/iftech/nim-libp2p/pull/3251) chore(results): one shape for every err call site
- [iftech/nim-libp2p#3258](https://github.com/iftech/nim-libp2p/pull/3258) fix(service-discovery): no .get() on an optional ticket wait
- [iftech/nim-libp2p#3231](https://github.com/iftech/nim-libp2p/pull/3231) test: fault-stream helper for kad and service discovery error paths
