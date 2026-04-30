<!--
Document : SPECIFICATIONS_GLOBAL.md
Author : Bruno DELNOZ
Email : bruno.delnoz@protonmail.com
Version : v1.0.0
Date : 2026-04-30 00:00 UTC
-->

# Purpose
Define the stable baseline for the GitHub Pages portfolio repository.

# Global scope
Portfolio content, Jekyll page structure, styling constraints, and governance files.

# Stable verified repository behavior
- Main public portfolio page is maintained in `index.md`.
- Jekyll front matter uses `layout: default`.
- Profile content follows CV/portfolio narrative with badges, expertise sections, and structured Markdown tables.
- `AGENTS.md` is governance and must remain immutable unless explicitly requested.
- `CLAUDE.md` must remain a symlink to `AGENTS.md`.

# Repository architecture
- Root Markdown pages and governance docs.
- Static style with `style.css`.
- Jekyll config in `_config.yml`.

# Global functional requirements
- Portfolio pages must remain professional, structured, and readable.
- Project listings should be categorized and descriptive.

# Global non-functional requirements
- No sensitive data disclosure.
- Maintain readability and consistent formatting.

# Global inputs
- Repository files.
- Publicly available metadata when accessible.

# Global outputs
- Portfolio Markdown pages.
- Specification documents.

# Global files and directories
- `index.md`, `index.new.md`, `_config.yml`, `style.css`, `AGENTS.md`, `CLAUDE.md`, `SPECIFICATIONS*.md`.

# Global interfaces and commands
- Git CLI for version control.
- Local shell tooling.

# Global constraints and safety rules
- Do not modify protected files unless explicitly authorized.
- Never expose secrets from private repositories.

# Global validation and acceptance criteria
- Protected files unchanged.
- New portfolio files keep professional style and structure.

# Task-scoped specification boundary
Task-specific content refreshes belong in `SPECIFICATIONS.md` and `SPECIFICATIONS_FR.md`.

# Out-of-scope items
- Source code changes in other repositories.
- Styling/system config changes.

# Changelog
- v1.0.0 | 2026-04-30 00:00 UTC | Bruno DELNOZ
  - Added: Initial global baseline specification from current repository state.
  - Modified: N/A.
  - Removed: N/A.
  - Reason: Initialize mandatory global specification baseline.

- v1.0.1 | 2026-04-30 00:00 UTC | Bruno DELNOZ
  - Added: Baseline note that portfolio repository inventory can be rebuilt from controlled owner inventory when live API access is unavailable.
  - Modified: Validation focus on avoiding stale repository counts in generated portfolio pages.
  - Removed: N/A.
  - Reason: Corrective quality pass after user feedback.
