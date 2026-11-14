# database-migrations

Liquibase CI/CD reference architecture for managing database schema changes across environments. Currently documentation only (`README.md`).

Org-wide standards come from the `engineering-ai` Devin plugin; this file adds repo-specific rules. Review rules: `.github/REVIEW.md`.

## Commands
- No build or tests yet. TODO: add Liquibase changelogs and a `liquibase validate` / `update-sql` check when code is added.

## Repo-specific rules
- Mermaid diagrams in `README.md` must render on GitHub; check the syntax before committing.
- When changelogs are added: never edit a changeset that has already been applied; add a new one instead.
- Every changeset needs an `id`, an `author` and a rollback (explicit `<rollback>` or an auto-rollback-capable change type).
