# JAIOS — JenR8ed AI Operating System

**JAIOS** (JenR8ed AI Operating System) is a reusable, vendor-neutral agent operating system.

It provides generators that produce adapters per AI platform (ChatGPT Projects, Claude Projects, Cursor rules, etc.) from a single source of truth: manifests, routing, and role files.

## Core Principles

- **Zero-credential / Zero-token policy**: No secrets, passwords, or API keys in any repository. All auth via local `.env` only.
- **FSAD (File-System-as-Database)**: All state tracked in plain-text markdown under `relations/` with explicit frontmatter governance (`dash_validated: true`, `status: Draft|Published|Archived`).
- **Atomic data lifecycle**: Records moved (never duplicated) between staging, production, and archive.
- **Privacy by design & data sovereignty**: Local-first, no unnecessary cloud datastores. Google Sheets used only where already in place for simplicity at current scale.
- **Agent roles are composable**: Specialist agents (orchestrator, frontend, github, testing, documentation, architecture) + routing for multi-step tasks.

## Relationship to Repositories

This `.github` repository holds org-wide governance, templates, and legal docs that apply across JenR8ed projects and the future JAIOS ecosystem.

See [JAIOS_SOT.md](../docs/governance/JAIOS_SOT.md) and [fsad-architecture.md](../docs/governance/fsad-architecture.md) for the full single source of truth.

Maintained by Jennifer McKinley (@JenR8ed).