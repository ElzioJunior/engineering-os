# Agent Operation

This directory keeps portable capabilities separate from repository delivery
orchestration:

- [skills](skills/README.md) use the public Agent Skills directory and
  `SKILL.md` format;
- [workflows](workflows/README.md) define the project-owned execution order and
  authorization boundaries.

Skills are independently discoverable and reusable. Workflows may invoke them
by relative path but must not duplicate their detailed procedures.
