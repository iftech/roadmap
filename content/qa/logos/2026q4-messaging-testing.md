---
title: Messaging Testing
tags:
  - "2026q4"
  - "qa"
  - "logos"
draft: false
description: Maintain messaging testing frameworks and continue migrating interop tests into Logos Delivery.
---

`ift-ts:qa:logos:2026q4-messaging-testing`

## Description

Continue improving messaging test reliability by maintaining existing frameworks and migrating the remaining interop tests into the Logos Delivery repository.
Adapt tests to messaging component changes, address regressions, and keep coverage useful as the implementation evolves.

## Task List

### Interop migration

* fully qualified name: `ift-ts:qa:logos:2026q4-messaging-testing:interop-migration`
* owner: Florin/Radek
* status: in progress (95%)
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Continue the Q3 migration of messaging interop tests into the Logos Delivery repository.
Port the remaining scenarios to the repository's E2E workflow, preserve relevant protocol coverage, and resolve failures or gaps exposed by the migration.

#### Deliverables
- [logos-messaging/logos-delivery#4335](https://github.com/logos-messaging/logos-delivery/pull/4335) test(e2e): cleanup harness code (migration 14)
- [logos-messaging/logos-delivery#4348](https://github.com/logos-messaging/logos-delivery/pull/4348) test(e2e): rename the wrapper suite to c_abi (migration 15)
- [logos-messaging/logos-delivery#4350](https://github.com/logos-messaging/logos-delivery/pull/4350) test(e2e): run the C ABI suite in parallel and make its xfailed tests pass (migration 16)
- [logos-messaging/logos-delivery#4353](https://github.com/logos-messaging/logos-delivery/pull/4353) test(e2e): python binding as a submodule (migration 17)
- [logos-messaging/logos-delivery-python-bindings#9](https://github.com/logos-messaging/logos-delivery-python-bindings/pull/9) chore: bump logos-delivery and move the wrapper to the CBOR ABI

### Maintenance

* fully qualified name: `ift-ts:qa:logos:2026q4-messaging-testing:maintenance`
* owner: Radek
* status: in progress (25%)
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Provide ongoing maintenance of messaging testing frameworks.
Update tests for messaging component changes, investigate failing or flaky tests, address regressions, and make minor framework improvements needed to keep the suites reliable.

#### Deliverables
- [logos-messaging/logos-delivery#4368](https://github.com/logos-messaging/logos-delivery/pull/4368) ci: cache nim, nimble and nimcache (ci improvements 1)
- [logos-messaging/logos-delivery#4379](https://github.com/logos-messaging/logos-delivery/pull/4379) test: configurable waiting times (ci improvements 2)
- [logos-messaging/logos-delivery#4395](https://github.com/logos-messaging/logos-delivery/pull/4395) test: wait on conditions instead of fixed sleeps (ci improvements 3)
