---
name: apollo-implement-feature
description: Implement assigned Apollo backend or frontend feature work or defect fixes, including API contract coordination, relevant checks, and an integration and QA handoff.
---

# Implement an Apollo feature

Use the charter for the assigned role: `.codex/agents/backend-developer.toml` or `.codex/agents/frontend-developer.toml`. If the assignment spans both roles, have the coordinator separate ownership and name an integration owner. Paths are relative to the project root. Read `AGENTS.md`, the assigned feature's requirements and UX behavior, relevant decisions, and the affected code.

1. Confirm scope and assigned write paths. Inspect the actual stack and commands before choosing an approach. If the app does not exist yet, establish necessary product and technical constraints with the coordinator before scaffolding.
2. Choose an implementation that satisfies the criteria with proportionate complexity. Surface consequential decisions and tradeoffs; make routine choices directly. Identify relevant data changes, API behavior, and failure handling. Before dependent backend and frontend work, agree on request and response shapes, authentication expectations, validation, and errors in the feature document or an existing API schema. Assign shared schemas, manifests, lockfiles, and configuration to one writer.
3. Implement the assigned change within the role boundary: Backend Developer owns server logic, persistence, migrations, server-side validation and authorization; Frontend Developer owns UI, client state, accessibility, and API consumption. Communicate contract changes before dependent edits. Label frontend mocks and replace or bypass them with actual service integration before claiming the complete feature works. Preserve other work and avoid touching another agent's files. If requirements are inconsistent or incomplete, return the specific decision needed while progressing on independent work.
4. Run relevant checks, including meaningful behavioral tests when warranted. Backend work needs appropriate server and API checks; frontend work needs appropriate UI and interaction checks. The assigned integration owner connects the parts and checks actual user flows against the backend. Identify any remaining mocks or blocked integration. Record exact commands and outcomes. Do not represent unavailable or skipped checks as successful.
5. Update the assigned implementation notes or return them to the coordinator. Explain setup, migrations, known limitations, and how QA can reproduce the feature. Identify the implementation version; without Git, arrange a stable set of files while QA verifies.

Handoff: changed paths, acceptance criteria addressed, contract changes, checks executed, remaining mocks or integration gaps, limitations, and QA starting instructions. Developer checks do not substitute for an independent QA verdict.
