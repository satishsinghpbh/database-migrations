# Review rules for database-migrations

Org baseline (OWASP ASVS / NIST SSDF mapped, from the `engineering-ai` plugin) applies: data loss and breaking schema changes are blocking. Repo-specific rules below.

## Blocking
- Modifying or deleting an already-applied changeset.
- Changeset without a rollback, or with a destructive change (`dropTable`, `dropColumn`, type narrowing) and no data backup or migration plan.
- Environment-specific values (hosts, passwords) hardcoded instead of coming from CI/CD variables.
- Non-backward-compatible schema change with no expand/contract plan for running applications.

## Non-blocking
- Diagram and wording improvements in `README.md`.
- Changeset naming and file organization.
