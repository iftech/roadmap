---
title: Status QA Desktop
tags:
  - "2026q4"
  - "qa"
  - "status"
draft: false
description: Support Status Desktop releases, maintain automated tests, and expand feature and performance coverage.
---

`ift-ts:qa:status:2026q4-status-qa-desktop`

## Description

Collaborate with the Status team on manual and automated QA for ongoing Desktop releases, including at least 2.40 and 2.41.
Maintain the existing test suite and expand coverage for new features as release scope becomes clear.
Keep feature automation flexible as priorities and delivery dates change; select concrete scenarios with the Status team as the automation backlog is clarified.
Continue Windows performance testing. macOS and Linux performance work remains tentative, subject to infrastructure availability and prioritization.

## Task List

### Release Testing

* fully qualified name: `ift-ts:qa:status:2026q4-status-qa-desktop:release-testing`
* owner: Nastya
* status: in progress (10%)
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Support ongoing Status Desktop releases, including at least 2.40 and 2.41, with exploratory testing, regression testing, and validation of new features.
Report bugs and release risks and verify fixes with the Status team.

#### Deliverables
- [status-im/status-app#22603](https://github.com/status-im/status-app/pull/22603) fix(wallet): keep the derived account address inside its field
- [status-im/status-app#22604](https://github.com/status-im/status-app/issues/22604) Race condition when balances arrive before the token catalog is ready leads to token list staying empty / loading

### Maintenance

* fully qualified name: `ift-ts:qa:status:2026q4-status-qa-desktop:maintenance`
* owner: Nastya
* status: in progress (25%)
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Investigate and fix failing nightly tests, address flaky scenarios, and keep the suite compatible with Status Desktop changes.
Assist developers with test changes in pull requests.

#### Deliverables
- [status-im/status-app#22623](https://github.com/status-im/status-app/pull/22623) chore(@e2e): skip destroyed community nav buttons after leave
- [status-im/status-app#22756](https://github.com/status-im/status-app/pull/22756) Revert "fix(chat): mark messages read when the newest one is on screen"
- [status-im/status-app#22736](https://github.com/status-im/status-app/pull/22736) fix(@e2e): record a CPU/RAM sample when a benchmark action finishes before the sampler thread
- [status-im/market-proxy#84](https://github.com/status-im/market-proxy/pull/84) feat: add base sepolia WETH to token list
- [status-im/market-proxy#83](https://github.com/status-im/market-proxy/pull/83) feat: add sepolia WETH to token list
- [status-im/status-app#22695](https://github.com/status-im/status-app/pull/22695) chore(@e2e): fix sign modal test reference
- [status-im/status-app#22654](https://github.com/status-im/status-app/pull/22654) fix(e2e): wait for link preview instead of failing on slow unfurl
- [status-im/status-app#22653](https://github.com/status-im/status-app/pull/22653) fix(chat): mark messages read when the newest one is on screen

### Performance tests for desktop application on Windows

* fully qualified name: `ift-ts:qa:status:2026q4-status-qa-desktop:windows-performance-tests`
* owner: nastya
* status: not started
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Continue creating Windows performance tests for the main Status Desktop user flows.
Maintain useful measurements for comparing releases and detecting performance regressions.

#### Deliverables

- PRs extending Windows performance test coverage.
- Performance measurements and tracked regressions.

### New tests

* fully qualified name: `ift-ts:qa:status:2026q4-status-qa-desktop:new-tests`
* owner: Nastya
* status: in progress (54%)
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Add automated coverage for new Status Desktop features, including those delivered in 2.40 and 2.41.
Choose scenarios as feature scope and the automation backlog are clarified with the Status team, and adjust coverage when features are delayed or changed.

#### Deliverables
- [status-im/status-app#22583](https://github.com/status-im/status-app/pull/22583) fix(communities): hide joined members in invite popup after accept request
- [status-im/status-go#7916](https://github.com/status-im/status-go/pull/7916) fix(wallet): omit relay API key on testnet
- [status-im/status-app#22741](https://github.com/status-im/status-app/pull/22741) tests(@e2e): send NFT on testnet
- [status-im/status-app#22734](https://github.com/status-im/status-app/pull/22734) test(@qml): onchain friends nim and QML coverage
- [status-im/status-app#22702](https://github.com/status-im/status-app/pull/22702) tests(@qml): buy crypto links
- [status-im/status-app#22607](https://github.com/status-im/status-app/pull/22607) tests(@e2e): request payment in chat

### Performance tests for desktop application on Mac

* fully qualified name: `ift-ts:qa:status:2026q4-status-qa-desktop:mac-performance-tests`
* owner: nastya
* status: not started
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Tentative: confirm with Infra whether a supported environment for macOS performance testing can be provided.
If the infrastructure dependency is resolved and the work is prioritized, add performance tests for the main Status Desktop user flows on macOS.

#### Deliverables

- A documented infrastructure decision and any remaining constraints.
- Performance test PRs and measurements if the work proceeds.

### Performance tests for desktop application on Linux

* fully qualified name: `ift-ts:qa:status:2026q4-status-qa-desktop:linux-performance-tests`
* owner: nastya
* status: not started
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Tentative: confirm whether Linux performance testing remains a Q4 priority and identify the scenarios worth covering.
If prioritized, add performance tests for the main Status Desktop user flows on Linux.

#### Deliverables

- A documented scope and prioritization decision.
- Performance test PRs and measurements if the work proceeds.
