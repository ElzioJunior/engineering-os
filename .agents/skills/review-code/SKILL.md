---
name: review-code
description: Perform an evidence-based review of a completed change for correctness, decisions, architecture, test quality, security, reliability, readability, and unnecessary complexity. Use after quality gates pass or when an independent code review is requested.
---

# Skill — Review Code

## Purpose
Perform an independent, evidence-based review of a completed change.

## Inputs
- Diff.
- Tests.
- Quality report.
- Relevant BDRs/ADRs/standards/data model.

Load the applicable rules and current authorized scope through the active
`AGENTS.md`, including when this skill is invoked directly. Inspect the actual
task diff and relevant callers. Use the implementation summary as context and
verify its claims against code and test evidence. Report any unavailable checks.

## Review dimensions
1. Correctness and edge cases.
2. Architecture and boundaries.
3. Business-rule compliance.
4. Test quality/completeness.
5. Security and sensitive-data handling.
6. Reliability:
   - durable job/message claiming, completion, retry, and recovery when used;
   - duplicate side effects;
   - idempotency where required;
   - external integration failure behavior.
7. Human readability and maintainability:
   - explicit domain naming and cohesive responsibilities;
   - cognitively simple control flow;
   - comments do not compensate for avoidable structural complexity;
   - non-obvious rationale, invariants, contracts, side effects, and failure
     semantics are documented;
   - JavaDoc exists where an architectural/public boundary needs an explicit
     contract;
   - changed methods, properties, and tests satisfy
     [Comments and JavaDoc](../../../docs/engineering/coding-standards.md#comments-and-javadoc);
   - comments and JavaDoc are accurate, useful, non-sensitive, and consistent
     with the implementation and governing decisions.
8. Unnecessary complexity.
9. Adherence to the authorized slice and applicable mandatory standards,
   including new infrastructure, client configuration, and shared-code changes.

## Finding format
Each finding must include:
- severity: BLOCKER / HIGH / MEDIUM / LOW;
- location;
- problem;
- consequence;
- recommended fix.
- governing rule and verification evidence for a standards finding.

Do not produce vague stylistic findings.
Readability findings must identify the concrete comprehension or maintenance
risk. Report missing documentation required by an applicable standard, including
test-method JavaDoc. For other comments, establish the important intent or
contract that code and existing documentation leave unclear.

## Output
Structured review report.

## Validation
Every finding must be grounded in code, tests, or repository decisions. Apply
the [verification and completion rules](../../../docs/engineering/ai-development-standards.md#verification-and-completion)
when deciding whether implementation is compliant. Keep a review-only task
within its requested reporting scope.
