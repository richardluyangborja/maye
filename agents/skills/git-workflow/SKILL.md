# Git workflow

## Branch model
- `main` is the only long-lived branch.
- Use short-lived `feature/<name>` branches for all work; no develop/release branches.
- Do not work directly on main.
- Start from current main; keep feature scope focused.

## Suggested sequence
1. Confirm clean working tree and current main state.
2. Update main from its remote if the repository is connected and permitted.
3. Create a focused feature branch.
4. Make small, reviewable commits. Conventional prefixes encouraged: `feat`, `fix`, `test`, `docs`, `refactor`, `chore`.
5. Before merge, inspect the diff and run required tests/checks. Review for secrets, scope creep, security, documentation and regression risk.
6. Ensure the branch is up to date with main and resolve conflicts; re-run affected checks.
7. Merge only when all required checks have passed, review is complete, and merge is authorized. Agents may merge their own branches when the task authorizes it and requirements are met.
8. Prefer a normal merge or squash merge based on repository policy; never force-push or rewrite main history.
9. Delete the merged feature branch after merge.

## Gate
**No merge if required checks fail, are skipped, or are unverified.** If a check cannot run, report the limitation and do not claim the branch is merge-ready. For automated repository settings, configure branch protection when hosting is established; agent instructions alone cannot enforce server-side protection.

## Reporting
Report branch, commits, diff scope, tests/checks and results, merge status, and cleanup. Never invent CI status.
