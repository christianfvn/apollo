# Decision log

Record consequential choices with date, status, context, decision, rationale, and affected feature links. Distinguish proposed choices from decisions already made; supersede earlier entries explicitly when direction changes.

## D-001: Development team structure

- Date: 2026-09-21
- Status: accepted by the user; developer role superseded by D-002
- Context: Start a web app with specialist AI roles and a shared workflow.
- Decision: Use the main conversation as coordinator, with PM, UX Designer, Developer, and QA roles; keep project instructions, role definitions, workflow skills, and durable handoff documents in this folder.
- Rationale: Separate responsibilities while sharing requirements and maintaining traceable handoffs.
- Scope: Team setup only. Product requirements and technology selection remain open.

## D-002: Separate backend and frontend development

- Date: 2026-09-21
- Status: accepted by the user
- Context: The user requested separate backend and frontend developer roles.
- Decision: Replace Developer with Backend Developer and Frontend Developer. Keep a shared implementation skill, with distinct role charters and an explicit API contract and integration handoff for work spanning both areas.
- Rationale: Clarify server and UI ownership while preserving coordinated delivery and independent QA.
- Effect: Supersedes the single Developer role in D-001. The coordinator assigns ownership of shared files and integration; QA verifies the integrated feature.
