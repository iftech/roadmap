---

title: Kademlia Auto-Mode Stability And Lifecycle Validation
tags:
  - "2026q4"
  - "p2p"
  - "ift"
draft: false
description: Validate Kademlia auto-mode stability and lifecycle behavior

---

`ift-ts:p2p:ift:2026q4-nimlibp2p-kademlia-auto-mode`

## Description

Automatic reachability-driven role selection and explicit client/server modes
were implemented in Q3 by
[nim-libp2p#2910](https://github.com/iftech/nim-libp2p/pull/2910). Auto mode starts
as a client, follows reachable/unreachable verdicts, and preserves its current
mode when reachability is unknown.

The current Kademlia handler immediately follows reachable/unreachable verdicts
and has no minimum observation window or cooldown. AutoNAT v1 aggregates a
bounded history of non-unknown answers (defaults: 10 answers, threshold 0.3),
with reachable taking priority when both outcomes meet the threshold. This is
sample-based aggregation, not a minimum stable duration. AutoNAT v2 uses
per-address verification: one selected peer supplies each address verdict, and
any confirmed candidate makes the node reachable. Its verification interval
controls probe cadence, not a Kademlia role-transition cooldown.

Add explicit transition timing safeguards and validate their interaction with
both reachability sources. Preserve fixed client/server modes and verify role
state and pending transitions across stop/restart.

Implementation baseline: nim-libp2p master at `5309dc87cb4b4385a4a37e4339cdeefca02c8667`:

- [Kademlia reachability handler](https://github.com/iftech/nim-libp2p/blob/5309dc87cb4b4385a4a37e4339cdeefca02c8667/libp2p/builders.nim#L585)
- [AutoNAT v1 answer aggregation](https://github.com/iftech/nim-libp2p/blob/5309dc87cb4b4385a4a37e4339cdeefca02c8667/libp2p/protocols/connectivity/autonat/service.nim#L93)
- [AutoNAT v2 address verification and reachability summary](https://github.com/iftech/nim-libp2p/blob/5309dc87cb4b4385a4a37e4339cdeefca02c8667/libp2p/address_manager.nim#L257)

## Task List

### Role-Transition Timing And Stability

* fully qualified name: `ift-ts:p2p:ift:2026q4-nimlibp2p-kademlia-auto-mode:stability`
* owner: not assigned yet
* status: not started
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Define and implement minimum observation windows and cooldowns for automatic
role changes, accounting for AutoNAT v1 answer aggregation and AutoNAT v2
per-address verdicts. Specify promotion and demotion timing so transient changes
do not cause repeated switching while sustained changes still take effect.

Define how opposite or unknown verdicts affect pending transitions. Include
inconclusive probes, which can retain prior reachability state rather than emit
an unknown verdict. Validate the policy through both AutoNAT integrations,
including loss of the last confirmed address in v2.

#### Deliverables

- Documented promotion/demotion windows, cooldowns, and pending-transition semantics
- Implemented timing safeguards for Kademlia auto mode
- Deterministic tests for transient and sustained verdict changes through AutoNAT v1 and v2
- Tests for unknown verdicts, inconclusive probes, and loss of the last confirmed address
- Checks that sustained reachability changes take effect within the documented timing bounds


### Fixed Modes And Service Lifecycle

* fully qualified name: `ift-ts:p2p:ift:2026q4-nimlibp2p-kademlia-auto-mode:lifecycle`
* owner: not assigned yet
* status: not started
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Verify that explicitly configured client and server modes remain fixed when
reachability changes. Exercise auto mode across service stop/restart, including
stopping while a role transition is pending. Ensure pending transitions cannot
fire after shutdown, restart uses the documented initial-state policy, and
subsequent reachability updates drive the expected role without duplicate
subscriptions. Fix defects identified by these tests.

#### Deliverables

- Tests for fixed client/server modes under changing reachability
- Auto-mode stop/restart tests covering pending-transition cancellation, subscriptions, and role state
- Fixes and regression coverage for lifecycle defects found during validation
