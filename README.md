# livecode

> **Current Version:** `0.0.0` (Baseline setup on `baseline` — first functional release will start at `v0.0.1`)

## Overview

**livecode** is currently initialized with its foundational development rules, workflow specifications, and documentation templates. The application requirements and implementation will be specified and built iteratively starting with `v0.0.1`.

---

## Project Documentation

| Document | Purpose |
| --- | --- |
| [`AGENTS.md`](AGENTS.md) | Root development rules and checklist for Antigravity and cross-platform AI agents |
| [`.agent/rules/`](.agent/rules/) | Modular Antigravity workspace rule files |
| [`docs/PRD.md`](docs/PRD.md) | Product Requirements Document (maintained continuously) |
| [`docs/SPECIFICATIONS.md`](docs/SPECIFICATIONS.md) | Technical Specifications and cross-platform handoff guide |
| [`docs/help/brukerveiledning.no.md`](docs/help/brukerveiledning.no.md) | In-app Help Text / User Guide (Norwegian) |
| [`docs/help/user-guide.en.md`](docs/help/user-guide.en.md) | In-app Help Text / User Guide (English) |

---

## Development Workflow Summary

All development follows the rules defined in [`AGENTS.md`](AGENTS.md) and [`.agent/rules/`](.agent/rules/):

- **Agent Models:** Planning & orchestration on **Neon (Extra High)**; development sub-agents/swarm on **Neon (High)**; Git & GitHub sub-agent on **Hydrogen (High)**.
- **Versioning:** Increments by `+0.0.1` per request (`0.0.1` → ... → `0.0.9` → `0.1.0` → ...).
- **Git / GitHub:** Each version is committed and pushed to its own branch (`v<X.Y.Z>`). No automatic PRs or merges.
- **Documentation:** `README.md` (including changelog), `docs/PRD.md`, `docs/SPECIFICATIONS.md`, and bilingual user guides (`docs/help/`) are updated continuously.
- **Clarifications & Skills:** Always ask when requirements are unclear, and list relevant installed skills for user selection when not yet specified.

---

## Version History / Changelog

### `0.0.0` (Baseline) — `baseline` *(2026-11-23)*
- Added root development rules in [`AGENTS.md`](AGENTS.md).
- Added modular Antigravity rules in [`.agent/rules/`](.agent/rules/):
  - `01-agent-models.md`
  - `02-versioning-and-git.md`
  - `03-documentation-and-specs.md`
  - `04-communication-and-skills.md`
- Created starter documentation templates for cross-platform continuity and future in-app help:
  - [`docs/PRD.md`](docs/PRD.md)
  - [`docs/SPECIFICATIONS.md`](docs/SPECIFICATIONS.md)
  - [`docs/help/brukerveiledning.no.md`](docs/help/brukerveiledning.no.md)
  - [`docs/help/user-guide.en.md`](docs/help/user-guide.en.md)
- Updated `README.md` with project overview, documentation index, workflow summary, and version changelog section.
