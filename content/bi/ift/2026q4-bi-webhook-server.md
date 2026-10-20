---
title: BI Webhook Server
tags:
  - "2026q4"
  - "bi"
  - "ift"
draft: false
description: Assess Twitter API webhook support for stream and broadcast data and document a feasible extraction approach.
---

`ift-ts:bi:ift:2026q4-bi-webhook-server`

## Description

Assess whether Twitter API webhooks expose the stream and broadcast information needed by BI. Document available events, required access, and delivery limitations, then recommend an extraction approach.

## Task List

### Twitter webhook research

* fully qualified name: `ift-ts:bi:ift:2026q4-bi-webhook-server:twitter`
* owner: alexis
* status: in progress (10%)
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Check which stream and broadcast fields are available through Twitter API webhooks, which events provide them, and what API access is required. Record unsupported requirements and recommend webhooks or an alternative extraction approach based on the findings.

#### Deliverables
* A feasibility report mapping required stream and broadcast fields to available webhook events, access requirements, and delivery limitations.
* A documented extraction recommendation covering the proposed data flow and alternatives for requirements that webhooks cannot meet.
