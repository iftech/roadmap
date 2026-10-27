---
title: Logos Basecamp QA
tags:
  - "2026q4"
  - "qa"
  - "logos"
draft: false
description: Expand Basecamp MCP coverage, validate releases, and maintain existing automated tests.
---

`ift-ts:qa:logos:2026q4-logos-basecamp`

## Description

Continue the Logos Basecamp MCP testing work from Q3, expanding automated UI integration coverage for preparation, installation navigation, and workspace application lifecycle behavior.
At Q4 planning, 61 of the 78 planned tests remain to be written.
Validate release artifacts and maintain the existing smoke, UI, sandbox, and doctest coverage as Basecamp evolves.

## Task List

### MCP tests

* fully qualified name: `ift-ts:qa:logos:2026q4-logos-basecamp:mcp-tests`
* owner: Roman
* status: in progress (45%)
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Implement the remaining 61 tests from the 78-test Basecamp MCP plan.
Keep new scenarios compatible with the existing test framework and track any scope changes or blockers as Basecamp evolves.

#### Deliverables
- [logos-co/logos-basecamp#477](https://github.com/logos-co/logos-basecamp/pull/477) Test/MCP UI apps inspector unload/reload of a non-visible UI plugin
- [logos-co/logos-basecamp#484](https://github.com/logos-co/logos-basecamp/pull/484) Test/MCP UI apps inspector unload/reload of package_manager_ui restores the Package Manager view
- [logos-co/logos-basecamp#485](https://github.com/logos-co/logos-basecamp/pull/485) Test/MCP UI module inspector search filters the table
- [logos-co/logos-basecamp#486](https://github.com/logos-co/logos-basecamp/pull/486) Test/MCP UI seed a loadable core-module fixture into the integration-test instance
- [logos-co/logos-basecamp#487](https://github.com/logos-co/logos-basecamp/pull/487) Test/MCP UI module inspector unloading a leaf module and reloading it
- [logos-co/logos-basecamp#488](https://github.com/logos-co/logos-basecamp/pull/488) Test/MCP UI module inspector interface view lists methods/events and calls a method
- [logos-co/logos-basecamp#511](https://github.com/logos-co/logos-basecamp/pull/511) Test/MCP UI module inspector interface view for a method-less module
- [logos-co/logos-basecamp#512](https://github.com/logos-co/logos-basecamp/pull/512) Test/MCP UI repositories invalid URL shows a dismissible error banner
- [logos-co/logos-basecamp#513](https://github.com/logos-co/logos-basecamp/pull/513) Test/MCP UI repositories unreachable URL is refused with a fetch error
- [logos-co/logos-basecamp#516](https://github.com/logos-co/logos-basecamp/pull/516) Test/MCP UI repositories whitespace is rejected and a duplicate is a no-op
- [logos-co/logos-basecamp#517](https://github.com/logos-co/logos-basecamp/pull/517) Test/MCP UI repositories refresh flips the button label
- [logos-co/logos-basecamp#518](https://github.com/logos-co/logos-basecamp/pull/518) Test/MCP UI repositories cancel on remove default repository keeps it
- [logos-co/logos-basecamp#519](https://github.com/logos-co/logos-basecamp/pull/519) Test/MCP UI window Cmd+M minimize action is wired (macOS)
- [logos-co/logos-basecamp#520](https://github.com/logos-co/logos-basecamp/pull/520) Test/MCP UI window hide-to-tray and restore preserves open docks
- [logos-co/logos-basecamp#521](https://github.com/logos-co/logos-basecamp/pull/521) Test/MCP UI apps inspector unloading the visible app closes its dock

### Release validation

* fully qualified name: `ift-ts:qa:logos:2026q4-logos-basecamp:release-validation`
* owner: Magnus
* status: in progress (25%)
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Validate Basecamp release artifacts and confirm the application starts cleanly on supported platforms.
Run release smoke checks, report defects and release risks, and verify fixes.

#### Deliverables

- Release validation checklists and test reports for the builds tested during Q4.
- Tracked release defects and verification results.
- [logos-co/logos-logoscore-cli#194](https://github.com/logos-co/logos-logoscore-cli/issues/194) `package install --root-hash` is accepted but never used: a hash that matches nothing still installs
- [logos-co/logos-storage-module#111](https://github.com/logos-co/logos-storage-module/issues/111) Storage data is always under `$HOME/.logos_storage`, so a second Basecamp or logosctl on the same machine fails to start Storage
- Ran the Basecamp 0.3.0 release checklist on macOS and Linux.

### Test coverage and maintenance

* fully qualified name: `ift-ts:qa:logos:2026q4-logos-basecamp:maintenance`
* owner: Roman
* status: not started
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Maintain and extend Basecamp smoke, UI, sandbox, and doctest coverage as the project evolves.
Investigate failing or flaky tests, adapt existing scenarios to application changes, and add regression coverage where needed.

#### Deliverables

- PRs maintaining the existing suites and adding targeted regression tests.
- Tracked application or test-framework defects and verification results.
