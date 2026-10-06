---
title: Status QA Mobile
tags:
  - "2026q4"
  - "qa"
  - "status"
draft: false
description: Support Status Mobile releases, maintain reliable automation, and expand coverage, framework capabilities, and performance testing.
---

`ift-ts:qa:status:2026q4-status-qa-mobile`

## Description

Support ongoing Status Mobile releases, including at least 2.40 and 2.41, and test the new features in each release.
Keep nightly automation and the per-PR gate reliable, add coverage for existing features, and improve the test harness.
Maintain the performance suite and extend measurements to a loaded existing account.

## Task List

### Release testing

* fully qualified name: `ift-ts:qa:status:2026q4-status-qa-mobile:release-testing`
* owner: Magnus
* status: in progress (10%)
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Support ongoing Status Mobile releases, including at least 2.40 and 2.41.
Perform exploratory and regression testing, test new features in each release, and report issues and release risks.

#### Deliverables
- [status-im/status-app#22522](https://github.com/status-im/status-app/issues/22522) \[QA - Mobile\] Share to Status: what to test in 2.40

### Maintenance

* fully qualified name: `ift-ts:qa:status:2026q4-status-qa-mobile:maintenance`
* owner: Magnus
* status: in progress (10%)
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Investigate and fix failing nightly tests and keep the per-PR gate running as a trusted regression signal.
Address flaky tests and assist developers with test changes in pull requests as the app evolves.

#### Deliverables
- [status-im/status-app#22504](https://github.com/status-im/status-app/pull/22504) test(e2e_appium): press only a message that is on screen
- Verified the logos-qt-mcp Qt inspector prototype on Status desktop and Android.

### Coverage for existing features

* fully qualified name: `ift-ts:qa:status:2026q4-status-qa-mobile:coverage`
* owner: magnus
* status: not started
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Add automated tests for existing Status Mobile features that lack coverage.
Prioritize gaps with the Status team based on user impact and the feasibility of reliable device-level automation.

#### Deliverables

- PRs covering previously untested existing features.
- Tracked coverage gaps and any constraints preventing automation.

### Framework improvements

* fully qualified name: `ift-ts:qa:status:2026q4-status-qa-mobile:framework`
* owner: magnus
* status: not started
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Improve the mobile test harness in the following areas:
- iOS build and execution support.
- Repeatable setup and reuse of a loaded existing account.
- Accessibility properties that provide stable locators and assertions.
- App/backend binding checks that detect missing or changed backend methods.
- Backend-peer support for messaging scenarios with a headless second participant.

#### Deliverables

- PRs implementing harness improvements and contract checks.
- Setup and usage documentation for iOS, loaded accounts, and backend-peer scenarios.

### Performance

* fully qualified name: `ift-ts:qa:status:2026q4-status-qa-mobile:performance`
* owner: Magnus
* status: in progress (25%)
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Maintain the mobile performance suite and add a loaded-account scenario using the account setup provided by the framework task.
Keep measurements useful for comparing releases and identifying performance regressions.

#### Deliverables
- [status-im/status-app#21248](https://github.com/status-im/status-app/issues/21248) \[QA - Android/iOS\] add test to measure Battery consumption, CPU and RAM usage
- Restored Android performance runs and published RC7 measurements.
