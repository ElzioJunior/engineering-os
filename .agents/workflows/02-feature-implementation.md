# Workflow 02 — Feature Implementation

## Objective
Implement the approved feature in the smallest coherent change.

Before editing or resuming a slice, reconcile the latest user instruction with
the plan and a comparable flow in the target service. Implement the authorized
behavior using that flow when it fits. Treat open proposals as pending. A new
table, scheduler, or delivery guarantee must trace to an explicit requirement
or active decision before it enters the slice. Follow the current instruction
for staging and review checkpoints.

## Skills
Before implementing, apply
[Prefer existing platform capabilities](../../docs/engineering/coding-standards.md#prefer-existing-platform-capabilities):
inspect comparable project flows and available framework mechanisms, and
choose the simplest option that preserves the required semantics. Recheck this
choice before handing the change to quality gates.

Execute:
1. `../skills/implement-java-feature/SKILL.md`
2. `../skills/create-unit-tests/SKILL.md`
3. `../skills/create-functional-tests/SKILL.md` when the feature has an important
   functional flow that should be validated across application boundaries.

Before completing, verify the adopting project's test layout and suite isolation
under [Testing Standards](../../docs/engineering/testing-standards.md#project-configuration).
Create real-boundary integrated tests when Workflow 05 is in scope.

Before handing the implementation to quality gates, apply
[Comments and JavaDoc](../../docs/engineering/coding-standards.md#comments-and-javadoc)
and the [verification and completion checks](../../docs/engineering/ai-development-standards.md#verification-and-completion)
to the final slice diff.

## Incremental delivery

Treat completion of each small, coherent implementation or backlog slice as a
delivery boundary:

1. Run the focused validation appropriate to the completed slice and record
   only evidence that was actually produced.
2. Update the canonical execution plan with the backlog status, resumable
   checkpoint, current user constraints, corrected assumptions, validation
   evidence, and exact next action.
3. Inspect the complete slice diff and identify exactly which implementation,
   tests, documentation, and execution-plan changes belong to that slice.
4. When the Workflow 01 development authorization exists, stage only the
   identified slice, commit it with a message that identifies its backlog item
   or behavior, and push it to the current remote branch without force-pushing.
5. Continue directly to the next planned slice without asking for another
   approval. Report concise progress and commit hashes at useful checkpoints.

The Workflow 01 authorization is lifecycle-wide, not slice-specific. If it is
absent, leave validated changes in the worktree and stop before starting the
next slice. A safe, retryable push failure does not create a new authorization
gate; preserve the commit, report/retry the failure, and continue only when
repository provenance remains reliable.

Do not absorb unrelated or user-owned changes into a checkpoint commit. Do not
commit secrets, generated artifacts, debug files, or claims unsupported by the
recorded validation. If an authorized commit or push cannot be completed
safely, preserve the completed work and keep the execution plan as an accurate
resume point.

## Output
Production implementation, required JavaDoc, and documented automated tests,
ready for quality gates, with every completed slice reflected in the execution
plan. Under the Workflow 01 development authorization, validated slices are
committed and pushed without per-slice approval.

## Stop conditions
Return to Workflow 01 if a missing business/architecture decision is discovered.

## Completion boundary
Do not perform the final comprehensive quality review here.
