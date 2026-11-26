# Specification workflow

Use this skill when a task requires discovery, requirement clarification, or a feature specification.

1. Read root instructions, product context, and existing specs/ADRs.
2. Understand the user problem and desired outcome; do not assume implementation details are requirements.
3. Identify scope, non-goals, constraints, privacy implications, dependencies, unresolved questions, and risks.
4. Describe flows, states, edge cases, and failure paths.
5. Write testable acceptance criteria (observable outcomes, not vague statements).
6. Break large capabilities into small vertical slices. Each slice should have independent acceptance criteria, scope, and verification strategy; prioritize foundational slices and dependencies.
7. Keep specification language implementation-agnostic unless an approved architecture decision constrains it.
8. Link related documents and avoid duplicated requirements.
9. Mark draft/proposed status clearly; don't imply approval.

Deliver a spec plus unresolved questions and a proposed slice sequence. Do not begin implementation unless the task explicitly includes it and the spec/decision context is sufficient.
