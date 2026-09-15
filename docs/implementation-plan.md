# Implementation Plan

## Workflow

Use a bounded engineering cadence throughout:

**inspect → reason → one bounded change → targeted verification → diff/review → commit → checkpoint**

Do not build several speculative layers at once.

## Objective 0 — Reverify competition contract

Before application code:

- verify current ACT III dates and submission requirements;
- verify current AMD technical/runtime requirements;
- verify tracks when announced;
- identify the smallest genuine AMD workload;
- record any infrastructure, quota, or judging-access constraints.

Acceptance: the project can state precisely why its AMD integration qualifies and how it will be demonstrated.

## Infrastructure readiness — AMD Developer Cloud credit

Status: **REQUEST SUBMITTED / AWAITING VALIDATION**

On 2026-09-14, the AMD AI Developer Program cloud-credit request was submitted for **AMD Developer Cloud — Direct GPU Access**.

Requested use: run and evaluate the UCII AMD Authority Agent autonomous AI workload on AMD Instinct GPU infrastructure using ROCm-compatible frameworks, with UCII independently providing cryptographic identity, bounded delegated authority, revocation, and verifiable provenance around consequential actions.

AMD's confirmation page stated:

- account validation is required before activation;
- activation instructions are expected by email within 3 business days;
- approvals may be delayed due to high demand;
- if credits have not arrived within 5 business days, contact `devcloudrequests@amd.com`;
- new AMD Developer Cloud users should log in with AMD SSO credentials to activate their cloud account;
- the member-perks page states the introductory AMD Developer Cloud credit is **$100** and expires **30 days after activation**.

Operational rule: do not treat the credit as available until AMD sends activation instructions and the credit is confirmed active. Avoid starting the 30-day activation window earlier than needed for the build.

## Objective 1 — Minimal AMD workload

Create the smallest reproducible autonomous AI workload that genuinely executes on AMD-backed infrastructure/ROCm and can emit one structured proposed action.

Acceptance: AMD usage is independently demonstrable without UCII authorization logic yet.

## Objective 2 — UCII identity binding

Bind the workload/agent to a real UCII identity through the public UCII boundary.

Acceptance: the proposed action can be attributed to the authenticated/verified UCII actor without granting execution authority.

## Objective 3 — Fail-closed authorization boundary

Route the proposed consequential action through the UCII authority gateway.

Acceptance: verified identity + capability + proposed action + no matching authority = DENY, with no consequential execution.

## Objective 4 — Bounded grant and successful execution

Establish a human-authorized delegated grant with explicit scope and expiry/limits appropriate to the selected action.

Acceptance: the same agent and same action succeed only while matching authority is valid.

## Objective 5 — Revocation proof

Revoke the delegated authority and perform a fresh authorization check.

Acceptance: same verified identity + same capability + same proposed action + revoked authority = DENY.

## Objective 6 — Provenance and evidence surface

Expose enough evidence for a judge to understand identity, proposed action, authority state, authorization decision, execution result, and revocation transition.

Acceptance: the canonical proof is understandable without reading the entire codebase.

## Objective 7 — Adversarial validation

Test at minimum:

- missing authority;
- expired authority;
- revoked authority;
- wrong actor;
- wrong action/scope;
- replay/stale evidence where applicable;
- model output attempting to claim or expand authority;
- AMD workload failure;
- UCII verification/authorization failure.

Acceptance: consequential execution fails closed.

## Objective 8 — Judge-ready demonstration

Create a compact repeatable demonstration of the canonical sequence and ensure setup can be reproduced from the public repository.

## Objective 9 — Submission package

Complete README, architecture, source, tests, friction log, product feedback, screenshots/cover material, presentation, demo video, application URL if required, and final rule compliance review.

## Scope control

Do not expand into a generic agent platform until the denial → grant → execute → revoke → denial proof is complete and verified.
