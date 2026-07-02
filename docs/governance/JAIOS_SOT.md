---
domain: governance/sot
status: draft
dash_validated: false
---

# JAIOS Single Source of Truth (SOT)

*Compiled from 08_2026-06-08_Dev_Notebook_SOT/ and agents/ library (2026-07).*

This document is the living root reference for the JenR8ed AI Operating System (JAIOS) and all related projects. All agent prompts, manifests, and docs should reference sections here.

## 1. Environment Setup & Key Authorization (01)

- **Reasoning Engine**: Google One AI Premium / Gemini Advanced primary.
- **eBay Developer Program**: Sandbox keysets configured per-account to avoid throttling.
- **Data Layer Security**: Strict zero-credential repository policy. All secrets via local `.env` only. No tokens/passwords in git.
- Sandbox verification handshake for baseline checks.

## 2. Operational Workflows & The Capture Loop (02)

**Phase 1: High-Speed Mobile Capture**
- Visual ingestion (4-6 high-res photos).
- OCR via iOS Live Text.
- iCloud staging with timestamp.

**Phase 2: Structural Serialization**
- Gemini processing with standardized prompts.
- JSON export: SEO title ≤ 80 chars + structured metadata ready for marketplace ingestion.

## 3. Zero-Token FSAD (03)

See dedicated `fsad-architecture.md` and `dash-governance.md`.

Core sectors under `relations/`:
- engineering/
- content/
- master_tasks/
- revenue/
- events/, marketing/affiliates/ etc.

Atomic moves + frontmatter gates.

## 4. Device-Specific Interaction Protocols (04)

- **Mobile / Voice**: High-level summaries only. No raw code blocks (audio-safe).
- **Desktop / Compute**: High-density technical payloads.
- Two-step exchange for voice: Brief (narrative) then explicit "Drop the code" payload request.

## 5. Media Production & Affiliate Publishing Rules (05)

- Vertical video: 9:16, 1080x1920 min, safe zones, 15-34s length.
- Affiliate storytelling: Problem-Solution narrative, link in first comment only, mandatory #ad / #affiliate disclosure.

## Agent Library (relations/engineering/projects/agents/)

**Core files** (paste into any tool's project instructions):
- `project-context.md` (universal)
- `orchestrator.md` + `routing.yaml`
- Specialist: `github.md`, `frontend.md`, `testing.md`, `documentation.md`, `architecture.md`

**Key Rules** (selected):
- No branch protection or required reviews in solo repos unless escalated.
- Commit messages: short imperative. Body only for non-obvious why.
- No automated test suite yet; produce manual QA checklist per change.
- Functional React only, plain CSS, preserve slug logic exactly.
- `agent.manifest.yaml` is the machine source of truth; keep README in sync.
- Escalate missing specialists to roadmap rather than inventing.

## Architecture Decisions (preserve unless explicitly changed)

- Sheets-as-database for current scale (writing-hub / links).
- Cloudflare Pages + Apps Script for edge + backend (no full server).
- Client-side dedupe (last row wins).

Any change to datastore, auth model, or hosting requires ADR in `architecture.md`.

## JAIOS Relationship

This library and governance is written in JAIOS-compatible shape (manifest + routing + role files) so it can plug into the future reusable JAIOS generator repo. It does not depend on a separate JAIOS runtime today.

## How to Extend

- Add new agent only when `roadmap_trigger` in manifest becomes true.
- Update SOT, agents/, and any affected FSAD entries in one atomic change set.
- Always run the relevant manual verification steps from `testing.md`.

**Maintained in**: JenR8ed/.github (this file) + workspace 08_2026-06-08_Dev_Notebook_SOT/ and agents/.

Update this file when core SOT sections evolve.