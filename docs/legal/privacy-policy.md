---
domain: governance/legal
status: draft
dash_validated: false
---

# Privacy Policy

**Effective Date:** 2026-07-02

## Overview

JenR8ed / JAIOS prioritizes data sovereignty and minimal data collection.

We operate on a **zero-credential repository policy** and **FSAD (File-System-as-Database)** model. Personal and operational data lives in local markdown files under version control within `secure_agent_workspace/relations/` (and mirrored only where explicitly chosen by the owner).

## What Data We Collect

- Public GitHub profile and commit data (standard for any open source activity).
- Data you explicitly publish via approved automation (after `dash_validated: true` gate).
- Analytics on public sites (see littlelink privacy page for example usage of privacy-focused tools like Fathom).

No third-party cookies or trackers are added without disclosure.

## How Data Is Stored & Protected

- All sensitive state is kept in the local FSAD. No passwords/tokens/API keys are ever stored in git.
- Atomic file moves between staging / production / archive.
- Cloud services (Google Sheets, Cloudflare Pages, Apps Script) are used only for specific public or convenience surfaces and contain only the minimum necessary public data.

## Your Rights

- Request deletion or correction of any published content by opening an issue or contacting the maintainer.
- Because the primary store is local FSAD under your control (as the owner), you retain full sovereignty.

## Changes

This policy is maintained in `docs/legal/privacy-policy.md` of the `.github` repo and applies org-wide.

## Contact

jen.mckinley@gmail.com