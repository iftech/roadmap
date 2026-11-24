---
title: DST Tooling
tags:
  - "2026q4"
  - "dst"
  - "ift"
draft: false
description: "Creating tools that allow
DST to easily work with other IFT projects.
This includes functionalities such as deployments,
monitoring, analysis, and control of aforementioned software's."
---

`ift-ts:dst:ift:2026q4-dst-tooling`

## Description

We will create tools to help DST efficiency.
These tools can be composed of utilities for Kubernetes,
or any other kind that fits the necessities of DST and other projects.
As projects might share common necessities, this tasks will be considered
as a scaffold for DST tools, adapting the tools for each project if it needs.
The primary focus will be on adapting the necessities of the Waku team for
the log parser tool. This will comprise retrieving information from a given
message id, history of discovered peers, subscriptions, while having good 
performance and supportability.
Additionally, the project will define workflows that facilitate the creation
and execution of specialized scenarios. These scenarios will assist in 
the analysis of libp2p and Gossipsub, supporting studies focused on 
adversarial conditions and control message behavior.


## Task list

### General tooling (recurring)

* fully qualified name: `ift-ts:dst:ift:2026q4-dst-tooling:general-tooling`
* owner: Alberto/Alan
* status: in progress (50%)
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description
Group of utilities that are added to the main repository.
Should be made general when possible.

#### Deliverables
- Code:
    - [iftech/roadmap#530](https://github.com/iftech/roadmap/pull/530) chore(DST): q4 commitments
    - [iftech/10ksim#391](https://github.com/iftech/10ksim/pull/391) Scrape metrics and draw the standard plots in post-run analysis
    - [iftech/10ksim#421](https://github.com/iftech/10ksim/pull/421) Look up the publisher once per run, not per message
    - [iftech/10ksim#442](https://github.com/iftech/10ksim/pull/442) Fix cleanup wait and CronJob cleanup
    - [iftech/dst-libp2p-test-node#63](https://github.com/iftech/dst-libp2p-test-node/pull/63) Shadow build for the two-binary regression node
    - [iftech/10ksim#444](https://github.com/iftech/10ksim/pull/444) Fix the Shadow log pull and the exit code of a failed Shadow run
    - [iftech/10ksim#453](https://github.com/iftech/10ksim/pull/453) Fail a run that published off its configured rate
    - [Publish each run's metrics to the DST dashboard](https://github.com/iftech/10ksim/pull/457)
    - [Read a run's metrics back from the DST dashboard](https://github.com/iftech/10ksim/pull/458)
    - [Publish a run's logs, whole-run node metrics and specs to the dashboard](https://github.com/iftech/10ksim/pull/462)
    - [Dashboard: fail on datasets without rows, guard clears](https://github.com/iftech/10ksim/pull/459)
    - [Dashboard manifests: match what runs, dev Mongo to ClusterIP](https://github.com/iftech/10ksim/pull/460)
- Reports:
- Other:
    - Added an interactive message-propagation view for nim-libp2p runs.
    - Deployed the updated DST dashboard backend with storage and retrieval of run metrics, logs and deployment specifications.
    - Moved lab system-service deployments to the main branch of vaclab-2.
