---
name: create-functional-tests
description: Create isolated, reproducible Java functional tests for important flows across application boundaries while controlling external systems. Use when behavior needs more real wiring than a unit test but must remain independent of consequential real providers.
---

# Skill — Create Functional Tests

## Purpose
Validate important feature flows across application boundaries while remaining
isolated and reproducible.

## Inputs
- Feature behavior.
- Existing functional-test conventions.

## Procedure
1. Use the configured isolated-functional source set and naming convention under
   [Testing Standards](../../../docs/engineering/testing-standards.md#project-configuration),
   preserving production package paths and suite isolation.
2. Identify the smallest important end-to-end/application flow.
3. Exercise real application wiring where practical.
4. Isolate external systems using controlled test doubles or ephemeral
   dependencies.
5. Avoid shared mutable/manual environments.
6. Validate both successful and important failure flows.
7. Keep fixtures explicit and understandable.
8. Run the functional tests.
9. Add concise JavaDoc to every test method, explaining the flow or failure it
   proves and why that scenario matters.

## Output
Isolated functional tests for important feature behavior.

## Validation
Tests are repeatable locally/CI and do not require manual external preparation.
Every test method documents its scenario and relevance.

## Stop conditions
Do not introduce a new heavyweight integration platform/tool without an
accepted architectural/engineering decision when required.
