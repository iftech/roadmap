---
title: Logos LEZ Fuzz Testing
tags:
  - "2026q4"
  - "qa"
  - "logos"
draft: false
description: Maintain LEZ fuzz targets, corpus automation, and CI reliability as the implementation evolves.
---

`ift-ts:qa:logos:2026q4-lez-fuzz-testing`

## Description

Continue maintaining the LEZ fuzz testing framework in Q4.
Keep targets compatible with upstream changes and preserve useful corpus handling, automated execution, and regression coverage.

## Task List

### Framework maintenance

* fully qualified name: `ift-ts:qa:logos:2026q4-lez-fuzz-testing:framework-maintenance`
* owner: Roman
* status: in progress (10%)
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

- Maintain existing fuzz targets as LEZ code and interfaces change.
- Extend or adjust targets for newly exposed execution paths, invariants, or regressions.
- Maintain corpus update automation and CI execution, documenting infrastructure constraints when they arise.

#### Deliverables
- [logos-blockchain/lez-fuzzing#35](https://github.com/logos-blockchain/lez-fuzzing/pull/35) chore: automated weekly corpus update
- [logos-blockchain/lez-fuzzing#36](https://github.com/logos-blockchain/lez-fuzzing/pull/36) chore: sync with LEZ main (account shards, native transfers, no deployment tx)
