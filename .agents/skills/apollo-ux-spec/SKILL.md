---
name: apollo-ux-spec
description: Specify Apollo user journeys, UI interactions, screen states, and accessibility for a defined feature. Use before UI implementation or for a focused experience review.
---

# Specify the Apollo experience

Use the UX charter in `.codex/agents/ux-designer.toml`. Paths are relative to the project root. Read `AGENTS.md`, the product brief, feature requirements, and existing design conventions or supplied references.

1. Map entry points, the primary journey, alternate paths, and completion behavior. Tie behavior to acceptance criterion IDs where useful.
2. Describe the screens and interactions needed to implement the flow, including relevant loading, empty, validation, error, success, and permission states. Include recovery from errors rather than just error messages.
3. Specify responsive behavior, keyboard interaction, focus movement, accessible names, and status feedback as applicable. For an existing UI, preserve its established design language unless the requested change requires otherwise.
4. Write the experience section of the assigned feature document. Create wireframes or prototypes only when they resolve a real ambiguity or the user requests them. Keep prototype artifacts within assigned paths.
5. Flag requirement gaps to the coordinator; do not silently expand scope. Distinguish proposed design choices from validated user findings.

Handoff: implementable flows and states, relevant artifacts, accessibility behavior, unresolved questions, and observable checks for QA. If another agent owns the feature document, return the proposed section to the coordinator instead of editing it concurrently.
