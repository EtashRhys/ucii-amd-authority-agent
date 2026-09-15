# Judging Strategy

## Goal

Make the technical distinction visible immediately:

> The AMD-backed agent remains equally capable before and after authorization changes. UCII independently changes whether that capability may become a consequential action.

## Current judging dimensions to design for

The ACT III event material previously identified these dimensions and they must be reverified before submission:

- Application of Technology
- Presentation
- Business Value
- Originality

## Application of Technology

Show real AMD infrastructure/ROCm usage and real UCII integration. Avoid sponsor-logo integration. The code and runtime evidence should make both technologies' roles obvious.

## Presentation

A judge should understand the entire security thesis from one short sequence:

**DENY → GRANT → EXECUTE → REVOKE → DENY**

Keep identity verification visibly constant so the authority-state difference is unmistakable.

## Business Value

Frame the problem broadly: enterprises want autonomous agents to perform useful work, but identity verification alone does not establish permission to spend, modify infrastructure, invoke tools, move data, or trigger external effects.

UCII provides a reusable control plane for bounded autonomous authority across execution environments.

## Originality

Do not compete as another generic AI agent. The differentiator is independent cryptographic identity plus externally enforceable delegated authority and revocation around an AMD-backed autonomous workload.

## Judge-facing evidence

Prefer observable proof over architectural claims:

- real AMD-backed workload;
- verified UCII identity;
- explicit authority state;
- structured requested action;
- deterministic allow/deny decision;
- actual execution result;
- revocation followed by fresh denial;
- attributable provenance.

## Narrative discipline

Never imply:

- model intelligence creates authority;
- successful authentication means authorization;
- AMD infrastructure itself grants UCII permission;
- a prior successful action grants future authority;
- provenance retroactively authorizes an action.

The story is strongest when the architecture itself enforces those distinctions.
