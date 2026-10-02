---

title: Nimbus Testnet Deployment
tags:
  - "2026q4"
  - "p2p"
  - "ift"
draft: false
description: Automate the deployment of a nim-libp2p change to Nimbus testnet nodes, with the start time and duration set by the p2p team

---

`ift-ts:p2p:ift:2026q4-nimlibp2p-nimbus-downstream-ci`

## Description

Today a deployment of a nim-libp2p change to a testnet node is manual.
The automation builds Nimbus with the nim-libp2p commit, deploys it to testnet nodes, collects metrics, restores the nodes, and reports the result.
The p2p team operates the levers of each run.

The workflow deploys any nim-libp2p commit.
A pull request with the `test-nimbus` label gets a build for each new commit.
A team member can also start a run on a standalone commit, e.g. a master commit or a commit on a branch with no pull request.

## Task List

### Nimbus Build For A nim-libp2p Commit

* fully qualified name: `ift-ts:p2p:ift:2026q4-nimlibp2p-nimbus-downstream-ci:build`
* owner: not assigned yet
* status: not started
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Each nim-libp2p commit to test gets its own nimbus-eth2 branch.
A pull request with the `test-nimbus` label uses `nim-libp2p-test-pr-<number>`, and a standalone commit uses `nim-libp2p-test-<short-hash>`.
Set `vendor/nim-libp2p` to the commit.
Read the dependency pins in `libp2p.nimble` and move each matching nimbus-eth2 `vendor/` submodule to that pin, because nimbus-eth2 ignores `libp2p.nimble`.
Build the beacon node from this branch.
Delete a pull request branch when the pull request closes or the `test-nimbus` label is removed.
Delete a standalone commit branch when its run ends.

#### Deliverables

- A beacon node binary for each pull request with the `test-nimbus` label
- A beacon node binary on request for any standalone commit
- Builds for different commits that run in parallel, with no change to `DEPENDENCIES_AUTOBUMP_ENABLED`
- Branch cleanup on pull request close and at the end of a standalone run


### Testnet Deployment Automation

* fully qualified name: `ift-ts:p2p:ift:2026q4-nimlibp2p-nimbus-downstream-ci:deployment`
* owner: not assigned yet
* status: not started
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Add a workflow that deploys the beacon node binary of a nim-libp2p commit to testnet nodes.
The workflow takes a commit hash or a pull request number, the start time, and the duration as inputs.
The workflow resolves a pull request number to the head commit of the pull request.
A commit hash needs no pull request and no label.
At the end of the desired duration, the workflow restores the previous binary on each node.
A lock on each node stops two runs from using the same node.
The team can stop a run before its end, and the workflow then restores the nodes at once.

#### Deliverables

- A deployment workflow with commit or pull request, start time, and duration inputs
- Automatic restore of the nodes at the end of a run or on stop
- A node lock that prevents overlapping runs
- Contributor documentation for how to start, schedule, and stop a run


### Metrics And Reporting

* fully qualified name: `ift-ts:p2p:ift:2026q4-nimlibp2p-nimbus-downstream-ci:reporting`
* owner: not assigned yet
* status: not started
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Run a baseline node on nim-libp2p master next to the deployed nodes.
Collect the libp2p and beacon node metrics from the deployed nodes and the baseline for the duration of the run.
Compare peer count, connection churn, gossipsub message delivery, block and attestation arrival delay, sync status, CPU, and memory.
Post the comparison on the pull request, with links to the node logs and dashboards.
For a standalone commit, write the comparison to the workflow run summary.

#### Deliverables

- A baseline node on nim-libp2p master
- A metrics comparison between the deployed nodes and the baseline for each run
- A run report on the pull request, or in the workflow run summary for a standalone commit, with logs and dashboards
