---

title: Bounded GossipSub Validation
tags:
  - "2026q4"
  - "p2p"
  - "ift"
draft: false
description: Bound GossipSub validation concurrency and queued work

---

`ift-ts:p2p:ift:2026q4-nimlibp2p-gossipsub-validation`

## Description

Application validation can be expensive, for example when using RLN. Add global
and per-topic budgets, bounded admission queues, and validator deadlines so
validation work remains bounded under load. Keep invalid-message outcomes
separate from local overload.

## Task List

### Validation Budgets And Admission

* fully qualified name: `ift-ts:p2p:ift:2026q4-nimlibp2p-gossipsub-validation:budgets`
* owner: not assigned yet
* status: not started
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Implement global and per-topic concurrency limits, bounded admission queues,
and deadlines for validation work. Release capacity when work completes, expires,
or is cancelled.

#### Deliverables

- Configurable validation concurrency and queue limits
- Deadline handling and tests proving that capacity is released


### Topic Fairness And Outcomes

* fully qualified name: `ift-ts:p2p:ift:2026q4-nimlibp2p-gossipsub-validation:fairness-outcomes`
* owner: not assigned yet
* status: not started
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Schedule validation fairly across topics so a busy topic cannot monopolize
validation capacity. Distinguish invalid messages from work rejected or expired
because of local overload, without treating overload as evidence of invalid data.

#### Deliverables

- Fair scheduling across topics
- Separate invalid-message and local-overload outcomes
- Tests with expensive validators, saturated queues, and competing topics
