---
name: implement-java-feature
description: Implement an approved Java feature while preserving application boundaries, repository conventions, decision traceability, documentation quality, and migration safety. Use for production Java changes after the implementation plan is authorized.
---

# Skill — Implement Java Feature

## Purpose
Implement production Java/Spring behavior according to an approved plan.

## Inputs
- Approved implementation plan.
- Relevant repository context.

## Procedure
1. Inspect existing conventions before creating new abstractions.
2. Implement business behavior in domain/application components.
3. Keep business logic out of controllers, DTOs, persistence entities, and
   provider-specific adapters.
4. Reuse existing abstractions before introducing new ones.
5. Implement boundaries as required:
   - Spring Web MVC;
   - asynchronous job or messaging adapters;
   - provider adapters;
   - Spring Data JPA repositories;
   - configuration.
6. Add Flyway migration when persistence schema changes.
7. Use the Java baseline and framework conventions governed by the repository's
   active ADRs and engineering standards.
8. Keep changes scoped and reviewable.
9. Remove dead/debug/speculative code before completion.
10. Optimize first for human-readable names, responsibilities, and control
    flow. Refactor code that requires narration merely to be understood.
11. Apply [Comments and JavaDoc](../../../docs/engineering/coding-standards.md#comments-and-javadoc)
    to changed methods, properties, and boundaries.
12. Recheck every nearby existing comment after behavior changes and remove or
    update anything stale, contradictory, speculative, or misleading.

## Output
Compiling production implementation ready for tests/quality gates.

## Validation
- Compiles.
- Matches BDR/ADR/product behavior.
- No unrelated architectural change.
- No secret/credential exposure.
- Data changes have migrations.
- Normal flow is readable through code structure and names.
- Non-obvious intent and boundary contracts are documented accurately.
- Documentation satisfies the linked coding standard.
- The final task diff satisfies the applicable rules and authorized slice,
  with evidence under [verification and completion](../../../docs/engineering/ai-development-standards.md#verification-and-completion).

## Stop conditions
Stop and return to planning when implementation reveals a missing durable
decision.
