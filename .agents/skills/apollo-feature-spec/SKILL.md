---
name: apollo-feature-spec
description: Turn an Apollo app idea or feature request into bounded scope and testable acceptance criteria. Use for MVP discovery and feature specification.
---

# Specify an Apollo feature

Use the PM charter in `.codex/agents/pm.toml`. Paths in this skill are relative to the Apollo project root. Read `AGENTS.md`, `docs/product.md`, the relevant backlog entry, and prior decisions.

1. Identify the target user, problem, intended outcome, and constraints from available evidence. Separate facts from assumptions. Ask only the questions that affect the next decision; keep making progress on independent parts.
2. Define the smallest useful scope and explicit exclusions. Describe success in observable terms without inventing product metrics or research.
3. Create or update the assigned feature document using `docs/templates/feature.md`. Give acceptance criteria stable IDs such as AC-01 and cover relevant error and boundary behavior as well as the normal flow. Avoid prescribing implementation details unless they are actual constraints.
4. Identify dependencies and decisions UX, Backend Developer, or Frontend Developer will need. Recommend QA review of ambiguous or hard-to-test criteria. Return proposed changes to the coordinator when the shared document is owned by another writer.

Handoff: scope, acceptance criteria, assumptions, unresolved decisions, changed files, and readiness for UX and development. Update `docs/product.md` only when assigned. The coordinator owns backlog and decision-log updates.
