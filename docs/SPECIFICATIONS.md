# Technical Specifications — livecode

> **Status:** Baseline / Pre-development  
> **Current Version:** `0.0.0` (Baseline on `baseline`)  
> **Next Version & Branch:** `v0.0.1`  
> **Last Updated:** 2026-11-23

---

## 1. Cross-Platform Handoff Summary

This specification is maintained continuously alongside [`docs/PRD.md`](PRD.md) so that any engineer or AI coding platform can resume work immediately with full context.

- **Repository:** `gm-opencode/livecode`
- **Mandatory Rules:** See [`AGENTS.md`](../AGENTS.md) and [`.agent/rules/`](../.agent/rules/)
- **Current State:** Foundational `.md` rules and documentation structure committed to branch `baseline`. No application code has been written yet.
- **Next Step:** Await the user's product specification, clarify any open questions (Rule 7), confirm relevant skills (Rule 10), and begin development on branch `v0.0.1`.

---

## 2. Active Skills & Tooling

- **Selected Skills:** *None selected yet — must be presented to and confirmed by the user at the start of development (Rule 10).*
- **Agent Model Policy (Rules 1–3):**
  - Planning & Orchestration: **Neon (Extra High)**
  - Development & Implementation Sub-agents / Swarm: **Neon (High)**
  - Git & GitHub Sub-agent: **Hydrogen (High)**

---

## 3. Tech Stack & Dependencies

*To be decided once the product specification is provided.*

| Layer | Technology | Notes |
| --- | --- | --- |
| Frontend | *TBD* | Web application |
| Backend / API | *TBD* | — |
| Database / Storage | *TBD* | — |
| Styling / UI | *TBD* | — |
| Testing | *TBD* | — |
| Build / Deployment | *TBD* | — |

---

## 4. Architecture Overview

*To be defined in `v0.0.1`.*

---

## 5. Directory Structure

```text
.
├── AGENTS.md                        # Cross-platform & Antigravity rules entry point
├── LICENSE
├── README.md                        # Project overview & version changelog
├── .agent/
│   └── rules/
│       ├── 01-agent-models.md
│       ├── 02-versioning-and-git.md
│       ├── 03-documentation-and-specs.md
│       └── 04-communication-and-skills.md
└── docs/
    ├── PRD.md                       # Product Requirements Document
    ├── SPECIFICATIONS.md            # Technical Specifications (this file)
    └── help/
        ├── brukerveiledning.no.md   # In-app Help / User Guide (Norwegian)
        └── user-guide.en.md         # In-app Help / User Guide (English)
```

---

## 6. Data Models & API Contracts

*To be documented as schemas and endpoints are designed.*

---

## 7. Help Text & Localization Integration

- End-user help documentation is authored in Markdown under `docs/help/`:
  - Norwegian: [`docs/help/brukerveiledning.no.md`](help/brukerveiledning.no.md)
  - English: [`docs/help/user-guide.en.md`](help/user-guide.en.md)
- Both files must keep matching sections and anchors so the web app can load, render, or bundle them cleanly as in-app Help Text / User Guide.

---

## 8. Environment & Local Development Setup

*Setup, run, build, and test commands will be added once the application stack is initialized.*

---

## 9. Testing & Verification Strategy

*To be defined alongside the chosen tech stack.*

---

## 10. Architectural Decision Log (ADR)

| Date | Version | Decision | Rationale |
| --- | --- | --- | --- |
| 2026-11-23 | `0.0.0` (Baseline) | Store rules in both `AGENTS.md` and `.agent/rules/*.md`. | Ensures native Antigravity rule discovery while remaining portable across other AI platforms. |
| 2026-11-23 | `0.0.0` (Baseline) | Use English for technical docs and maintain both Norwegian and English for end-user help guides. | User preference for international technical handoff with bilingual in-app user documentation. |
| 2026-11-23 | `0.0.0` (Baseline) | Commit initial rules/templates to `baseline` (ready for manual merge to `main`); start versioned branching at `v0.0.1` using `v<X.Y.Z>` naming. | Keeps project foundation separate from versioned feature branches while respecting `main` branch protection and enforcing strict branch-per-version history from the first feature request. |
