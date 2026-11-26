# Privacy, quality, and engineering principles

## Privacy and security
- Relationship-space data must be isolated; every relevant request verifies membership and resource-level permissions.
- Authentication and authorization are separate concerns. A valid login does not imply access to a couple's data.
- Media must remain private; use short-lived access where appropriate and avoid public object URLs.
- Validate inputs and uploads; constrain file type, size, and processing.
- Avoid logging private memory content, credentials, tokens, or sensitive data.
- Protect invitation, authentication, upload, and other sensitive flows with appropriate abuse controls.
- Design account deletion, relationship-space deletion, export, backup, and restoration deliberately.

## Reliability
- Push notifications are delivery mechanisms, not canonical state.
- Handle upload failures, retries, cancellation, incomplete uploads, and orphaned storage objects.
- Dates representing anniversaries or memory dates should be modeled deliberately as calendar dates when appropriate; avoid accidental timezone shifts.
- Plan migration and data integrity checks for relational data.

## Quality
- Test behavior and meaningful edge cases, including permission boundaries.
- Integration tests should use a real disposable/local PostgreSQL database where DB semantics matter.
- Test before implementing; do not weaken tests to force a pass.
- Accessibility, responsive layouts, performance, and maintainability are quality requirements.
- Coverage numbers are a signal, not the goal.
