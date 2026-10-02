---
title: Status Website
tags:
  - "2026q4"
  - "web"
  - "status"
draft: false
description: Maintain the Status website, revamp its UI, copy, performance, and translations, and implement prioritized ad hoc features.
---

`ift-ts:web:status:2026q4-status-website`

## Description

Continue supporting the Status website in Q4 through recurring upkeep, fixes and improvements to existing functionality, and delivery of new features requested during the quarter.
Maintain the marketing, blog, help, and feed experiences developed in previous quarters.
Revamp the website through four work streams agreed with Volodymyr on 2026/10/01: UI design and copy, performance, cleanup of unused pages, and translation, tackled progressively with the UI revamp first.
Select concrete work with stakeholders as needs arise and record the scope and acceptance criteria in linked issues.

## Task List

### Maintenance

* fully qualified name: `ift-ts:web:status:2026q4-status-website:maintenance`
* owner: Jinho/JulesFiliot
* status: not started
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Keep the Status website and its existing integrations working as dependencies, content, and releases change.
Maintain site-specific dependencies and configuration, CMS and feed integrations, release and download information, and deployment health.
Investigate production failures and ship necessary hotfixes, coordinating shared tooling changes with the Web maintenance commitment.

#### Deliverables

- PRs for site upkeep, dependency updates, configuration changes, and production hotfixes.
- Verified content and integration updates, with tracked operational issues and resolution notes.

### Website revamp: UI design and copy update

* fully qualified name: `ift-ts:web:status:2026q4-status-website:revamp-ui-copy`
* owner: Jinho/JulesFiliot
* status: not started
* start-date: 2026/10/05
* end-date: 2026/12/31

#### Description

Revamp the Status website UI and copy so they reflect the privacy focus of the app, based on requirements provided by Volodymyr.
Start with the homepage hero banners, then rewrite copy substantially, replace images, adjust the colour palette towards a calmer, privacy-oriented tone, and recompose page sections.
Reuse existing blocks (image and text, bullet lists) wherever possible, adding new blocks only when the requirements need them.
Make sure the revamped pages work well on mobile, including flows that are currently weak there, such as the Windows download popup.
Assess the requirements with stakeholders before implementation and agree a lighter scope if the workload proves too large for Q4.

#### Deliverables

- Assessed requirements for the homepage and other pages, with agreed scope and acceptance criteria.
- PRs implementing the new copy, images, colours, and section compositions, starting with the homepage hero.
- Desktop and mobile QA of the revamped pages and download flows, with stakeholder review results.

### Website revamp: Performance

* fully qualified name: `ift-ts:web:status:2026q4-status-website:revamp-performance`
* owner: Jinho/JulesFiliot
* status: not started
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Measure and improve Status website performance, building on the existing ping dashboards.
Evaluate content loading times across different locations for desktop and especially mobile, identify bottlenecks, and ship prioritized improvements.
Run this work progressively, in parallel with the UI revamp where capacity allows.

#### Deliverables

- Baseline loading-time measurements by location and device type.
- A prioritized list of identified performance issues.
- PRs for the improvements, with before and after measurements.

### Website revamp: Cleanup of unused pages

* fully qualified name: `ift-ts:web:status:2026q4-status-website:revamp-cleanup`
* owner: Jinho/JulesFiliot
* status: not started
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Simplify the Status website by removing old pages that are no longer relevant, keeping the site light.
Check each candidate page's organic search traffic and ranking before removal, keeping or updating pages that still matter for search.
Add redirects for removed pages where needed so existing links and search results do not break.

#### Deliverables

- An inventory of candidate pages with keep, update, or remove decisions agreed with stakeholders.
- PRs removing or updating pages, with redirects for removed routes.
- Verification that sitemap, internal links, and redirects work after cleanup.

### Website revamp: Translation

* fully qualified name: `ift-ts:web:status:2026q4-status-website:revamp-translation`
* owner: Jinho/JulesFiliot
* status: not started
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Translate the Status website into the six or seven languages currently supported by the Status app, once the new copy and site structure from the UI revamp are in place.
Review the current state of website localization support and complete any missing implementation, since the site currently serves English only.
Provide an English base file for translation; the first translation pass will be prepared in-house following the app's translation rules, such as keeping specified terms in English and keeping string lengths comparable so the UI does not break.
Translations will be reviewed internally, with Jinho proofreading Korean, and users will be invited to suggest improvements on GitHub.

#### Deliverables

- Working localization support on the website, with an English base file for translation.
- Translated content for the languages supported by the Status app, with internal review notes.
- Desktop and mobile QA of translated pages for layout and string-length issues.
- A visible link inviting community translation feedback on GitHub.

### Ad hoc features

* fully qualified name: `ift-ts:web:status:2026q4-status-website:ad-hoc-features`
* owner: Jinho/JulesFiliot
* status: not started
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Implement prioritized new Status website features requested during Q4, including new pages, marketing experiences, blog features, or integrations as requirements become clear.
Capture requests, agree scope and acceptance criteria with stakeholders, and schedule delivery according to priority and capacity.
Create dedicated roadmap tasks when a request grows into a substantial project.

#### Deliverables

- Scoped feature issues with acceptance criteria and stakeholder requirements.
- PRs and released features with validation or stakeholder review results.
