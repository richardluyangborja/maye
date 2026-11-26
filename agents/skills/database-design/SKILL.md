# Database design

- Candidate DB: PostgreSQL with Prisma; validate decisions in ADRs.
- Read domain specs and data-model docs before schema changes.
- Model relationship-space membership and access boundaries explicitly; avoid cross-couple data leakage.
- Use relational constraints, transactions, indexes and migrations intentionally.
- Store calendar dates as date types when semantics are calendar dates; carefully model timestamps/timezones.
- Keep media binaries outside the database; store metadata and object references.
- Test constraints, migrations, transactions and queries against a real disposable/local PostgreSQL instance where practical.
- Never use destructive migration/testing commands against production data.
