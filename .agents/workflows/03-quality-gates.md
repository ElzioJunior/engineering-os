# Workflow 03 — Quality Gates

## Objective
Prove the implementation meets mandatory engineering standards.

Apply [Do not bypass quality rules](../../docs/engineering/coding-standards.md#do-not-bypass-quality-rules).
Correct failures at their source and rerun affected checks. Inspect the diff
for new suppressions, exclusions, disabled tests, or weakened rules before
reporting quality results.

## Skills
Execute:
1. `../skills/run-quality-checks/SKILL.md`

If a quality failure requires code/test changes, use the relevant implementation
or testing skill and rerun this workflow. Under an authorized full lifecycle,
apply fixes, commit/push coherent corrections, and continue without an approval
pause.

## Output
Passing quality report or explicit blocking failures.

## Completion boundary
Do not perform independent code review here.
