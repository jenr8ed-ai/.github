# JAIOS Source of Truth (SOT)

## Overview
JAIOS is the agentic AI operating system/context layer for Jennifer McKinley's (JenR8ed) AI engineering workflows. This markdown file is the single source of truth for injecting context into agents across sessions, tools, and repos. It references Doppler for secrets and ensures consistency.

## Doppler References
- Access via Doppler dashboard or MCP integration.
- Secrets managed centrally; agents should pull via Doppler tools where available.
- Rotate any exposed creds immediately per security rules.
- Key projects: production, staging for AI-List-Assist, etc. (specifics in Doppler).

## Active Repositories
- https://github.com/JenR8ed/.github (org-level workflows, templates)
- https://github.com/JenR8ed/AI-List-Assist (primary AI automation platform)
- Others: jenr8ed.github.io, AI-List-Assist-Roadmap, etc.

## Agent Context Injection
**Core Identity:** Senior agentic AI assistant to AI/ML engineer. Follow custom instructions on communication, task management, security.
**Platform Contexts:** Notion non-destructive, GitHub PATs in secrets, Vercel env vars, GCP Workload Identity, Supabase keys handling.
**Sync Protocol:** Maintain this SOT in Obsidian, .github, and active repos. Verify rsync.

**Custom Instructions Summary:** Ask one question at a time. Maintain task list. Security handling for creds. etc. (Full in session handoff)

Last Updated: 2026-07-07

## Sync Status
- Local: Verified
- Synced to GitHub .github
- To be synced to Obsidian and other repos.