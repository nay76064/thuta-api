# API workspace boundaries

- This workspace owns authentication, listing validation and authorization, search, and persistence. Keep client presentation in `../app` and communicate through the JSON HTTP API.
- Stack: TypeScript, Express, and SQLite via `better-sqlite3`. Keep endpoint behavior suitable for both web and the planned mobile client.
- Validate all user input on the server. Enforce owner access for listing changes, protect private account data, and store only password hashes.
- Production requires a private `JWT_SECRET`; configure allowed origins deliberately. Never commit secrets or real user data.
- Follow repository-level architecture and constraints in [../AGENTS.md](../AGENTS.md); product behavior is specified in [../SPEC.md](../SPEC.md).
- Keep `README.md` user-facing and `CLAUDE.md` as a pointer to the repository guidance.
