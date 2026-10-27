---

title: Logos Delivery Consulting
tags:
  - "2026q4"
  - "p2p"
  - "ift"
draft: false
description: Support Logos Delivery with pluggable libp2p, nim-ffi, and module API integration

---

`ift-ts:p2p:ift:2026q4-logos-delivery-consulting`

## Description

Provide consulting to Logos Delivery as they make libp2p pluggable, tracked in
[logos-delivery#4341](https://github.com/logos-messaging/logos-delivery/issues/4341).
Coordinate the integration with the Logos libp2p module, support nim-ffi design
and code reviews, and help the team understand the API the module offers.

This as an ongoing consulting commitment, adding specific follow-up tasks
as requirements and priorities become clearer during Q4.

## Task List

### Consulting

* fully qualified name: `ift-ts:p2p:ift:2026q4-logos-delivery-consulting:consulting`
* owner: Gabe
* status: in progress (27%)
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Work with the Logos Delivery team on the interfaces and integration needs for
pluggable libp2p. Explain the Logos libp2p module API, identify missing capabilities,
and review opportunities to modify or simplify it based on Delivery's needs.

Review nim-ffi pull requests and discuss or propose changes where needed,
including the proposed use of polling instead of callbacks. Coordinate resulting
API and integration decisions with Delivery and capture concrete follow-up work
as it is agreed.

#### Deliverables
- [logos-messaging/nim-ffi#209](https://github.com/logos-messaging/nim-ffi/pull/209) chore(ffi): zero the request envelope with c_calloc
- [logos-messaging/nim-ffi#205](https://github.com/logos-messaging/nim-ffi/pull/205) chore(ci): one source for the sanitizer runtime options
- [logos-messaging/nim-ffi#226](https://github.com/logos-messaging/nim-ffi/pull/226) fix(ffi): set up the caller thread's GC before a request is rejected
- [logos-messaging/nim-ffi#227](https://github.com/logos-messaging/nim-ffi/pull/227) fix: build with a tagged chronos
- [logos-messaging/nim-ffi#236](https://github.com/logos-messaging/nim-ffi/pull/236) fix(codegen): return the send error from the C wrappers
- [logos-messaging/nim-ffi#238](https://github.com/logos-messaging/nim-ffi/pull/238) fix(ffi): refuse a NULL callback in the callback-mode ctor
- [logos-messaging/nim-ffi#228](https://github.com/logos-messaging/nim-ffi/pull/228) chore: narrow LSan suppressions
- [logos-storage/logos-storage-nim#1519](https://github.com/logos-storage/logos-storage-nim/pull/1519) feat(library): generate the C bindings with nim-ffi
- [logos-messaging/nim-ffi#249](https://github.com/logos-messaging/nim-ffi/pull/249) fix: skip a listener removed during its dispatch
- [logos-messaging/nim-ffi#250](https://github.com/logos-messaging/nim-ffi/pull/250) fix: destroy from inside a callback fails fast
