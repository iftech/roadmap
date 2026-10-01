---
title: Website E2E Testing
tags:
  - "2026q4"
  - "web"
  - "ift"
draft: false
description: Add nightly end-to-end browser tests for status.app and logos.co so broken pages, missing key elements, and navigation regressions are caught before users report them.
---

`ift-ts:web:ift:2026q4-e2e-testing`

## Description

[status.app](https://status.app/) ([status-im/status-web](https://github.com/status-im/status-web)) and [logos.co](https://logos.co/) ([logos-co/logos-web](https://github.com/logos-co/logos-web)) have nothing that checks the live sites in real browsers on a schedule; regressions surface through users, stakeholders, or the team.
Q4 adds an end-to-end suite to each monorepo that loads the production sites in Chromium and Firefox, asserts that critical pages and elements are present, and walks the main navigation paths.
Both suites run every night through GitHub Actions and report failures to the team.
Playwright is the proposed runner since it covers both browsers; reuse the existing e2e tooling in `status-web` where it fits.

## Task List

### status.app E2E suite

* fully qualified name: `ift-ts:web:ift:2026q4-e2e-testing:status-app`
* owner: Jinho/JulesFiliot
* status: not started
* start-date: 2026/10/05
* end-date: 2026/10/30

#### Description

Set up the e2e harness for the `status.app` app in `status-web` and cover the highest-traffic pages: home, apps and downloads, blog and blog search, help, Keycard, and legal pages.
Check that each page loads without errors, that key elements (navigation, hero, calls to action, download links, footer) are visible, and that navigating between pages, opening blog posts, and switching languages lands on the expected URL.

#### Deliverables

- PRs in `status-im/status-web` adding the e2e configuration and the status.app suite, runnable locally against production or a preview URL.
- Smoke tests for critical pages and key elements, plus navigation tests for the main user journeys, passing in Chromium and Firefox.

### logos.co E2E suite

* fully qualified name: `ift-ts:web:ift:2026q4-e2e-testing:logos-co`
* owner: Jinho/JulesFiliot
* status: not started
* start-date: 2026/10/19
* end-date: 2026/11/20

#### Description

Set up the e2e harness in `logos-web` and cover the main pages: home, tech stack, release and download pages, Circles, forms, and the newsletter signup (without submitting).
Cover the new `/media` article and podcast routes once they reach production through [[web/logos/2026q4-logos-media-migration|Logos Media]], and check that a sample of `blog.logos.co` URLs redirect to them after the cutover.

#### Deliverables

- PRs in `logos-co/logos-web` adding the e2e configuration and the logos.co suite, runnable locally against production or a preview URL.
- Smoke tests for critical pages and key elements, plus navigation tests for the main user journeys, passing in Chromium and Firefox.
- `/media` coverage and a redirect sample added after the media cutover.

### Nightly runs and reporting

* fully qualified name: `ift-ts:web:ift:2026q4-e2e-testing:nightly-ci`
* owner: Jinho/JulesFiliot
* status: not started
* start-date: 2026/11/02
* end-date: 2026/12/04

#### Description

Run both suites every night against production through scheduled GitHub Actions workflows, with manual dispatch for on-demand runs.
Keep the runs trustworthy: retry once before failing, keep traces and screenshots of failures, and notify the team so a red run gets triaged under [[web/ift/2026q4-maintenance|Web Maintenance]] instead of going unnoticed.

#### Deliverables

- Scheduled workflows in `status-web` and `logos-web` running the Chromium and Firefox projects nightly.
- Failure artifacts (traces, screenshots) attached to each failed run.
- Failure notifications sent to an agreed channel or opened as GitHub issues.
- Analytics requests blocked during test runs so nightly visits do not skew site analytics.
- A short README note on running the suites locally and adding a test.
