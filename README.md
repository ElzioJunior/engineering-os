# Engineering OS for Java Projects

This repository is a reusable, repository-owned operating system for building
Java applications with engineers and AI coding agents. It was extracted from
Supply Pilot and generalized so that product rules, architecture decisions,
engineering standards, delivery workflows, and implementation evidence remain
traceable in other projects.

## What to copy into a new project

Copy these paths to the root of the target repository:

- `AGENTS.md`
- `docs/`
- `.agents/` — public-format Agent Skills and repository workflows.

Then complete the placeholders in `AGENTS.md`, create the initial product
documents and decisions, and adapt the commands and thresholds in
`docs/engineering/` to the project's build.

## Operating model

The default feature lifecycle is:

1. design and context update;
2. implementation and automated tests;
3. quality gates;
4. independent AI code review;
5. opt-in real-boundary integrated tests, when applicable;
6. finalization and documentation synchronization.

The lifecycle uses two planned human authorization gates:

1. after the design, decision-impact report, and execution plan;
2. immediately before the first test that consumes a real provider, paid API,
   real model, production-like shared environment, or other consequential
   external boundary.

Projects that have no consequential real-boundary suite may explicitly mark the
second gate as not applicable in the execution plan.

The portable skills live at `.agents/skills/<skill-name>/SKILL.md` and follow
the public Agent Skills specification. Workflow ordering remains separate under
`.agents/workflows/`; numeric prefixes apply only to workflows.

## Adoption checklist

- Replace all `<PROJECT_...>` placeholders in `AGENTS.md`.
- Record the supported Java version and framework in an ADR.
- Confirm the Maven/Gradle commands and test source layout.
- Choose and document the coverage threshold.
- Create the first product overview and decision register.
- Remove optional folders that the project deliberately does not use.
- Keep project-specific skills in the target project; do not add them to this
  reusable baseline unless they are genuinely feature-agnostic.

## Provenance

The reusable baseline was exported from Supply Pilot on 2026-08-31. Product,
supplier, procurement, WhatsApp, and provider-specific behavior was deliberately
excluded. The source repository was not modified by this export.
