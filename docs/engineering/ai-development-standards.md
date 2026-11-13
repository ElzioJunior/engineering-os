# AI-Assisted Development Standards

## Applicability and authority

Apply these practices to implementation and review, including standalone tasks
and resumed work. Use the source priority and authorization boundaries in the
active `AGENTS.md`. Carry forward explicit user instructions and granted
authorization until the user changes them. A workflow applies within the scope
requested by the user.

Engineering standards own recurring rules. Workflows and skills link to those
rules at the point of use. Keep local adaptations explicit and resolve
contradictions at their source. An example illustrates its stated conditions.
A preference allows alternatives with a concrete reason. A mandatory rule
requires compliance or an explicit applicable exception.

## Before the first edit

For a non-trivial task, establish the following in the existing plan, checkpoint,
or a concise working summary. Reuse the same record throughout the task.

| Evidence | What to establish |
| --- | --- |
| Scope and authority | Requested behavior, current slice, explicit exclusions, review mode, and staging/publication instructions. Distinguish accepted decisions from open proposals. |
| Working state | Repository, branch/base revision, relevant existing changes, active standards location, and service context revision when available. |
| Applicable rules | Links to the sections that govern the changed boundaries and how the implementation will satisfy them. Read referenced sections before relying on them. |
| Existing implementation | A comparable component or flow, its relevant configuration, and the concrete gap if a different mechanism is needed. |
| Verification | Applicable configured commands, expected behavioral evidence, and review checks for rules that tooling cannot prove. |

For a small correction, establish only the affected rules and checks. Keep this
record proportional to the task. Use an existing artifact or the conversation
when a separate plan adds no value.

Load centralized context first when the workspace requires it. Check affected
source afterward. Record stale or mismatched context and use the current
implementation to establish behavior, while preserving the governing intent.
For provider-specific behavior, verify the contract and effective configuration
before introducing shared decoding, validation, recovery, or infrastructure.

## During implementation and resumption

Use the established flow when it meets the requirement. Trace new infrastructure,
dependencies, queries, and durable behavior to the authorized requirement or
active decision. If an agent-created precaution expands the scope, remove that
expansion and proceed with the authorized solution. Resolve a genuine missing
decision only for the work that depends on it.

When the user corrects a choice, update the implementation, affected tests, and
the existing checkpoint together. Record the decision and its reason so the
next slice can apply it. Keep feature-specific limits and exceptions in the
feature context. Promote recurring guidance into the owning standard when a
durable update is requested.

On resumption, handoff, or a change of scope, reread the current request,
checkpoint, and relevant standards. Check branch/base and the current diff.
Reconcile superseded assumptions before editing. Reuse valid evidence for
unchanged areas and rerun checks affected by subsequent changes.

## Verification and completion

Inspect the final task diff, including staged, unstaged, and new files belonging
to the task. Compare it against the applicable rules and the authorized slice.
For each material rule, retain a source reference and concrete evidence in the
existing quality report or delivery summary. Suitable evidence includes the
component reused, a targeted test result, a configured static-analysis result,
or the location inspected during review. A statement that standards were read
establishes context loading only.

Use the following outcomes for applicable checks.

| Outcome | Required handling |
| --- | --- |
| Passed | Record the executed command or inspected evidence and its result. |
| Failed | Fix in-scope violations and rerun affected checks. |
| Unverified | State the missing evidence and the concrete blocker. Keep the completion claim limited to what was verified. |
| Not applicable | Give the task-specific reason. |
| Explicit exception | Reference the user's instruction or active decision and its scope. |

Configured tests and linters establish the properties they check. Review scope,
reused behavior, business semantics, authorization, and unnecessary complexity
against the actual diff as well. Review severity describes impact. Mandatory
rule violations require correction or an explicit applicable exception before
claiming implementation compliance, including violations rated MEDIUM or LOW.

A review-only task finishes by reporting findings and validation limits.
Applying findings requires implementation authorization. For implementation,
complete the requested slice and report remaining blockers or unverified
requirements clearly. Follow the user's publication instructions at delivery.

## Deterministic enforcement in adopting projects

During adoption or a requested tooling update, bind mechanically checkable rules
to the repository's existing formatter, static analyzer, test runner, and CI.
Record the command and configuration location in the local engineering
standards. Examples include formatting, size limits, test isolation, coverage,
and architecture dependencies when supported by the selected tooling.

Verify that configured checks detect a representative violation and fail with
an actionable result. Use protected required CI checks where the repository's
delivery policy provides them. Agent instructions and local hooks complement
that enforcement. Report uncovered rules as tooling gaps and review them
explicitly until enforcement exists. Make tooling changes within the authorized
scope and preserve existing thresholds and exceptions.
