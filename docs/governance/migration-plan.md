---
domain: governance
status: draft
dash_validated: false
---

# Migration Plan

## Goals

Migrate legacy or ad-hoc data sources into the canonical FSAD structure under `relations/` while preserving history, auditability, and sovereignty.

## Principles

- Atomic moves preferred over copy.
- Every migrated record receives proper domain + dash_validated + status frontmatter.
- Existing published artifacts (e.g. on Substack, YouTube, TikTok) are referenced by pointer records rather than duplicated.
- Zero new credential dependencies introduced.

## Current State (as of 2026-07)

- Core relations/ sectors populated for engineering, content, master_tasks, revenue, events, marketing/affiliates.
- Sync tools exist: Supabase ↔ FSAD, Dropbox ↔ FSAD (Antigravity Orchestrator).
- Publishing automation respects governance gate.
- Some legacy Google Sheets usage remains for the writing-hub / links dashboard (intentionally kept for current scale).

## Phased Plan

1. **Inventory** (current)
   - Scan all workspaces and external sources for state that should live in FSAD.
   - Document in master_tasks/ or a dedicated migration log.

2. **Relations Structure Hardening**
   - Standardize subfolder naming and frontmatter across all domains.
   - Add JAIOS_SOT references where appropriate.

3. **Tooling Alignment**
   - Update all sync and publish scripts to use the new canonical paths.
   - Ensure `dash` and engineering portal surface the full picture.

4. **Legacy Cutover**
   - For each old system: one-time atomic migration + verification.
   - Update any hard-coded paths in agents / orchestrators.

5. **Verification & SOT Update**
   - Run full publishing dry-runs.
   - Update `docs/governance/JAIOS_SOT.md` and fsad-architecture.md with final layout.
   - Close migration issues.

## Risks & Mitigations

- Data loss during move → always keep git history + external backup (Dropbox archive).
- Agent context drift → keep agent library in sync via documentation agent.

See Dev Notebook SOT and relations/ for detailed current layout.