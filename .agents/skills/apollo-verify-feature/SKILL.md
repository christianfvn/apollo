---
name: apollo-verify-feature
description: Independently verify an Apollo feature against acceptance criteria, or review requirements for testability. Produce evidence, reproducible defects, and explicit coverage gaps.
---

# Verify an Apollo feature

Use the QA charter in `.codex/agents/qa.toml`. Paths are relative to the project root. Read `AGENTS.md`, the assigned acceptance criteria and UX specification, and relevant implementation instructions.

For an early requirements review, identify ambiguous outcomes and missing high-impact scenarios. Return proposed clarifications to the coordinator. Do not issue an implementation pass before there is an implementation to test.

For implementation verification:

1. Record the environment, prerequisites, and implementation version or stable file snapshot. Coordinate with the writer so results refer to an identifiable implementation.
2. Map each acceptance criterion to appropriate checks. Include important normal, error, boundary, and regression cases. Inspect implementation and tests where useful, and exercise the running UI when browser tooling is available. Code inspection alone does not establish that a UI flow works. For work spanning backend and frontend, verify the real integrated flow and relevant API failure behavior. Record both implementation versions and any remaining mocks; mocked checks alone do not establish integration success.
3. Execute the available checks. Record pass, fail, blocked, or not run for every criterion, with evidence and reasons for gaps. Keep proposed tests separate from executed tests. If a defect prevents later checks, record the dependency explicitly.
4. Report defects with an ID, user impact and severity, prerequisites, reproduction steps, expected and actual behavior, and supporting evidence. Do not change application code or acceptance criteria during verification. Author test files only when assigned exclusive ownership.
5. Return a verdict supported by the criterion results. After the responsible backend or frontend developer fixes a defect, rerun affected checks and relevant regressions before recording it as resolved.

Write only the assigned QA report or feature section. When the feature document has another active writer, return results to the coordinator for integration. Disclose when the same agent implemented the change and the review is therefore not independent.
