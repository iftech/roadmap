---
title: Web Maintenance & Support
tags:
  - "2026q4"
  - "web"
  - "ift"
draft: false
description: Maintain shared Web tooling, dependencies, and deployment workflows across the team's repositories.
---

`ift-ts:web:ift:2026q4-maintenance`

## Description

Continue recurring Web maintenance from Q3, focusing on common tooling and workflows used by the team's websites.
Keep shared dependencies, CI, preview deployments, and hosting integrations reliable.
Triage incoming requests with the team and track scope, priorities, and follow-up ownership.
Record site-specific upkeep and implementation under [[web/logos/2026q4-logos-website|Logos Website]], [[web/status/2026q4-status-website|Status Website]], [[web/status/2026q4-status-wallet-extension|Status Wallet Extension]], or [[web/ift/2026q4-admin-acid|Logos Admin]], with shared changes tracked here once.
Shared AI workflow tooling is tracked separately under [[web/ift/2026q4-ai-tooling|AI Tooling]].

## Task List

### Maintenance

* fully qualified name: `ift-ts:web:ift:2026q4-maintenance:maintenance`
* owner: Jinho/JulesFiliot
* status: done
* start-date: 2026/10/01
* end-date: 2026/10/13

#### Description

Maintain common build tools, shared dependencies, CI checks, preview deployments, and hosting workflows.
Resolve shared infrastructure or tooling failures, coordinate with Infra where needed, and document changes that affect website development or releases.

#### Deliverables
- [status-im/nimbus-site#180](https://github.com/status-im/nimbus-site/pull/180) fix: point shared footer links at Logos technology stack
- [keycard-tech/keycard-website#266](https://github.com/keycard-tech/keycard-website/pull/266) chore: update Node.js to 24
- [acid-info/free.technology#23](https://github.com/acid-info/free.technology/pull/23) fix: update team member to Dr. Martin Strobl
- [acid-info/admin-acid.logos.co#76](https://github.com/acid-info/admin-acid.logos.co/pull/76) fix(redis): lazily create client to avoid connecting at build
- [Status app Korean translation](https://docs.google.com/document/d/101OBvvoprtp5I5GXFf5hBLrsvSV8R5YShX3smgnQbhE/edit?tab=t.qso6thz9xpc3)
- [Status app store French translation — Apple doc](https://docs.google.com/document/d/199SNFI-fFA4pTaG8Xp-y26um6HAQf42mcp8PFB08CwQ/edit?tab=t.tkqt8nea3kvv)
- [Status app store French translation — Google Play doc](https://docs.google.com/document/d/199SNFI-fFA4pTaG8Xp-y26um6HAQf42mcp8PFB08CwQ/edit?tab=t.ghept0o2oy0u)
- [status-im/infra-sites#175](https://github.com/status-im/infra-sites/issues/175) Request a security-patched MediaWiki test instance for the Logos wiki, including the PHP RCE patches disclosed on 21 October
