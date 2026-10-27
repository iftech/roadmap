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
* owner: Vlado
* status: in progress (53%)
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Deploy the latest master revision to the Lab and trigger basic regression
tests. Define expected outcomes and retain the tested revision, configuration,
and results so failures can be reproduced.

#### Deliverables

- Automated Lab deployment and basic regression workflow
- Documented expected results and retained run artifacts
- [iftech/nim-libp2p-network-lab#6](https://github.com/iftech/nim-libp2p-network-lab/pull/6) chore: better dummy experiments
- [iftech/nim-libp2p-network-lab#3](https://github.com/iftech/nim-libp2p-network-lab/pull/3) add dummy experiment
- [iftech/nim-libp2p-network-lab#2](https://github.com/iftech/nim-libp2p-network-lab/pull/2) improvements
- [iftech/nim-libp2p-network-lab#1](https://github.com/iftech/nim-libp2p-network-lab/pull/1) add project structure with initial nodes
- Completed scheduled workflow runs for the network lab.


### Automatic Regression Issues

* fully qualified name: `ift-ts:p2p:ift:2026q4-dst-automated-workflow:issue-reporting`
* owner: Vlado
* status: in progress (53%)
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
- [iftech/nim-libp2p-network-lab#9](https://github.com/iftech/nim-libp2p-network-lab/issues/9) Experiment failed: experiments/dummy-failure.yaml
- [iftech/nim-libp2p-network-lab#8](https://github.com/iftech/nim-libp2p-network-lab/issues/8) Experiment failed: experiments/dummy-failure.yaml
- [iftech/nim-libp2p-network-lab#7](https://github.com/iftech/nim-libp2p-network-lab/issues/7) Experiment failed: experiments/dummy-failure.yaml
- Added automatic issue creation for failed scheduled runs; successful runs do not create issues.
