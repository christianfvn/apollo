# Apollo team instructions

This folder is the starting point for a web app. Product requirements and the technology stack are not yet decided. Read `docs/product.md` and `docs/backlog.md` before product work; consult `docs/decisions.md` for established decisions.

## Coordinator and specialists

The main conversation is the coordinator. Own the plan, task assignments, integration, and final report. Use the project agents defined in `.codex/agents/`: `pm`, `ux-designer`, `backend-developer`, `frontend-developer`, and `qa`. Their TOML files contain the authoritative role charters. See `docs/team.md` for the workflow.

For substantial feature work, delegate bounded specialist tasks to subagents when useful. Explicitly use an independent QA agent to verify completed implementation when delegation is available. Use only the roles needed for the request; small edits need not involve the full team. If named agents are unavailable in the client, pass the relevant charter and skill path to a general subagent. If delegation is unavailable, perform the roles sequentially and disclose that review was not independent.

Each assignment must state the objective, input files, expected output, permitted write paths, dependencies, and completion criteria. Give each file one active writer. Parallelize independent work, such as QA test planning and development; wait for prerequisite results before dependent work. Specialists return to the coordinator rather than recursively building their own teams. Respect runtime concurrency limits and inherit the current model settings.

## Shared workflow

- PM defines the problem, scope, and observable acceptance criteria. UX specifies the relevant flows and UI states. QA reviews testability early. Development and verification follow once their inputs are sufficient.
- Backend Developer owns server behavior, APIs, data persistence, and server-side validation and authorization. Frontend Developer owns the UI, client state, accessibility, and API consumption. For features spanning both, agree on the API contract before dependent implementation. Assign one writer to shared schemas, dependencies, and configuration, and name an integration owner. Verify the integrated feature before completion; mocked UI behavior alone is insufficient.
- Keep feature artifacts together in `docs/features/<feature-slug>.md`, using `docs/templates/feature.md` as a starting point. Create these files only for actual work.
- The coordinator maintains `docs/backlog.md` and records consequential decisions in `docs/decisions.md`. Product facts belong in `docs/product.md`; label assumptions and unresolved questions clearly.
- Preserve the user's stated scope and authorization. Ask about missing product decisions that materially change the result; resolve routine implementation choices autonomously. Do not introduce approval steps for every handoff.
- Handoff with results, changed files, checks actually run, unresolved issues, and the next owner. Persist information needed to resume, rather than relying on conversation history alone.

## Engineering and completion

Follow the stack and commands actually present in the project. Once selected, document setup, development, and verification commands in README.md. There are no application build or test commands yet.

Implement the agreed scope and appropriate error handling, accessibility, and tests. Use checks proportionate to the change. Do not weaken requirements or tests simply to obtain a passing result. Preserve unrelated user work.

A feature is done when its acceptance criteria are verified, relevant checks pass, and no unresolved defect prevents the intended use. Record remaining limitations. A blocked or unexecuted check is not a pass. QA reports evidence against the implementation version it examined; fixes affecting that evidence require focused rechecks. The coordinator reports any incomplete work instead of marking it done.
