# Apollo

A web app workspace with a Codex development team. The application has not been scaffolded yet.

## Start here

Open this folder in Codex and start a new task so the project instructions and agent definitions can be loaded. Try:

> Use the Apollo team to help define the MVP. Start with the PM. My app is for [target users] who need to [main task]. Record the product brief, identify the most important unanswered questions, and propose the first feature.

For a feature with clear requirements:

> Coordinate the Apollo team to implement [feature]. Have PM define acceptance criteria, UX specify the experience, Backend Developer and Frontend Developer agree on the API contract and implement their parts, and QA independently verify the integrated feature. Keep the feature document and backlog current.

For a focused review:

> Have QA verify [feature] against its acceptance criteria. Report evidence and reproducible defects without changing application code.

## Team files

- [Shared instructions](AGENTS.md): coordination and completion rules.
- [Team guide](docs/team.md): responsibilities, handoffs, and available skills.
- [Product brief](docs/product.md): known facts and open product questions.
- [Backlog](docs/backlog.md): current work and next steps.
- [Decision log](docs/decisions.md): durable product and technical decisions.
- [Feature template](docs/templates/feature.md): specification through verification.

Custom agents live in `.codex/agents/`; reusable skills live in `.agents/skills/`. These definitions are used on demand, not continuously running services. They inherit the parent session's model and permissions. The coordinator is the main conversation, not a fifth spawned agent.

If new skills or named agents do not appear, reopen the task or restart Codex. The coordinator can also read the role files and delegate their instructions to general subagents. Project trust and client support may affect configuration loading.

## Development

Product scope, stack, and application commands are undecided. Define the MVP before scaffolding. Add the actual installation, local development, build, and test commands here when the application exists.
