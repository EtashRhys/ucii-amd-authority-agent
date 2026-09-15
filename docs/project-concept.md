# Project Concept

## Thesis

UCII AMD Authority Agent demonstrates an autonomous AI workload running on AMD infrastructure whose real-world execution remains independently governed by UCII.

The project is not "UCII hosted on AMD." AMD must provide a genuine AI/compute execution surface, while UCII provides a genuine cryptographic identity and authority boundary around consequential actions.

## Problem

Autonomous systems are increasingly capable of reasoning, using tools, consuming compute, modifying resources, and initiating external actions. Capability alone does not establish that an agent is the correct actor or that it has current permission to perform a particular action.

A model deciding that an action "looks safe" is not an authorization system.

## Proposed solution

Bind an autonomous AMD-backed agent/workload to UCII identity and require independently established UCII authority before a consequential executor accepts its proposed action.

The intended separation is:

**Capability ≠ Identity ≠ Authority ≠ Execution**

The AI system proposes. UCII authenticates and authorizes. The executor enforces.

## Canonical proof

The strongest demonstration uses one agent and one consequential action across changing authority states:

1. Agent is capable and UCII identity is verified.
2. No matching delegated authority exists.
3. Action is denied.
4. Human grants narrowly scoped delegated authority.
5. Same agent and same action are allowed.
6. Authority is revoked.
7. Same identity remains verified.
8. Same capability remains available.
9. Same action is denied again.

This proves that authorization is not being inferred from model capability, identity verification, or successful execution history.

## Durable UCII value

The competition project should leave behind a reusable AMD/ROCm autonomous-execution integration pattern for UCII. The artifact should remain valuable after the hackathon as evidence that UCII can govern autonomous workloads across heterogeneous compute environments.

## Non-goals

- Reimplementing UCII inside this repository.
- Treating AMD infrastructure as an authority source.
- Allowing an LLM to mint or expand its own authority.
- Building a broad generic agent platform before the canonical proof works.
- Adding unrelated SaaS dependencies merely to increase apparent complexity.
