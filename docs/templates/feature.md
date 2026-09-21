# Feature: <title>

Copy to `docs/features/<feature-slug>.md` for a real feature. Replace the prompts below with current facts; remove irrelevant sections. The coordinator assigns one writer at a time.

## Status and ownership

- Backlog ID:
- Status:
- Current owner and next handoff:

## Problem and scope — PM

- Target user and problem:
- Desired outcome:
- In scope:
- Out of scope:
- Assumptions, dependencies, and unresolved decisions:

## Acceptance criteria — PM

Assign stable IDs such as AC-01. Describe observable behavior, including important failure cases. Distinguish confirmed requirements from proposals.

| ID | Scenario or precondition | Action | Expected result |
| --- | --- | --- | --- |

## Experience — UX Designer

- Entry points and primary flow:
- Screens, interactions, and navigation:
- Relevant loading, empty, error, success, and permission states:
- Responsive behavior, keyboard use, focus, labels, and feedback:
- Visual references or artifacts, if needed:
- Requirement ambiguities or proposed changes:

## API contract and integration — Backend and Frontend Developers

For features spanning both areas, record the contract before dependent implementation. Omit this section when there is no API boundary.

- API operations, request and response shapes:
- Authentication expectations, validation, and error behavior:
- Contract location and owner; shared file ownership:
- Integration owner and dependencies:
- Mocked behavior versus actual backend integration:

## Backend implementation — Backend Developer

- Approach and relevant decisions:
- Changed files and setup details:
- Relevant data, API, or migration behavior:
- Checks executed and their results:
- Known limitations and QA handoff:

## Frontend implementation — Frontend Developer

- Approach and relevant decisions:
- Changed files and setup details:
- UI states, accessibility, and API consumption:
- Checks executed and their results:
- Known limitations and QA handoff:

## Integration handoff — Assigned integration owner

- Backend and frontend versions or snapshot:
- Real user flows checked and results:
- Remaining mocks, blockers, or unverified behavior:

## Verification — QA

- Implementation version or snapshot tested:
- Environment and prerequisites:

| Criterion | Scenario and method | Result: pass / fail / blocked / not run | Evidence |
| --- | --- | --- | --- |

### Defects

For each defect include an ID, severity and user impact, reproduction steps, expected and actual behavior, evidence, and status. Record recheck evidence when fixed.

### Coverage gaps and verdict

State what was verified, what remains unverified, and whether the acceptance criteria are met. Record the reason for each blocked or unexecuted check.

## Completion — Coordinator

- Outcome against agreed scope:
- Remaining limitations or follow-up work:
- Backlog and decision log updated:
