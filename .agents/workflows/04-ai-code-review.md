# Workflow 04 — AI Code Review

## Objective
Independently review the implementation after quality gates pass.

Check compliance with
[Prefer existing platform capabilities](../../docs/engineering/coding-standards.md#prefer-existing-platform-capabilities).
Flag custom infrastructure that duplicates a simpler supported project or
framework mechanism, explaining the concrete maintenance cost and an
equivalent alternative that preserves behavior.

Compare the diff with the currently authorized slice and the analogous project
flow. Flag material deviations whose requirement or active decision is missing.
When reviewing a colleague's change for comments, report findings in the
requested format. Apply fixes when the review request or lifecycle authorizes
implementation.

## Skills
Enforce [Do not bypass quality rules](../../docs/engineering/coding-standards.md#do-not-bypass-quality-rules):
identify bypasses introduced by the change and require correction of the
underlying issue rather than suppression of the finding.

Execute:
1. `../skills/review-code/SKILL.md`
2. `../skills/apply-review-findings/SKILL.md` when actionable findings exist and
   implementation is authorized.
3. `../skills/run-quality-checks/SKILL.md` again for affected checks after fixes.

When the execution environment and user instructions allow delegation,
independent review dimensions may be assigned to separate reviewers.

Under an authorized full lifecycle, apply review findings, rerun affected
quality checks, commit/push coherent corrections, and continue to integrated
test preparation without an approval pause.

## Output
Review report with rule references, evidence, and validation limits. When fixes
are authorized, include corrections, deferred findings, and updated results.

## Completion condition
A review-only request completes with its findings and validation limits.
An implementation lifecycle can advance when BLOCKER and HIGH findings are
resolved and applicable mandatory rules satisfy the
[completion standard](../../docs/engineering/ai-development-standards.md#verification-and-completion).
