---

title: DST Automated Workflow
tags:
  - "2026q4"
  - "p2p"
  - "ift"
draft: false
description: Deploy nim-libp2p master to the Lab and report regression failures automatically

---

`ift-ts:p2p:ift:2026q4-dst-automated-workflow`

## Description

Automate deployments of the latest nim-libp2p master to the Lab and execute
basic regression tests. When results deviate from expected behavior, open an
issue automatically in the nim-libp2p repository for triage.

## Task List

### Lab Deployment And Regression Runs

* fully qualified name: `ift-ts:p2p:ift:2026q4-dst-automated-workflow:deployment-tests`
* owner: not assigned yet
* status: not started
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Deploy the latest master revision to the Lab and trigger basic regression
tests. Define expected outcomes and retain the tested revision, configuration,
and results so failures can be reproduced.

#### Deliverables

- Automated Lab deployment and basic regression workflow
- Documented expected results and retained run artifacts


### Automatic Regression Issues

* fully qualified name: `ift-ts:p2p:ift:2026q4-dst-automated-workflow:issue-reporting`
* owner: not assigned yet
* status: not started
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Compare regression results with expected outcomes and automatically create
nim-libp2p issues for deviations. Include the tested revision, failing checks,
and links to logs, and avoid repeatedly filing the same unresolved failure.

#### Deliverables

- Automatic issue creation for regression deviations
- Reproducible triage details and duplicate-issue handling
- Workflow checks demonstrating expected-result and regression-result paths
