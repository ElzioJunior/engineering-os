# Definition of Done

A change is done when, as applicable:

- Business behavior matches the relevant product docs and BDRs.
- Architecture complies with accepted ADRs.
- Code complies with engineering standards.
- Automated tests cover the new/changed behavior.
- Unit-test coverage remains at or above the required threshold for eligible code.
- Relevant functional tests pass.
- No known security-sensitive data is exposed.
- Logging and errors are actionable and do not leak secrets.
- Public/API behavior is documented when changed.
- A new ADR/BDR is added when the change introduces a durable architectural/business decision.
- The implementation has been reviewed for unnecessary complexity and dead code.
- The normal execution flow is understandable through explicit names,
  cohesive responsibilities, and cognitively simple structure.
- Non-obvious rationale, invariants, contracts, side effects, failure behavior,
  and architectural/external boundaries have accurate comments or JavaDoc when
  code alone cannot communicate them safely.
- Changed behavior has not left stale, contradictory, speculative, or
  sensitive comments/JavaDoc behind.
- Documentation satisfies [Comments and JavaDoc](coding-standards.md#comments-and-javadoc),
  including its method, property, and test criteria.
- The final task diff matches the authorized scope and current user constraints.
- Applicable mandatory rules have evidence or an explicit scoped exception
  under [Verification and completion](ai-development-standards.md#verification-and-completion).
  Required checks with missing evidence remain unverified.

Apply this definition to the requested deliverable. A review-only deliverable
contains findings and validation limits. An implementation deliverable must
satisfy its applicable checks before being reported as complete.
