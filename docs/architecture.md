# Architecture

## System boundary

```text
┌──────────────────────────────────────────────┐
│ AMD-backed autonomous AI workload            │
│ ROCm / AMD GPU execution                     │
└──────────────────────┬───────────────────────┘
                       │ proposed action
                       ▼
┌──────────────────────────────────────────────┐
│ UCII Authority Gateway                       │
│                                              │
│ 1. Authenticate / verify agent identity      │
│ 2. Bind request to authenticated actor       │
│ 3. Evaluate delegated authority              │
│ 4. Enforce scope / limits / expiry            │
│ 5. Produce allow or deny decision             │
└──────────────────────┬───────────────────────┘
                       │ authorized action only
                       ▼
┌──────────────────────────────────────────────┐
│ Deterministic Consequential Executor          │
└──────────────────────┬───────────────────────┘
                       │ result
                       ▼
┌──────────────────────────────────────────────┐
│ UCII provenance / judge-facing evidence       │
└──────────────────────────────────────────────┘
```

## Authority boundary

The AMD-backed model or agent is not an authority source. Model output is untrusted proposed intent until the independent UCII authorization boundary establishes permission.

The executor must not accept a consequential action solely because:

- the model generated it;
- the agent is technically capable of performing it;
- the agent identity is valid;
- a similar action previously succeeded;
- the request originated from AMD infrastructure.

## UCII boundary

This repository consumes UCII through its public SDK/API boundary. It does not copy private UCII implementation details or create an alternate trust root.

UCII remains responsible for the relevant identity, credential, authentication/verification, authorization/delegation, revocation, and provenance facts.

## AMD boundary

AMD technology must be materially involved in the autonomous workload. The final implementation should establish the exact AMD infrastructure and ROCm/runtime components from current ACT III requirements before coding begins.

AMD provides compute/execution capability. AMD infrastructure does not implicitly grant UCII authority.

## Consequential executor

The executor should be intentionally small and deterministic so a judge can distinguish AI reasoning from security enforcement. It should require valid authorization evidence before execution rather than merely receiving an advisory policy recommendation.

## Fail-closed behavior

Missing, expired, revoked, malformed, mismatched, or unverifiable authority must produce denial. Failure to verify identity or authority must not degrade into permissive execution.

## Provenance

The demo should retain enough attributable evidence to show:

- which UCII identity proposed the action;
- which action was requested;
- what authority state applied;
- why the request was allowed or denied;
- whether execution occurred;
- what changed between the successful and denied attempts.

Provenance records facts; it does not create authority.
