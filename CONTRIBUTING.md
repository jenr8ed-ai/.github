# Contributing

Thank you for your interest in contributing to JenR8ed projects and the JAIOS ecosystem.

## Governance & Legal

All contributions are governed by the documents in `docs/legal/` and `docs/governance/`:

- [Privacy Policy](https://github.com/JenR8ed/.github/blob/main/docs/legal/privacy-policy.md)
- [Terms of Service](https://github.com/JenR8ed/.github/blob/main/docs/legal/terms-of-service.md)
- [Jurisdiction Addendum](https://github.com/JenR8ed/.github/blob/main/docs/legal/jurisdiction-addendum.md)
- Client Services Agreement and Grant templates

## FSAD Governance

This organization uses **FSAD** (File-System-as-Database) for all state.

- Source files live under `relations/` (engineering, content, master_tasks, revenue, etc.).
- Every publishable record **must** include frontmatter:
  ```yaml
  ---
  domain: <category/sub>
  dash_validated: true
  status: Draft | Published | Archived
  ---
  ```
- Use the publishing automation only on files that pass the governance gate (`dash_validated: true` + `status: Draft`).
- Never commit secrets. Follow zero-credential policy.

## Development Process

See the agent library (orchestrator + specialists) and `docs/governance/JAIOS_SOT.md` for how work is structured.

- Reference relevant SOT sections in commits and PRs.
- Use the provided issue and PR templates.
- Keep agent role files, manifests, and human docs in sync.
- Manual verification replaces automated CI for now.

## Code of Conduct

Be respectful. This is primarily a solo / small-team agent-augmented workflow. Agent outputs are always reviewed by a human before publication or merge.

## Questions

Open an issue using the appropriate template or reference this repo's docs.