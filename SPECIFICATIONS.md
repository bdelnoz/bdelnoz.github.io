<!--
Document : SPECIFICATIONS.md
Author : Bruno DELNOZ
Email : bruno.delnoz@protonmail.com
Version : v1.0.0
Date : 2026-04-30 00:00 UTC
-->

# Purpose
Rebuild `index.new.md` as a complete professional portfolio page, preserving the style and structure of `index.md` while refreshing the GitHub repository portfolio section.

# Scope
- Create `index.new.md` in English.
- Preserve `index.md` unchanged.
- Keep protected files unchanged.
- Include full repository inventory provided by the user, with categorized presentation.

# Existing verified behavior
- `index.md` contains a CV-style portfolio with profile header, badges, category tables, and long-form professional sections.
- No specification files were present before this task.

# Functional requirements
- `index.new.md` must keep Jekyll front matter and profile structure.
- GitHub section must be fully refreshed and categorized.
- All repositories from provided inventory must be represented individually.
- Forks must be explicitly marked as forks.
- Private projects must be listed without exposing private URLs or sensitive content.

# Non-functional requirements
- Professional, non-generic writing.
- No banned low-quality phrases.
- No sensitive information leakage.

# Inputs
- `AGENTS.md` rules.
- Existing `index.md` style model.
- User-provided repository inventory.
- Limited local environment tooling (no `gh` available).

# Outputs
- `SPECIFICATIONS.md` (English).
- `SPECIFICATIONS_FR.md` (French synchronized companion).
- `index.new.md` (English portfolio draft).

# Files and directories concerned
- `SPECIFICATIONS_GLOBAL.md`
- `SPECIFICATIONS.md`
- `SPECIFICATIONS_FR.md`
- `index.new.md`

# Interfaces and commands
- Shell tools (`sed`, `cat`, `python3`, `git`).

# Constraints and safety rules
- Do not edit `index.md`, `AGENTS.md`, `style.css`, `_config.yml`.
- Do not expose private repo internals.
- Do not invent unsupported technical claims.

# Validation and acceptance criteria
- `index.new.md` exists and is in English.
- Protected files remain unchanged.
- Inventory entries are individually represented and forks marked.
- No banned low-quality fallback phrases appear.

# Out-of-scope items
- Modifying external repositories.
- Changing site CSS or Jekyll config.

# Changelog
- v1.0.0 | 2026-04-30 00:00 UTC | Bruno DELNOZ
  - Added: Task-scoped specification for portfolio reconstruction.
  - Modified: N/A.
  - Removed: N/A.
  - Reason: User-approved rebuild of `index.new.md`.
