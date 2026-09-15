# Canonical Demo Script

## Purpose

Prove that an autonomous agent's capability and cryptographic identity can remain constant while its permission to execute changes independently.

## Scene 1 — Establish AMD-backed capability

Show the autonomous AI workload running on the selected AMD/ROCm environment. Establish the same agent/workload that will be used for every subsequent attempt.

## Scene 2 — Verify identity

Show UCII cryptographically verifying the agent identity.

Visible state:

```text
AGENT IDENTITY: VERIFIED
AUTHORITY: NONE
```

## Scene 3 — First consequential attempt

The agent produces a structured proposed action.

Example action class (final action to be chosen during implementation):

```text
resource.allocate
scope: demo-workload
limit: bounded
```

UCII performs a fresh authority check.

Expected result:

```text
IDENTITY: VERIFIED
AUTHORITY: NOT ESTABLISHED
DECISION: DENY
EXECUTION: NOT PERFORMED
```

## Scene 4 — Human grants bounded authority

Grant only the authority required for the selected action. The final grant should visibly demonstrate meaningful constraints such as actor, action class, scope, resource/amount limit, expiry, and/or one-shot semantics where appropriate.

## Scene 5 — Repeat the same action

The same agent proposes the same action.

Expected result:

```text
IDENTITY: VERIFIED
AUTHORITY: VALID / MATCHING
DECISION: ALLOW
EXECUTION: PERFORMED
```

Show the deterministic execution result.

## Scene 6 — Revoke

Revoke the delegated authority without destroying or invalidating the agent identity.

Visible state:

```text
IDENTITY: VERIFIED
AUTHORITY: REVOKED
```

## Scene 7 — Third attempt

The same agent proposes the same action again. Perform a fresh UCII authorization check.

Expected result:

```text
IDENTITY: VERIFIED
AUTHORITY: REVOKED / NOT VALID
DECISION: DENY
EXECUTION: NOT PERFORMED
```

## Scene 8 — Provenance proof

Show the attributable sequence:

```text
verified identity
→ denied without authority
→ bounded human grant
→ authorized execution
→ revocation
→ denied after revocation
```

## Closing line

> Same agent. Same AMD capability. Same verified identity. Different authority state — different execution outcome.

**Capability is not authority.**
