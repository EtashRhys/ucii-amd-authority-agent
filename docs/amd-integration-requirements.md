# AMD Integration Requirements

## Purpose

This file defines the engineering gate for claiming AMD integration. It is intentionally conservative until the current AMD Developer Hackathon ACT III technical requirements, tracks, and available infrastructure are reverified from authoritative event material.

## Required integration principle

The final project must use AMD technology as a real runtime or workload dependency. Merely mentioning AMD, deploying an otherwise unchanged UCII service beside AMD infrastructure, or adding AMD branding is insufficient for this project's technical goal.

## Intended technical role

The current design targets:

- an AI workload executing on AMD GPU infrastructure;
- a ROCm-compatible runtime or framework where applicable;
- autonomous reasoning or workload output that produces a structured proposed action;
- a UCII authorization boundary that remains independent of the model/runtime;
- an executor that accepts only appropriately authorized actions.

## Pre-implementation verification gate

Before choosing libraries, model runtime, cloud image, GPU class, or deployment topology, verify and record:

1. Current ACT III official technical requirements.
2. Current AMD infrastructure made available to participants.
3. Required or eligible AMD SDKs, ROCm components, APIs, or developer services.
4. Track-specific requirements once tracks are announced.
5. Submission and public-repository requirements.
6. Any usage, credit, quota, or judging-access constraints.

Do not manufacture missing event requirements from assumptions.

## Evidence expected for final submission

The repository and demo should make AMD usage independently understandable through source code, configuration, runtime evidence, documentation, and the demonstration itself.

## UCII separation

AMD infrastructure supplies execution capability. UCII supplies the identity/authority control plane. Neither side silently substitutes for the other.
