# UCII AMD Authority Agent

A UCII-governed autonomous AI agent on AMD infrastructure using cryptographic identity, bounded delegated authority, revocation, provenance, and safe execution for consequential actions.

## Core idea

The project demonstrates that an autonomous agent's ability to run on powerful AI infrastructure is not the same thing as possessing authority to perform consequential actions.

```text
Autonomous Agent / AI Workload
   ↓
AMD Infrastructure / ROCm-backed Execution
   ↓
Structured Proposed Action
   ↓
UCII Cryptographic Identity + Authority Gateway
   ↓
ALLOW / DENY
   ↓
Consequential Executor
   ↓
UCII Provenance
```

## Security model

The project keeps these domains separate:

**Capability ≠ Identity ≠ Authority ≠ Execution**

AMD provides the compute and AI execution environment. UCII independently governs who the agent is, what authority it currently has, whether that authority is bounded and still valid, and whether execution may proceed.

## Primary demo

1. An autonomous AI agent runs a real workload on AMD-backed infrastructure.
2. UCII verifies the agent's cryptographic identity.
3. The agent proposes a consequential action.
4. No matching delegated authority exists, so UCII denies execution.
5. A human grants tightly bounded authority for the action class, scope, amount/resource limit, and expiry.
6. The same agent proposes the same action and execution succeeds.
7. The delegated authority is revoked.
8. The same cryptographically verified agent attempts the action again and is denied.

The agent remains capable and cryptographically identified throughout. Only the authority state changes.

## Design principle

**Capability is not authority.**

The model or agent may propose actions. It cannot manufacture the authority needed to execute them.

## Planned stack

- AMD GPU infrastructure
- ROCm-compatible AI workload/runtime
- Python application layer
- UCII public SDK/API boundary
- Deterministic consequential tool executor
- Compact status UI or judge-facing evidence surface
- Verifiable provenance for authorization and execution decisions

## Repository purpose

This repository is the dedicated AMD Developer Hackathon ACT III competition and reference implementation for a UCII-governed autonomous-agent execution surface on AMD infrastructure. It is intentionally separate from the UCII core repository and from other environment-specific adapters.

See `docs/` for the detailed project contract, AMD integration requirements, architecture, implementation plan, judging strategy, demo plan, and submission checklist.
