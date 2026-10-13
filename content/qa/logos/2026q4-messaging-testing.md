---
title: Messaging Testing
tags:
  - "2026q4"
  - "qa"
  - "logos"
draft: false
description: Maintain messaging testing frameworks and continue migrating interop tests into Logos Delivery.
---

`ift-ts:qa:logos:2026q4-messaging-testing`

## Description

Continue improving messaging test reliability by maintaining existing frameworks and migrating the remaining interop tests into the Logos Delivery repository.
Adapt tests to messaging component changes, address regressions, and keep coverage useful as the implementation evolves.

## Task List

### Interop migration

* fully qualified name: `ift-ts:qa:logos:2026q4-messaging-testing:interop-migration`
* owner: Florin/Radek
* status: done
* start-date: 2026/10/01
* end-date: 2026/10/13

#### Description

Continue the Q3 migration of messaging interop tests into the Logos Delivery repository.
Port the remaining scenarios to the repository's E2E workflow, preserve relevant protocol coverage, and resolve failures or gaps exposed by the migration.

#### Deliverables
- [logos-messaging/logos-delivery#4335](https://github.com/logos-messaging/logos-delivery/pull/4335) test(e2e): cleanup harness code (migration 14)
- [logos-messaging/logos-delivery#4348](https://github.com/logos-messaging/logos-delivery/pull/4348) test(e2e): rename the wrapper suite to c_abi (migration 15)
- [logos-messaging/logos-delivery#4350](https://github.com/logos-messaging/logos-delivery/pull/4350) test(e2e): run the C ABI suite in parallel and make its xfailed tests pass (migration 16)
- [logos-messaging/logos-delivery#4353](https://github.com/logos-messaging/logos-delivery/pull/4353) test(e2e): python binding as a submodule (migration 17)
- [logos-messaging/logos-delivery-python-bindings#9](https://github.com/logos-messaging/logos-delivery-python-bindings/pull/9) chore: bump logos-delivery and move the wrapper to the CBOR ABI
- [status-im/status-go#7816](https://github.com/status-im/status-go/pull/7816) ci: test Logos Delivery nightly and issue reporting in Jenkins
- [logos-messaging/logos-delivery#4422](https://github.com/logos-messaging/logos-delivery/pull/4422) test: include orphaned suites

### Maintenance

* fully qualified name: `ift-ts:qa:logos:2026q4-messaging-testing:maintenance`
* owner: Radek
* status: in progress (25%)
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Provide ongoing maintenance of messaging testing frameworks.
Update tests for messaging component changes, investigate failing or flaky tests, address regressions, and make minor framework improvements needed to keep the suites reliable.

#### Deliverables
- [logos-messaging/logos-delivery#4368](https://github.com/logos-messaging/logos-delivery/pull/4368) ci: cache nim, nimble and nimcache (ci improvements 1)
- [logos-messaging/logos-delivery#4379](https://github.com/logos-messaging/logos-delivery/pull/4379) test: configurable waiting times (ci improvements 2)
- [logos-messaging/logos-delivery#4395](https://github.com/logos-messaging/logos-delivery/pull/4395) test: wait on conditions instead of fixed sleeps (ci improvements 3)
- [logos-messaging/logos-delivery#4420](https://github.com/logos-messaging/logos-delivery/pull/4420) ci: test reporter
- [logos-messaging/logos-delivery#4463](https://github.com/logos-messaging/logos-delivery/pull/4463) test(e2e): fix flaky test_s31_concurrent_sends_mixed_topics_during_churn
- [logos-messaging/logos-delivery#4439](https://github.com/logos-messaging/logos-delivery/pull/4439) test: bug reproductions
- [logos-messaging/logos-delivery#4459](https://github.com/logos-messaging/logos-delivery/pull/4459) test: bug reproductions 2
- [logos-messaging/logos-delivery#4438](https://github.com/logos-messaging/logos-delivery/issues/4438) bug: the archive counts a message it already holds as written on Postgres and as an insert failure on sqlite
- [logos-messaging/logos-delivery#4437](https://github.com/logos-messaging/logos-delivery/issues/4437) question: GET /store/v3/messages reads a startTime or endTime of 0 or less as absent, and a negative pageSize as the maximum
- [logos-messaging/logos-delivery#4436](https://github.com/logos-messaging/logos-delivery/issues/4436) question: any --rate-limit entry replaces the default rate limits, so filter falls to 30/1m and unnamed protocols run without a limit
- [logos-messaging/logos-delivery#4435](https://github.com/logos-messaging/logos-delivery/issues/4435) question: filter UNSUBSCRIBE of a criterion the requester does not hold answers 200 or 404 depending on other peers, and its 404 can follow a partial removal
- [logos-messaging/logos-delivery#4434](https://github.com/logos-messaging/logos-delivery/issues/4434) bug: /filter/v2/subscriptions answers 200 "UNKNOWN" without pubsubTopic under static sharding, and its message cache ignores the result
- [logos-messaging/logos-delivery#4432](https://github.com/logos-messaging/logos-delivery/issues/4432) bug: REST API answers an undecodable JSON body without the decoder's reason
- [logos-messaging/logos-delivery#4431](https://github.com/logos-messaging/logos-delivery/issues/4431) bug: /lightpush/v3/message answers 500 for INVALID_MESSAGE (420), and 413 or 500 for the same oversize message
- [logos-messaging/logos-delivery#4433](https://github.com/logos-messaging/logos-delivery/issues/4433) question: lightpush v3 client turns the service's BAD_REQUEST for an undecodable request into "response failure, requestId mismatch"
- [logos-messaging/logos-delivery#4457](https://github.com/logos-messaging/logos-delivery/issues/4457) bug: POST /relay/v1/subscriptions joins a shard of another cluster or past --num-shards-in-network, and the node's metadata then misreports its shards
- [logos-messaging/logos-delivery#4456](https://github.com/logos-messaging/logos-delivery/issues/4456) question: DELETE /relay/v1/auto/subscriptions of one content topic unsubscribes its whole shard, silencing the other content topics on it
- [logos-messaging/logos-delivery#4455](https://github.com/logos-messaging/logos-delivery/issues/4455) question: under autosharding --shard does not limit which shards the relay joins, yet the REST cache and --protected-shard still follow it
- [logos-messaging/logos-delivery#4454](https://github.com/logos-messaging/logos-delivery/issues/4454) question: --cluster-id=2 applies the logos.dev preset, whose nodes are on cluster 3, and replaces an explicit --preset=logos.test
- [logos-messaging/logos-delivery#4453](https://github.com/logos-messaging/logos-delivery/issues/4453) bug: a duplicate a node publishes goes through its own relay handlers again, and is answered as NoPeersToPublish
- [logos-messaging/logos-delivery#4485](https://github.com/logos-messaging/logos-delivery/issues/4485) bug: with a raised --max-msg-size, store sync never transfers a message above 150 KiB, and a few such messages stop the node's transfers to every peer
- [logos-messaging/logos-delivery#4484](https://github.com/logos-messaging/logos-delivery/issues/4484) bug: a node that gets SIGTERM while store sync transfers messages to a peer never finishes stopping and is killed
- [logos-messaging/logos-delivery#4486](https://github.com/logos-messaging/logos-delivery/issues/4486) bug: a message encoded within --max-msg-size is not relayed or stored when the encoded RPC message gossipsub would send exceeds the limit, and the publish routes answer 200 or "no peers"
- [logos-messaging/logos-delivery#4483](https://github.com/logos-messaging/logos-delivery/issues/4483) bug: store sync transfer writes the pubsub topic as field 1 and the message as field 2, the reverse of the WAKU-SYNC specification
- [logos-messaging/logos-delivery#4482](https://github.com/logos-messaging/logos-delivery/issues/4482) bug: --preset=status.prod runs the 150KiB default of --max-msg-size instead of the 1024KiB of the preset, and warns at every start that the size was provided
- [logos-messaging/logos-delivery#4481](https://github.com/logos-messaging/logos-delivery/issues/4481) bug: a peer that connects in while the node's own dial to it is in flight stays CannotConnect for as long as it is connected
- [logos-messaging/logos-delivery#4480](https://github.com/logos-messaging/logos-delivery/issues/4480) question: /admin/v1/peers lists a peer that dialled in over TCP at its connection's source port, where nothing listens
