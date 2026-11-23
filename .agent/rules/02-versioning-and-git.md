---
trigger: always_on
description: Mandatory versioning increment rules and branch-per-version Git/GitHub workflow (no PRs, no merges).
---

# Rule 02: Versioning & Git / GitHub Workflow

## 1. Version Numbering Scheme

- Format: `MAJOR.MINOR.PATCH` (`X.Y.Z`).
- **Baseline:** The initial repository setup (rules and starter documentation on `baseline` / `main`) is the pre-release baseline (`0.0.0` / baseline).
- **First Development Version:** The first functional change/development request starts at **`0.0.1`**.
- **Increment Rule:** After **every** change or development request, increment the version by `+0.0.1`.
- **Base-10 Rollover Rule:**
  - Patch digit rolls over after `9`:
    - `0.0.1` → `0.0.2` → ... → `0.0.9` → **`0.1.0`** → `0.1.1` → ...
  - Minor digit rolls over after `9`:
    - `0.1.9` → `0.2.0` → ... → `0.9.9` → **`1.0.0`** → `1.0.1` → ...

### Quick Reference Sequence

```text
0.0.1 -> 0.0.2 -> ... -> 0.0.8 -> 0.0.9 -> 0.1.0 -> 0.1.1 -> ... -> 0.1.9 -> 0.2.0 -> ... -> 0.9.9 -> 1.0.0
```

## 2. Git & GitHub Branching Policy

- **Branch Naming Convention:** `v<X.Y.Z>` (for example: `v0.0.1`, `v0.0.2`, `v0.1.0`).
- **One Branch Per Version:**
  - Every version must be committed and pushed to **its own dedicated branch** on GitHub.
  - Each new version should branch from the latest completed version branch (or `baseline` / `main` for `v0.0.1`) so work builds cleanly and sequentially, unless the user explicitly specifies a different base branch.
- **Strictly Prohibited Actions (Unless Explicitly Requested by User):**
  - **Do NOT create a Pull Request (PR).**
  - **Do NOT merge** version branches into `main` or into other branches.
  - **Do NOT force-push** or rewrite history on previously pushed version branches.

## 3. Commit Standards

- Include the version number clearly in the commit message (e.g., `v0.0.1: <concise summary of changes>`).
- Ensure all required documentation updates (`README.md`, `docs/PRD.md`, `docs/SPECIFICATIONS.md`, `docs/help/*`) are included in the version commit before pushing.
- Delegate Git and GitHub operations to the Git/GitHub sub-agent using **Hydrogen (High)** (see `01-agent-models.md`).
