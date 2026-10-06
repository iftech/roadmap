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
* status: in progress (4%)
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
