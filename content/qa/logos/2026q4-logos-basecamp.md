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
* status: in progress (43%)
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

### Release validation

* fully qualified name: `ift-ts:qa:logos:2026q4-logos-basecamp:release-validation`
* owner: TBD
* status: not started
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Validate Basecamp release artifacts and confirm the application starts cleanly on supported platforms.
Run release smoke checks, report defects and release risks, and verify fixes.

#### Deliverables

- Release validation checklists and test reports for the builds tested during Q4.
- Tracked release defects and verification results.

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
