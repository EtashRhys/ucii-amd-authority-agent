# AMD Developer Hackathon ACT III — Requirements Ledger

## Status

This is a living requirements ledger. Reverify authoritative event rules immediately before implementation and again before submission. Do not treat stale marketing copy or remembered requirements as authoritative.

## Current planning facts

The project is being prepared for AMD Developer Hackathon ACT III. The current planning checkpoint records:

- participation mode: online;
- team: closed solo team `UCII Labs`;
- official online build period currently published as October 12–17, 2026;
- submission deadline currently published as October 18, 2026 at 15:00 UTC;
- intended technology: AMD GPU infrastructure / ROCm-backed autonomous AI workload;
- public GitHub project repository;
- final submission expected to include a working project and judge-facing presentation/demo materials.

All dates, tracks, required technologies, submission fields, infrastructure access, prize information, and prior-work rules must be reverified from current authoritative event material before relying on them.

## Prior-work / pre-build interpretation — REVERIFY BEFORE CODE

Current public event material establishes the official online build period, but the public pages reviewed so far do **not** establish an explicit blanket prohibition on all code written before October 12, 2026.

Until a more specific authoritative rule is published, use the conservative operating boundary below:

### Permitted pre-event preparation

Before October 12, prepare as much as possible without building the final competition-specific application implementation. This may include:

- architecture and system-boundary design;
- requirements research and compliance notes;
- repository scaffolding and documentation;
- threat modeling and adversarial test planning;
- UCII public API / SDK interface inspection;
- AMD Developer Cloud account and credit setup;
- ROCm / AMD Instinct learning and generic environment experiments;
- identification and evaluation of candidate AMD models, runtimes, and frameworks;
- generic reusable UCII-side components that are not created specifically as the ACT III submission;
- schemas and data-contract planning;
- deterministic executor design;
- judge-flow and demo storyboard planning;
- UI wireframes/mockups that are not wired into the final competition application;
- deployment/runbook planning and generic infrastructure templates;
- dependency and version research;
- preparation of test cases, acceptance criteria, and evidence requirements.

### Hold for the official build window unless rules explicitly permit earlier implementation

Do not implement the final ACT III submission-specific system before the official build window unless authoritative rules clearly allow it. Hold at minimum:

- the final ACT III autonomous agent/workload implementation;
- the final AMD-to-UCII authority integration;
- the competition-specific consequential executor;
- the judge UI wired to the live competition system;
- the completed end-to-end denial → grant → execute → revoke → denial demonstration;
- submission-specific deployment and final integrated demo application.

### Governing principle

**Maximize pre-event preparation; reserve competition-specific implementation for the official build window unless authoritative rules explicitly permit earlier implementation.**

The purpose is to arrive at kickoff with decisions, infrastructure, compliance, tests, interfaces, and demo design already settled, while preserving a clean eligibility boundary around competition-specific implementation.

## Mandatory rules-page recheck gate

Before any competition-specific application code is written, recheck the current authoritative AMD/Lablab ACT III event page, rules, FAQ, terms, track descriptions, and any newly published prior-work or eligibility language.

Record the result in this file before implementation begins.

The recheck must answer at minimum:

- [ ] Does the event prohibit code written before kickoff?
- [ ] Does it permit pre-existing libraries, frameworks, or project components?
- [ ] Must all submission-specific code be created during the official build period?
- [ ] Are substantial updates to pre-existing projects permitted?
- [ ] Are there disclosure requirements for prior work or reused components?
- [ ] Have tracks been announced?
- [ ] Have required AMD technologies or runtime constraints changed?
- [ ] Have submission or judging requirements changed?

If the authoritative rules conflict with this planning interpretation, the authoritative rule wins immediately.

## Previously identified submission shape — REVERIFY

Prior event inspection indicated a submission could require or benefit from:

- project title and descriptions;
- tags;
- cover image;
- demo video;
- slide presentation;
- public GitHub repository;
- demo/application URL or platform information.

Do not mark these final until current rules are checked.

## Previously identified judging dimensions — REVERIFY

- Application of Technology
- Presentation
- Business Value
- Originality

## Engineering compliance gate

Before code is written, record authoritative answers for:

- [ ] Exact submission deadline and timezone
- [ ] Current tracks
- [ ] Required AMD technologies
- [ ] Allowed infrastructure/runtime choices
- [ ] AMD Developer Program requirements
- [ ] Team/solo eligibility
- [ ] Public repository requirements
- [ ] License requirements, if any
- [ ] Demo/video requirements and duration
- [ ] Presentation requirements
- [ ] Working application/demo access requirements
- [ ] Judging criteria
- [ ] Product feedback requirements, if any
- [ ] Infrastructure credit/quota constraints
- [ ] Any AI/model disclosure requirements
- [ ] Prior-work / pre-existing-code rules

## Rule

If an event requirement conflicts with this repository's planning documents, the current authoritative competition rule wins and this ledger must be updated before implementation proceeds.
