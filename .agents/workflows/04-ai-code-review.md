# Workflow 04 — AI Code Review

## Objective
Independently review the implementation after quality gates pass.

Check compliance with
[Prefer existing platform capabilities](../../docs/engineering/coding-standards.md#prefer-existing-platform-capabilities).
Flag custom infrastructure that duplicates a simpler supported project or
framework mechanism, explaining the concrete maintenance cost and an
equivalent alternative that preserves behavior.

## Skills
Enforce [Do not bypass quality rules](../../docs/engineering/coding-standards.md#do-not-bypass-quality-rules):
identify bypasses introduced by the change and require correction of the
underlying issue rather than suppression of the finding.

Execute:
1. `../skills/review-code/SKILL.md`
2. `../skills/apply-review-findings/SKILL.md` when actionable findings exist.
3. `../skills/run-quality-checks/SKILL.md` again for affected checks after fixes.

When the execution environment and user instructions allow delegation,
independent review dimensions may be assigned to separate reviewers.

Under an authorized full lifecycle, apply review findings, rerun affected
quality checks, commit/push coherent corrections, and continue to integrated
test preparation without an approval pause.

## Output
Review report, fixes applied, deferred findings, and updated quality results.

## Completion condition
No unresolved BLOCKER or HIGH finding.
