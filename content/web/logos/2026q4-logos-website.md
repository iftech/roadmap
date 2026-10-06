---
title: Logos Website
tags:
  - "2026q4"
  - "web"
  - "logos"
draft: false
description: Maintain the Logos website, deliver Comms-requested landing pages and campaign experiences, and implement prioritized ad hoc features.
---

`ift-ts:web:logos:2026q4-logos-website`

## Description

Continue supporting the Logos website in Q4 through recurring upkeep, fixes and improvements to existing functionality, and delivery of new features requested during the quarter.
Build on the pages, release information, forms, and newsletter flows delivered in Q3.
Deliver the Q4 landing pages and campaign experiences requested by the Logos Comms team, including the Node Program, Basecamp, RFP and Lambda Prize, Parallel Societies, Thesis Phase 3, and End of Year Recap work.
Select concrete work with stakeholders as needs arise and record the scope and acceptance criteria in linked issues.

## Task List

### Maintenance

- fully qualified name: `ift-ts:web:logos:2026q4-logos-website:maintenance`
- owner: Jinho/JulesFiliot
- status: done
- start-date: 2026/10/01
- end-date: 2026/10/06

#### Description

Keep the Logos website and its existing integrations working as dependencies, content, and releases change.
Handle recurring content updates requested by the Comms team, including testnet updates, legal page changes, homepage message testing, and image replacements.
Maintain site-specific dependencies and configuration, release and download links, forms, newsletter flows, and deployment health.
Investigate production failures and ship necessary hotfixes, coordinating shared tooling changes with the Web maintenance commitment.

#### Deliverables
- [logos-co/logos-web#193](https://github.com/logos-co/logos-web/pull/193) feat(web): testnet v0.3 launch content updates
- [logos-co/logos-web#203](https://github.com/logos-co/logos-web/pull/203) feat(web): testnet v0.3 legal pages and links
- [logos-co/logos-web#205](https://github.com/logos-co/logos-web/pull/205) fix: update Basecamp platform downloads to 0.3.1
- [logos-co/logos-web#184](https://github.com/logos-co/logos-web/pull/184) Publish the site from the CMS
- [logos-co/logos-web#189](https://github.com/logos-co/logos-web/issues/189) Repo is 2.5 GB because build output is committed to deploy branches
- [status-im/infra-sites#171](https://github.com/status-im/infra-sites/issues/171) chore(logos.co): drop git history from deploy-* branches on each build
- [logos-co/logos-web#191](https://github.com/logos-co/logos-web/pull/191) chore(web): remove unused about mountain video

### Past Present Future: content update and migration

- fully qualified name: `ift-ts:web:logos:2026q4-logos-website:past-present-future`
- owner: Jinho
- status: done
- start-date: 2026/10/01
- end-date: 2026/10/06

#### Description

Continue the Past Present Future work with the Comms team following the Mike experience.
Turn agreed content updates into an implementation-ready plan, including copy, calls to action, journey changes, media, and supporting assets.
Migrate the approved experience and its assets into the existing `logos-web` repository so it can be maintained, deployed, and measured alongside the main Logos website.
Preserve working routes, responsive behaviour, Umami tracking, and event naming through the migration.

Coordinate with the agency when content, creative assets, interaction design, or technical handover requires their input.
Document ownership, dependencies, and acceptance criteria before work that crosses the Comms, agency, and web teams begins.

#### Deliverables

- A prioritised, approved content and asset update list for the post-Mike experience, with owners and acceptance criteria.
- Migration PRs in `logos-web` for the approved experience, routes, assets, responsive behaviour, and analytics integration.
- Desktop and mobile QA covering key journeys, calls to action, video presentation, and Umami event tracking.
- Agency handover and review notes for any work requiring external creative or technical collaboration.
- [logos-co/logos-web#194](https://github.com/logos-co/logos-web/pull/194) feat(web): add Amanda film to past-present-future

### Logos Zine

- fully qualified name: `ift-ts:web:logos:2026q4-logos-website:logos-zine`
- owner: JulesFiliot
- status: not started
- start-date: 2026/10/12
- end-date: 2026/12/31

#### Description

Deliver the initial Logos Zine page described in [logos-web#172](https://github.com/logos-co/logos-web/issues/172), at `logos.co/zine`.
The first release will list the available issue or issues and provide PDF downloads, while keeping the content structure flexible for future issues.
It will be responsive on desktop and mobile, but will not include a web-based reader in this phase.

Before implementation, collect the final PDF, approved copy and assets, and a design wireframe or reference sites from stakeholders.

#### Deliverables

- A responsive `logos.co/zine` page listing the current issue and supporting additional issues without a page redesign.
- A verified PDF download for each published issue.
- Final copy, PDF, assets, and design references documented before implementation.
- QA evidence for desktop and mobile presentation, issue links, and downloads.

### Node Program landing page

- fully qualified name: `ift-ts:web:logos:2026q4-logos-website:node-program-lp`
- owner: Jinho/JulesFiliot
- status: not started
- start-date: 2026/10/01
- end-date: 2026/10/31

#### Description

Design and build a new landing page to launch the Node Referral Program, covering program details, how to join, and the resources participants need.
This is a large page, so kick off requirements, copy, and design with the Comms team at the start of October.

#### Deliverables

- Approved page structure, copy, and design for the Node Referral Program.
- A responsive landing page on `logos.co` with join flow links and participant resources.
- Desktop and mobile QA, plus Umami tracking on key calls to action.

### Basecamp landing page revamp

- fully qualified name: `ift-ts:web:logos:2026q4-logos-website:basecamp-lp`
- owner: Jinho
- status: in progress (10%)
- start-date: 2026/10/01
- end-date: 2026/10/31

#### Description

Fully redesign the Basecamp landing page based on feedback about the current version.
Make the page more explanatory, expand its content, and focus it on conversion.

#### Deliverables

- A summary of the collected feedback and the redesign goals agreed with Comms.
- Approved redesign and copy.
- A rebuilt, responsive Basecamp page with conversion events tracked in Umami.
- [logos-co/logos-web#112](https://github.com/logos-co/logos-web/issues/112) Install Basecamp is throught web wrongly implemented

### RFP and Lambda Prize landing page updates

- fully qualified name: `ift-ts:web:logos:2026q4-logos-website:rfp-lambda-prize-lp`
- owner: Jinho/JulesFiliot
- status: not started
- start-date: 2026/11/01
- end-date: 2026/11/30

#### Description

Revisit the RFP and Lambda Prize pages to support the new focus on developer programs, making them more informative and conversion driven.
Audit the current pages and agree a design strategy with Comms before starting the redesign.

#### Deliverables

- An audit of the current RFP and Lambda Prize pages and an agreed design strategy.
- Updated, responsive RFP and Lambda Prize pages based on that strategy.
- QA and Umami tracking on the developer program calls to action.

### Parallel Societies campaign landing page

- fully qualified name: `ift-ts:web:logos:2026q4-logos-website:parallel-societies-lp`
- owner: Jinho/JulesFiliot
- status: not started
- start-date: 2026/11/01
- end-date: 2026/11/30

#### Description

Build an informational campaign page that showcases events and live operations across the ecosystem and explains the "Parallel Societies" idea through a recap of past events.
The page links out to other properties, such as Luma, for details. It is not meant to drive registrations.

#### Deliverables

- Approved copy, event list, and media for past Parallel Societies events.
- A responsive campaign page with outbound links to event properties.
- Desktop and mobile QA.

### Thesis Phase 3 deployment

- fully qualified name: `ift-ts:web:logos:2026q4-logos-website:thesis-phase-3`
- owner: Jinho
- status: not started
- start-date: 2026/11/01
- end-date: 2026/11/30

#### Description

Deploy the new web experience for the final stage of the Thesis campaign. The Hype agency is building and testing it.
Hype also owns the content updates to Past Present Future (see the Past Present Future task). This task covers receiving the packaged code, deploying it, and verifying it in production.
Agree on the handover format, hosting and routes, analytics requirements, and the launch date with Hype and Comms before November.

#### Deliverables

- An agreed handover checklist covering package format, routes, environment, and analytics.
- The Phase 3 experience deployed to production on its agreed route or domain.
- Post-deploy checks on desktop and mobile, routing, and tracking.

### End of Year Recap campaign

- fully qualified name: `ift-ts:web:logos:2026q4-logos-website:eoy-recap`
- owner: Jinho/JulesFiliot
- status: not started
- start-date: 2026/11/01
- end-date: 2026/12/31

#### Description

Deliver an interactive web experience that walks through the full Logos thesis to close out the year.
Design and production ownership (in-house or agency) is still to be decided. Confirm scope, ownership, and timeline with Comms in early November.

#### Deliverables

- An agreed scope, production approach, and timeline.
- An approved design and narrative structure.
- The interactive recap experience, launched and QA'd on desktop and mobile.

### Ad hoc features

- fully qualified name: `ift-ts:web:logos:2026q4-logos-website:ad-hoc-features`
- owner: Jinho/JulesFiliot
- status: not started
- start-date: 2026/10/01
- end-date: 2026/12/31

#### Description

Implement prioritized new Logos website features requested during Q4, including new pages, campaign experiences, forms, or integrations as requirements become clear.
Capture requests, agree scope and acceptance criteria with stakeholders, and schedule delivery according to priority and capacity.
Create dedicated roadmap tasks when a request grows into a substantial project.

#### Deliverables

- Scoped feature issues with acceptance criteria and stakeholder requirements.
- PRs and released features with validation or stakeholder review results.
