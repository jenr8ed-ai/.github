---
domain: governance/fsad
dash_validated: false
status: draft
---

# Dash Governance

## Purpose

`dash_validated` + `status` frontmatter provides the single control point for what is allowed to flow into public publishing, automation, or archives.

## The Governance Gate

From automation code (e.g. publish_all.py, substack_publisher.py):

```python
# FSAD governance gate
if not (meta.get("dash_validated") is True and meta.get("status") == "Draft"):
    logger.info("SKIPPED %s (governance gate...)", ...)
    return False
```

Only files explicitly marked `dash_validated: true` **and** `status: Draft` are eligible for publishing pipelines.

After successful publish, the file is typically updated to `status: Published` (via atomic move or edit) and re-committed.

## Directory Structure & Domains

- `relations/engineering/`
- `relations/content/`
- `relations/master_tasks/`
- `relations/revenue/`
- `relations/events/`, `marketing/affiliates/...` etc.

Each file declares its `domain:` to enable targeted scanning.

## Workflows

1. Capture / draft in staging (dash_validated: false initially ok during heavy editing).
2. Human + agent review → set `dash_validated: true`, `status: Draft`.
3. Run publisher / orchestrator.
4. Post-publish: update status and move to archive where appropriate.

## Dash Tooling

- `dash/` docker-compose runs the `adamoutler/dash` service (port 8080) for local dashboard views.
- Engineering portal and other surfaces may consume FSAD records.

## Enforcement Notes

- Never bypass the gate in scripts.
- Agent prompts must surface the requirement to set proper frontmatter.
- Violations are treated as infrastructure / governance bugs (see issue template).

See also fsad-architecture.md and the SOT notebook in the main workspace.