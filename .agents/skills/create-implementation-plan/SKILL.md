---
name: create-implementation-plan
description: Turn approved repository context and decisions into a scoped, ordered Java implementation plan with acceptance criteria, test strategy, documentation impact, delivery slices, and authorization summary. Use after design context is resolved and before production implementation.
---

# Skill — Create Implementation Plan

## Purpose
Turn approved context and decisions into a small, executable coding plan.

## Inputs
- Context summary.
- Decision-impact result.
- Existing code structure.

## Procedure
1. Define acceptance criteria.
2. Identify affected modules/components.
3. Identify domain/application changes.
4. Identify applicable adapters/boundaries, such as:
   - HTTP/API;
   - asynchronous jobs or messaging;
   - third-party providers;
   - persistence;
   - configuration.
5. Identify data/Flyway impact.
6. Identify unit, isolated functional, and affected regression tests using the
   adopting project's configured layout and commands. Include real-boundary
   integrated work when it belongs to the requested scope. Use
   [Testing Standards](../../../docs/engineering/testing-standards.md#project-configuration)
   for defaults and adaptation rules.
7. Identify failure/edge cases.
8. Order work into small coherent steps.
9. Avoid speculative abstractions and unrelated refactors.
10. Identify documentation needed under
    [Comments and JavaDoc](../../../docs/engineering/coding-standards.md#comments-and-javadoc).
11. Produce a concise execution report that summarizes the approved scope,
    ordered development slices, material decisions/risks, validation and
    quality strategy, integrated-test scope, and normal commit/push behavior.

## Output
An ordered implementation plan with:
- files/components likely affected;
- behavior per step;
- tests per step;
- required JavaDoc/comment intent where code alone cannot communicate the
  contract safely;
- the existing flow to reuse and any justified material deviation per slice;
- applicable rule references and their planned verification;
- validation after each meaningful stage.

Also produce `<ID>-execution-report.md` beside the feature/epic and execution plan.
The report must be short enough for the user to approve the complete
development scope without rereading the detailed backlog. Under Workflow 01,
request development authorization when it is still needed and describe its
publication scope. Carry forward existing authorization and explicit limits
when updating an already authorized plan.

## Validation
The plan must not silently introduce a new durable decision.

## Stop conditions
Return to decision/context work if implementation cannot proceed without a new
BDR/ADR or unresolved requirement.
