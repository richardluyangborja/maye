# Maye

Maye is a private, shared digital scrapbook for two partners: a cozy place to preserve memories, celebrate milestones, share letters and questions, and build a record of their relationship.

This repository is the **agent-ready project foundation**. It establishes product context, boundaries, working conventions, and workflows. Detailed feature specifications, architecture decisions, plans, and implementation are intentionally delegated to agents in small, reviewed tasks.

## Start here
1. Read [`AGENTS.md`](AGENTS.md) for the universal agent contract.
2. Read [`docs/README.md`](docs/README.md) to navigate project context.
3. Review the relevant skill(s) under [`agents/skills`](agents/skills/README.md).
4. Before doing feature work, locate or create an approved spec and decision records as appropriate.

## Current stage
- [x] Product vision and v1 direction captured
- [x] Candidate technology baseline documented
- [x] Agent workflows and Git rules established
- [ ] Detailed feature specifications
- [ ] Architecture decisions (ADRs)
- [ ] Implementation plans and code

Do not treat this repository context as a substitute for feature specifications or approved ADRs. Agents should identify unresolved questions instead of silently inventing answers.

## Product and technical context
See `docs/context/` and `docs/architecture/` for the initial context and candidate stack. Stack choices are a baseline to validate and record in ADRs—not a license to introduce additional services or complexity without justification.

## Git workflow
- `main` is the integration branch.
- Use short-lived `feature/<concise-name>` branches for changes.
- No routine develop, release, or long-lived feature branches.
- Merge only after the required checks pass and review is complete.
- Delete feature branches after merge.
- Never commit secrets, generated credentials, or local environment files.

## Working philosophy
- Build the smallest useful slice.
- Write tests before implementation (RED → GREEN → REFACTOR).
- Prefer boring, maintainable solutions.
- Validate behavior, permissions, and failure cases—not just happy paths.
- Never claim a check passed unless it was actually run.
