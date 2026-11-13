---
name: apply-review-findings
description: Apply actionable code-review findings with severity-based prioritization, narrow fixes, supporting tests, and affected quality reruns. Use after a structured review identifies defects or justified improvements.
---

# Skill — Apply Review Findings

## Purpose
Fix actionable code-review findings without expanding scope unnecessarily.

## Inputs
- Review report.
- Current implementation.

## Procedure
Apply this skill when implementing findings is authorized. For review-only
requests, complete the requested report through the review skill.

1. Fix all BLOCKER findings.
2. Fix all HIGH findings.
3. Fix in-scope mandatory-rule violations at any severity or record an explicit
   applicable exception under the
   [completion standard](../../../docs/engineering/ai-development-standards.md#verification-and-completion).
4. For other MEDIUM findings, fix or explicitly defer with reason. Apply other
   LOW findings when beneficial and low-risk.
5. Keep fixes narrowly scoped.
6. Add/update tests when findings expose missing behavior.
7. Rerun affected quality checks.
8. Re-review changed areas when fixes are substantial.

## Output
- Updated implementation.
- List of findings fixed.
- Explicitly deferred findings with rationale.
- Updated test/quality results.

## Completion condition
No unresolved BLOCKER or HIGH finding remains, and applicable mandatory-rule
violations are corrected or covered by an explicit exception.
