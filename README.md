# jenr8ed-ai/.github — Organization Governance & Community Health

> **This is a special repository** for the `jenr8ed-ai` GitHub Organization. Files here apply org-wide as defaults for all repositories.

[![Org](https://img.shields.io/badge/Org-jenr8ed--ai-0A0F1C?style=for-the-badge)](https://github.com/jenr8ed-ai)
[![Portfolio Hub](https://img.shields.io/badge/Portfolio-jenr8ed.github.io-0A2A4A?style=for-the-badge)](https://jenr8ed.github.io)
[![Governance](https://img.shields.io/badge/Governance-Dash%20CI-5EEAD4?style=for-the-badge)](#-dash-ci-governance)

### What lives here

| Path | Purpose |
| :--- | :--- |
| `profile/README.md` | **Org profile** that renders at `github.com/jenr8ed-ai` |
| `.github/workflows/dash-ci.yml` | Enforces `get_status` + `get_logs` + Zero-Bloat (.env block) |
| `.github/workflows/sanitize.yml` | Runs `python sanitize.py` credential scan on every PR |
| `.github/CODEOWNERS` | `@jenr8ed` owns all governance changes |
| `JAIOS_SOT.md` | Central Agent Context Source of Truth |
| `grok-system-prompt.md` | Handoff prompt for Grok / Meta AI agents |

### Architecture Governed: 3-Pillar FSAD

All agent work is localized in `~/secure_agent_workspace/` on WSL2/Ubuntu — **Zero-Deviation Rule**.

- **Pillar 1: Infrastructure & Governance** → Docker, Cloudflare Tunnels, Dash CI, wikis — `pillar1-infra/`
- **Pillar 2: Product Development (AI List Assist)** → LangGraph, multi-modal workflows, inventory validation — `pillar2-product/`
- **Pillar 3: Growth & Monetization** → Affiliate funnels (Coursera/Google, Amazon/Impact) + LinkedIn Newsletter / Discord — `pillar3-growth/`

### 🛡️ Zero-Bloat Mandate (Enforced in CI)

```bash
# BLOCKED in CI
.env
.env.*
.env.local
# SECRETS MUST USE
Vercel Dashboard → Environment Variables
Colab → Secrets Manager
# PRE-PUSH
python sanitize.py
```

### 🔄 Dash CI Governance

Every autonomous agent write in this org is gated by the Dash container:

1. `get_status` — verify `~/secure_agent_workspace/` state
2. `get_logs` — tail 100 lines, check for errors
3. Commit only after both pass
4. Headless UI via Playwright only — no manual clicking
5. Naming: `[Function]-[Stack]-[Version]` e.g., `Audit-Claude-v2`

### 🚀 Org Featured Repos

- **AI-Agentic-Terminal-Portfolio** → Prod: `ai-agentic-terminal-portfolio.vercel.app` (Vercel, no iframe wrappers)
- **Gemini Trusted Tester Evaluation Prep** → Study Notebook + Deliverables A/B
- **Google Drive Pipeline + FSAD SOPs** → Gmail Academic, Drive, Notion workflows
- **Grant Writing & Funding Research** → Notion SOT index

> **Portfolio Stability Rule:** No AI Studio iframe wrappers — they hit CSP blocking & auth walls. Live demos deploy to **Hugging Face Spaces**, **Cloudflare Pages**, and **Vercel**.

### 📁 How to use this repo

This repo was imported from `JenR8ed/.github` to seed `jenr8ed-ai` org with same guardrails.

To update org profile:
1. Edit `profile/README.md`
2. Commit to `main`
3. Profile appears at https://github.com/jenr8ed-ai within 1 minute

To update org-wide workflows:
1. Edit `.github/workflows/*.yml` here
2. They auto-apply to all new repos in org (opt-in for existing repos via reuse)

### 🔗 Ecosystem Links

- Personal Hub: [jenr8ed.github.io](https://jenr8ed.github.io)
- Newsletter: [GenAI Revenue Plays](https://www.linkedin.com/newsletters/genai-revenue-plays)
- Personal Gov Repo: [JenR8ed/.github](https://github.com/JenR8ed/.github)
- Figma: [figma.com/@jenr8ed](https://figma.com/@jenr8ed)

---
**Maintained by:** @jenr8ed — Oakland, CA — QA-minded, community-driven, grant-backed R&D
**Method:** Built in Oakland. Shipped via Vercel. Governed by Dash CI. No bloat.
