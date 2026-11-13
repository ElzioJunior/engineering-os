---
name: load-relevant-context
description: Load the minimum product, decision, engineering, data, code, and test context needed for a repository task. Use before planning or implementing non-trivial changes when correctness depends on project-owned documentation.
---

# Skill — Load Relevant Context

## Purpose
Load the minimum repository context required to understand a task correctly.

## Inputs
- User request.
- Optional target files/classes/components.

## Procedure
1. Locate the active standards and service context through the applicable
   `AGENTS.md`. Follow centralized-context routing when configured. Use the
   active documentation map to locate the relevant documents.
2. Read the relevant product files under `docs/product/`.
3. Find relevant active BDRs under `docs/bdr/`.
4. Find relevant active ADRs under `docs/adr/`.
5. Check `docs/DECISIONS.md` for related open decisions.
6. Read applicable engineering standards under `docs/engineering/`.
7. Read `docs/database/` when persistence/data is involved.
8. Inspect affected source and tests when they exist.
9. Ignore unrelated documentation unless dependencies require expansion.

Use the [before-edit and resumption checks](../../../docs/engineering/ai-development-standards.md)
to establish scope, source revision, applicable rules, comparable flows, and
local validation commands. Resolve paths through the adopting project's entry
point when the standards live outside the service.

## Output
A concise context summary containing:
- intended behavior;
- governing BDRs;
- governing ADRs;
- applicable engineering standards;
- data-model constraints;
- related open decisions;
- affected code areas;
- unresolved conflicts or missing decisions;
- current scope, accepted decisions, pending proposals, and existing authorization;
- repository/base and any discrepancy with generated context;
- comparable flow and rule-to-verification references for the task.

## Validation
Every material implementation assumption must be traceable to context or clearly
identified as an assumption.

## Stop conditions
Stop when active records conflict or a missing durable decision prevents safe
implementation.
