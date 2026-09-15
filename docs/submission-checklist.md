# Submission Checklist

This checklist is deliberately conservative. Reconcile it with current authoritative ACT III rules before submission.

## Competition contract

- [ ] Current deadline/timezone reverified
- [ ] Current tracks reverified
- [ ] Eligibility and solo-team status reverified
- [ ] Required AMD technologies reverified
- [ ] Judging criteria reverified
- [ ] Submission fields reverified

## Technical proof

- [ ] Real AMD-backed AI workload runs reproducibly
- [ ] AMD/ROCm usage is evident in code/runtime evidence
- [ ] Agent has real UCII cryptographic identity binding
- [ ] Identity verification does not create execution authority
- [ ] Missing authority denies execution
- [ ] Bounded delegated authority permits only matching action
- [ ] Revocation is effective on a fresh authorization check
- [ ] Same verified identity remains after revocation
- [ ] Consequential executor structurally requires authorization
- [ ] Provenance records the canonical sequence
- [ ] Failure paths fail closed
- [ ] Targeted/adversarial tests pass

## Public repository

- [ ] README explains project in seconds
- [ ] License present
- [ ] Setup instructions verified from a clean environment
- [ ] Architecture documented
- [ ] AMD integration documented
- [ ] UCII public-boundary integration documented
- [ ] No private keys, tokens, credentials, or secrets committed
- [ ] No private UCII implementation copied into this repository
- [ ] Commit history reflects meaningful development

## Judge experience

- [ ] Demo starts from a known state
- [ ] AMD workload visibly established
- [ ] UCII identity visibly VERIFIED
- [ ] First unauthorized action visibly DENIED
- [ ] Human bounded grant visibly established
- [ ] Same action visibly EXECUTED
- [ ] Delegated authority visibly REVOKED
- [ ] Same action visibly DENIED after revocation
- [ ] Provenance/evidence is readable
- [ ] Demo can be repeated reliably

## Submission media — REVERIFY exact requirements

- [ ] Project title and descriptions complete
- [ ] Cover image complete
- [ ] Demo video complete and within required duration
- [ ] Slide presentation complete
- [ ] Public GitHub URL correct
- [ ] Demo/application URL correct if required
- [ ] Product feedback complete if requested
- [ ] Friction evidence complete if useful/eligible

## Final security review

- [ ] No authority can be minted by model output
- [ ] No authentication-to-authorization shortcut
- [ ] No stale authority survives revocation
- [ ] No secret material appears in logs/screenshots/video
- [ ] Judge/test path does not weaken production UCII trust boundaries

## Final rule

Do not submit based on this checklist alone. Perform a final authoritative rules review and update this file for any changes before submission.
