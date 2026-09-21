# Team guide

## Roles

| Role | Charter | Owns | Usual outputs |
| --- | --- | --- | --- |
| Coordinator | [AGENTS.md](../AGENTS.md) | Assignments, dependencies, integration, completion | Current plan, backlog, decisions, consolidated result |
| PM | [pm.toml](../.codex/agents/pm.toml) | User problem, scope, priorities, acceptance criteria | Product brief and feature requirements |
| UX Designer | [ux-designer.toml](../.codex/agents/ux-designer.toml) | Flows, interaction behavior, accessibility | UX specification and relevant screen states |
| Backend Developer | [backend-developer.toml](../.codex/agents/backend-developer.toml) | Server logic, APIs, persistence, server-side validation and authorization | API contract, backend code, migrations, tests, handoff |
| Frontend Developer | [frontend-developer.toml](../.codex/agents/frontend-developer.toml) | UI, client state, accessibility, API consumption | Responsive interface, frontend tests, integration handoff |
| QA | [qa.toml](../.codex/agents/qa.toml) | Independent verification and reproducible findings | Acceptance results, defects, coverage gaps |

Role charters specify working boundaries, not operating-system access controls. Runtime permissions still apply.

## From idea to verified feature

1. The coordinator reads the current product context and selects a bounded feature.
2. PM writes the problem, scope, and numbered acceptance criteria in a feature document. Ask the user only for decisions that meaningfully affect scope or behavior.
3. UX describes relevant user flows and states. QA can review the requirements for testability and suggest missing cases at this stage.
4. Backend Developer and Frontend Developer agree on the API contract for features spanning both, then implement their assigned parts. Use only the relevant developer for a change confined to one area. QA can independently prepare scenarios while implementation proceeds.
5. The assigned integration owner connects the parts and checks the real flow. QA tests the integrated implementation against the specification, recording evidence and findings. The responsible developer fixes defects; QA rechecks affected behavior.
6. The coordinator reconciles the results, updates the backlog and decision log, and reports completion or remaining gaps.

Scale the process to the task. A copy edit or small bug fix can skip irrelevant product and design documents. Return to an earlier role when evidence reveals a requirement or design gap.

## Assignments and handoffs

The coordinator provides: objective; input paths and implementation version where applicable; acceptance criteria; permitted write paths; dependencies; expected deliverable; and when to return.

Specialists return: outcome; files changed or suggested changes; evidence from checks actually executed; assumptions or unresolved questions; and recommended next owner. If a check cannot run, explain what is missing and mark it blocked or not run.

Feature documents have one active writer at a time, even when agents would edit different sections. Parallel reviewers return their findings to the coordinator for integration. Assign separate test files explicitly if QA and either developer author tests. After implementation, pause changes to the files under verification until QA finishes, or identify exactly which version QA tested.

For work spanning backend and frontend, record request and response shapes, authentication expectations, validation, and error behavior before dependent implementation. Include pagination or other behavior only when relevant. The coordinator assigns one writer for shared API types, dependency manifests, lockfiles, and configuration, plus one developer responsible for integration. Route contract changes to the other developer before implementing dependent changes. Frontend may use clearly identified mocks for parallel progress, but the handoff must distinguish mocked behavior from behavior verified against the actual backend.

## Workflow skills

| Skill | Use it for |
| --- | --- |
| [apollo-feature-spec](../.agents/skills/apollo-feature-spec/SKILL.md) | Turning a product idea into bounded scope and testable requirements |
| [apollo-ux-spec](../.agents/skills/apollo-ux-spec/SKILL.md) | Specifying user flows, UI behavior, and accessibility |
| [apollo-implement-feature](../.agents/skills/apollo-implement-feature/SKILL.md) | Implementing the assigned backend or frontend work and preparing an integration and QA handoff |
| [apollo-verify-feature](../.agents/skills/apollo-verify-feature/SKILL.md) | Checking implementation against requirements and reporting defects |

Invoke a skill by name, or ask the coordinator for the relevant work. Skills describe procedures; agent definitions describe responsibility. All five specialist roles share the product brief, feature documents, and decision log. The two developers share the implementation skill and follow their respective role charters.

## Configuration reference

This setup uses project agent TOML files and repository skills as described in the official [subagent documentation](https://learn.chatgpt.com/docs/agent-configuration/subagents) and [skills documentation](https://learn.chatgpt.com/docs/build-skills). No model overrides or external integrations are required.
