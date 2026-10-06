---

title: Anoncomms Unified Networking
tags:
  - "2026q3"
  - "p2p"
  - "ift"
draft: false
description: Support Anoncomms unified networking module design and implementation

---

`ift-ts:p2p:ift:2026q3-anoncomms-unified-networking`

Support Anoncomms in designing and implementing a unified networking module that
packages libp2p, mix, and RLN-for-mix into a cohesive downstream component.

## Description

P2P provides consulting, design review, and implementation support for the
Anoncomms unified networking module. The exact scope is still expected to
change, so the first part of the commitment is to define module boundaries,
runtime responsibilities, configuration surfaces, and handoff points between
libp2p, mix, and RLN-for-mix.

This commitment should remain flexible while the Anoncomms team refines its
architecture, but it should still produce concrete module design and integration
artifacts during Q3.

## Task List

### Scope And Architecture

* fully qualified name: `ift-ts:p2p:ift:2026q3-anoncomms-unified-networking:scope-architecture`
* owner: Richard
* status: done
* start-date: 2026/07/01
* end-date: 2026/09/29

#### Description
Work with Anoncomms to define the responsibilities of the unified networking
module, including which functionality belongs in the module itself and which
functionality should remain in nim-libp2p, mix, RLN-for-mix, or downstream
application code.

#### Deliverables

- [logos-libp2p-mix-rln#1](https://github.com/logos-co/logos-libp2p-mix-rln/pull/1) feat: use Delivery for RLN coordination
- [nim-libp2p-mix-rln-ffi#1](https://github.com/logos-co/nim-libp2p-mix-rln-ffi/pull/1) feat(ffi): use Delivery as Mix-RLN node
- Initial module responsibility map
- Integration assumptions for libp2p, mix, and RLN-for-mix
- List of open design questions and required decisions
- [vacp2p/zerokit#435](https://github.com/vacp2p/zerokit/pull/435) nix: bump release-25.11 rev to pick up fetch-cargo-vendor-util-v2, and update cargoHash for v3.0.0
- Created [nim-libp2p-mix-rln-ffi](https://github.com/logos-co/nim-libp2p-mix-rln-ffi) and [logos-libp2p-mix-rln](https://github.com/logos-co/logos-libp2p-mix-rln) for the unified Logos Core networking module.
- [logos-co/logos-libp2p-mix-rln#3](https://github.com/logos-co/logos-libp2p-mix-rln/pull/3) build(mix)!: use merged shared-only FFI from main
- [logos-co/logos-libp2p-mix-rln#2](https://github.com/logos-co/logos-libp2p-mix-rln/pull/2) feat(mix): add standalone intermediates with shared RLN proofs
- [logos-co/nim-libp2p-mix-ffi#2](https://github.com/logos-co/nim-libp2p-mix-ffi/pull/2) feat: run Mix on a standalone libp2p switch
- [logos-co/logos-rln-modules#34](https://github.com/logos-co/logos-rln-modules/pull/34) fix(rln): expose effective registry epoch gap
- [logos-co/logos-libp2p-mix-rln#6](https://github.com/logos-co/logos-libp2p-mix-rln/pull/6) build: update Mix FFI pin to latest upstream main
- [logos-co/nim-libp2p-mix-ffi#4](https://github.com/logos-co/nim-libp2p-mix-ffi/pull/4) refactor(ffi): enable sending and exit delivery by default
- [logos-co/nim-libp2p-mix-ffi#3](https://github.com/logos-co/nim-libp2p-mix-ffi/pull/3) refactor(ffi)!: expose exit-as-destination only
- [logos-co/logos-libp2p-mix-rln#4](https://github.com/logos-co/logos-libp2p-mix-rln/pull/4) build(wallet): migrate registry dependency to upstream LEZ
- [logos-co/logos-libp2p-mix-rln#5](https://github.com/logos-co/logos-libp2p-mix-rln/pull/5) refactor(mix)!: expose exit-as-destination only
- [logos-co/logos-libp2p-mix-rln#14](https://github.com/logos-co/logos-libp2p-mix-rln/pull/14) test(e2e): configure Delivery pure-libp2p peer budget
- [logos-co/logos-modules-release#75](https://github.com/logos-co/logos-modules-release/pull/75) chore: release libp2p module 1.1.0
- [logos-co/logos-libp2p-mix-rln#13](https://github.com/logos-co/logos-libp2p-mix-rln/pull/13) docs(e2e): add native build prerequisites
- [logos-co/logos-libp2p-mix-rln#12](https://github.com/logos-co/logos-libp2p-mix-rln/pull/12) chore(mix): pin and document tested seven-host stack
- [logos-co/nim-libp2p-mix-ffi#7](https://github.com/logos-co/nim-libp2p-mix-ffi/pull/7) chore: update Mix RLN plugin pin
- [logos-co/nim-libp2p-mix-ffi#6](https://github.com/logos-co/nim-libp2p-mix-ffi/pull/6) chore(deps): update Mix integration
- [logos-co/logos-libp2p-module#114](https://github.com/logos-co/logos-libp2p-module/pull/114) chore(build): pin nim-libp2p and set version 1.1.0
- [logos-co/logos-libp2p-mix-rln#11](https://github.com/logos-co/logos-libp2p-mix-rln/pull/11) docs: update native Delivery integration pins
- [logos-co/logos-libp2p-mix-rln#10](https://github.com/logos-co/logos-libp2p-mix-rln/pull/10) chore(rln): pin backend directly
- [logos-co/logos-libp2p-mix-rln#9](https://github.com/logos-co/logos-libp2p-mix-rln/pull/9) chore(rln): pin typed verification result
- [logos-co/logos-rln-modules#27](https://github.com/logos-co/logos-rln-modules/pull/27) feat(rln): accept Mix proofs with a derived external nullifier
- [logos-co/logos-delivery-module#125](https://github.com/logos-co/logos-delivery-module/pull/125) feat(mix): expose native Mix routing with a shared RLN backend
- [logos-co/logos-libp2p-mix-rln#7](https://github.com/logos-co/logos-libp2p-mix-rln/pull/7) refactor(mix): configure cover rate only at initialization
- [logos-co/nim-libp2p-mix-ffi#5](https://github.com/logos-co/nim-libp2p-mix-ffi/pull/5) refactor(ffi): configure cover rate only at initialization
- [logos-messaging/logos-delivery#4181](https://github.com/logos-messaging/logos-delivery/pull/4181) feat(mix): allow spam protection injection
