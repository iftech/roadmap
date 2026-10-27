---
title: AI Tooling
tags:
  - "2026q4"
  - "web"
  - "ift"
draft: false
description: Build and maintain the team's shared AI workflow tooling; ai-review, its ai-auto-fix companion, and ai-docs-sync.
---

`ift-ts:web:ift:2026q4-ai-tooling`

## Description

Three tools are in scope: [ai-review](https://github.com/acid-info/ai-review), already consumed by `status-im/status-web`, `logos-co/logos-web`, and `acid-info/admin-acid.logos.co`; an **ai-auto-fix** companion that turns accepted ai-review findings into a patch, not yet started; and [ai-docs-sync](https://github.com/acid-info/ai-docs-sync), in development.
All three ship as reusable GitHub workflows pinned to `@v1`, with zero npm dependencies, so a tool or model change is one edit in the shared repository rather than one per consumer.
Human approval before merge stays a hard requirement for every tool here.

## Task List

### Shared AI tooling monorepo

* fully qualified name: `ift-ts:web:ift:2026q4-ai-tooling:monorepo`
* owner: JulesFiliot
* status: in progress (80%)
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Consolidate ai-review and ai-docs-sync in [acid-info/ai-tools](https://github.com/acid-info/ai-tools), with shared core modules and separate tool modules. Maintain shared repository documentation and run both tools against the monorepo.

#### Deliverables
- [docs: split root README and AGENTS.md by audience](https://github.com/acid-info/ai-tools/pull/1)
- [ci: run ai-review and ai-docs-sync on this repo](https://github.com/acid-info/ai-tools/pull/4)
- [acid-info/ai-tools#14](https://github.com/acid-info/ai-tools/pull/14) docs: apply the house style to the root docs

### ai-review maintenance and tuning

* fully qualified name: `ift-ts:web:ift:2026q4-ai-tooling:ai-review`
* owner: JulesFiliot
* status: in progress (45%)
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Maintain [acid-info/ai-review](https://github.com/acid-info/ai-review) as the shared PR reviewer for `logos-co`, `status-im`, and `acid-info` repositories.
Keep the dual-model review plus synthesis pipeline reliable as provider APIs and models change, tune per-repository context and guideline files to cut false positives, and refine diff packing, path filtering, and severity thresholds.
Keep the degraded paths honest: a single-model review when one provider is down, a local merge when synthesis fails, and a posted body that says the review was partial.
Onboard remaining Web repositories and keep the `@v1` tag stable for consumers.

#### Deliverables
- [acid-info/ai-tools#2](https://github.com/acid-info/ai-tools/pull/2) docs(ai-review): add AGENTS.md and trim the README
- [acid-info/ai-tools#5](https://github.com/acid-info/ai-tools/pull/5) ci: bump node to 24
- [acid-info/admin-acid.logos.co#77](https://github.com/acid-info/admin-acid.logos.co/pull/77) chore(ci): use ai-review from acid-info/ai-tools
- [logos-co/logos-web#208](https://github.com/logos-co/logos-web/pull/208) chore(ci): use ai-review and ai-docs-sync from acid-info/ai-tools
- [status-im/status-web#1326](https://github.com/status-im/status-web/pull/1326) chore(ci): use ai-review from acid-info/ai-tools
- [acid-info/ai-review#8](https://github.com/acid-info/ai-review/pull/8) docs: redirect to acid-info/ai-tools
- [acid-info/ai-tools#13](https://github.com/acid-info/ai-tools/pull/13) refactor(ai-review): restyle the reviewer and synthesis prompts
- [acid-info/ai-tools#15](https://github.com/acid-info/ai-tools/pull/15) refactor(ai-review): drop dashes and emoji from posted reviews
- [acid-info/ai-tools#16](https://github.com/acid-info/ai-tools/pull/16) docs(ai-review): apply the house style

### ai-auto-fix companion

* fully qualified name: `ift-ts:web:ift:2026q4-ai-tooling:ai-auto-fix`
* owner: JulesFiliot
* status: not started
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Build an **ai-auto-fix** companion to ai-review that takes review findings and produces a patch the author can accept, rather than leaving every finding as manual follow-up work.
Nothing exists yet, so the task starts from specification: which finding severities and categories are eligible, how a fix is requested (a comment command on the PR, or opt-in per finding), how the patch is delivered (a commit pushed to the PR branch, or a suggested-change comment), and what the tool must refuse to touch.
Reuse the ai-review pipeline's shape -- reusable workflow, zero npm dependencies, Node 22 `fetch`, pinned `@v1` -- and keep every produced change inside normal PR review with no branch-protection bypass.

#### Deliverables

- Written specification covering eligible findings, trigger mechanism, patch delivery, and refusal rules.
- Prototype workflow producing patches against real ai-review findings on Web repositories.
- Documented guardrails: disallowed change types, secret handling, and required human approval before merge.

### ai-docs-sync

* fully qualified name: `ift-ts:web:ift:2026q4-ai-tooling:ai-docs-sync`
* owner: JulesFiliot
* status: in progress (80%)
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Finish [acid-info/ai-docs-sync](https://github.com/acid-info/ai-docs-sync), which keeps a repository's documentation in step with its code by triaging each push, rewriting affected docs with one model, checking the rewrite with a second, and running mechanical gates.

#### Deliverables

- Merged publishing stage: rolling branch and PR, cursor move, generated PR body, with unit tests.
- End-to-end runs on a real repository, including unmerged-edit carry-forward and collapsed-push handling.
- `v1` tag cut and the README status banner removed.
- First consumer repository onboarded via `.github/workflows/docs-sync.yml`, with the resulting docs PRs linked.
- [acid-info/ai-docs-sync#4](https://github.com/acid-info/ai-docs-sync/pull/4) feat(tool): delete stale docs and drop the per-run cap
- [acid-info/ai-docs-sync#5](https://github.com/acid-info/ai-docs-sync/pull/5) feat(tool): create docs for new surfaces
- [acid-info/ai-docs-sync#6](https://github.com/acid-info/ai-docs-sync/pull/6) feat(tool): honour reviewer deletes and renames on the rolling branch
- [acid-info/ai-tools#3](https://github.com/acid-info/ai-tools/pull/3) docs(ai-docs-sync): add AGENTS.md and trim the README
- [acid-info/ai-tools#5](https://github.com/acid-info/ai-tools/pull/5) ci: bump node to 24
- [logos-co/logos-web#208](https://github.com/logos-co/logos-web/pull/208) chore(ci): use ai-review and ai-docs-sync from acid-info/ai-tools
- [acid-info/ai-docs-sync#7](https://github.com/acid-info/ai-docs-sync/pull/7) docs: redirect to acid-info/ai-tools
- [acid-info/ai-tools#7](https://github.com/acid-info/ai-tools/pull/7) fix(ai-docs-sync): sign the rolling commit
- [acid-info/ai-tools#8](https://github.com/acid-info/ai-tools/pull/8) feat(ai-docs-sync): request reviewers on the rolling pr
- [acid-info/ai-tools#10](https://github.com/acid-info/ai-tools/pull/10) ci: request web team review on the docs sync pr
- [logos-co/logos-web#234](https://github.com/logos-co/logos-web/pull/234) ci: request web team review on the docs sync pr
- [acid-info/admin-acid.logos.co#83](https://github.com/acid-info/admin-acid.logos.co/pull/83) chore(ci): add ai-docs-sync from acid-info/ai-tools
- [status-im/status-web#1331](https://github.com/status-im/status-web/pull/1331) chore(ci): add ai-docs-sync from acid-info/ai-tools
- [acid-info/admin-acid.logos.co#87](https://github.com/acid-info/admin-acid.logos.co/pull/87) fix(docs-sync): request web members by login
- [acid-info/ai-tools#12](https://github.com/acid-info/ai-tools/pull/12) fix(docs-sync): request web members by login
- [logos-co/logos-web#240](https://github.com/logos-co/logos-web/pull/240) fix(docs-sync): request web members by login
- [status-im/status-web#1333](https://github.com/status-im/status-web/pull/1333) fix(docs-sync): request web members by login
- [acid-info/ai-tools#17](https://github.com/acid-info/ai-tools/pull/17) feat(ai-docs-sync): write docs in the house style
- [acid-info/ai-tools#18](https://github.com/acid-info/ai-tools/pull/18) refactor(ai-docs-sync): drop dashes from the pr body
- [acid-info/ai-tools#19](https://github.com/acid-info/ai-tools/pull/19) docs(ai-docs-sync): apply the house style
- [logos-co/logos-web#242](https://github.com/logos-co/logos-web/pull/242) docs(repo): restructure docs for docs-sync
- [logos-co/logos-web#243](https://github.com/logos-co/logos-web/pull/243) docs(repo): rewrite docs for humans and agents
- [status-im/status-web#1334](https://github.com/status-im/status-web/pull/1334) docs(repo): restructure docs for docs-sync
- [status-im/status-web#1335](https://github.com/status-im/status-web/pull/1335) docs(repo): rewrite docs for humans and agents
