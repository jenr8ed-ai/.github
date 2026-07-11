---
domain: governance/fsad
status: draft
dash_validated: false
---

# FSAD Architecture (File-System-as-Database)

*Source of truth adapted from Dev Notebook SOT 03_Zero_Token_FSAD.md and related automation.*

## 1. Local Database Schema

To bypass external platform overhead and maintain absolute data sovereignty, all system relations are tracked locally via plain-text markdown records within version-controlled storage directories.

State changes are explicitly logged across four key database sectors:

* `relations/engineering/` — Infrastructure configurations, script schemas, and baseline audits.
* `relations/content/` — Automation templates, prompt rules, and output text dumps.
* `relations/master_tasks/` — Cross-domain activity timelines and target workflows.
* `relations/revenue/` — E-commerce tracking analytics and link performances.

(Additional sectors such as events, marketing/affiliates, projects/ under the relations root follow the same pattern.)

## 2. Data Lifecycle Rules

* **Atomic Processing**: System state records must be directly moved, never loosely duplicated, between staging directories, production vaults, and final archival storage.
* **Workspace Isolation**: All agent run scripts and execution blocks are strictly quarantined within the secure filesystem loop (`~/secure_agent_workspace/`) to prevent host system pollution.
* **Frontmatter Governance Gate**: Every file intended for publishing or automation **must** carry:
  ```yaml
  ---
  domain: <path/category>
  dash_validated: true
  status: Draft | Published | Archived
  ---
  ```

See [dash-governance.md](dash-governance.md) for the enforcement details in publishing scripts.

## 3. Zero-Token / Zero-Credential Mandate

- No secrets of any kind in git.
- `.env` and local credential stores only.
- All sync (Supabase ↔ FSAD, Dropbox ↔ FSAD, etc.) must respect this.

## 4. Implementation Examples

- Publishing automation (`01-20260623-PublishingAutomation`)
- Sync scripts (`05_*_Data_Sync_Scripts`, `07_*`)
- Agent context library lives alongside but does not duplicate state.

This architecture enables full reproducibility and auditability without reliance on any single cloud vendor for core state.