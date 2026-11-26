# Test-driven implementation workflow

Mandatory default for implementation and bug fixes.

1. Read instructions, skill(s), spec, ADRs, plan and current code.
2. Choose one small vertical slice with clear acceptance criteria.
3. Write a test that captures the desired behavior and fails for the expected reason (**RED**).
4. Implement the smallest change to pass (**GREEN**).
5. Refactor with behavior preserved; keep tests passing (**REFACTOR**).
6. Run relevant unit, integration, lint, type-check and other applicable checks. Use real PostgreSQL integration tests for database behavior.
7. Review privacy, authorization, error paths, boundary cases, accessibility where applicable, and regressions.
8. Update docs and propose next slice if needed.

Do not weaken/delete tests, skip failing checks, or claim unrun checks passed. If test-first is infeasible, document why and seek approval when material.
