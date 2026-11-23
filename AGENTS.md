# AGENTS.md — Development Rules & Project Guidelines

This file defines the mandatory development rules, orchestration policies, versioning workflow, and documentation standards for the **livecode** repository. It is intended for **Antigravity** and any other AI coding agent or platform working on this project.

Detailed rule modules for Antigravity are also located in [`.agent/rules/`](.agent/rules/).

---

## Core Rules Summary

### 1. Model & Agent Orchestration
1. **Planning & Orchestration:** Use **Neon** at **Extra High** (*Ekstra høy*).
2. **Development & Implementation Sub-agents / Swarm:** Use **Neon** at **High** (*Høy*).
3. **Git & GitHub Sub-agent:** Use **Hydrogen** at **High** (*Høy*).

> See [`.agent/rules/01-agent-models.md`](.agent/rules/01-agent-models.md) for full details.

### 2. Versioning & Git / GitHub Workflow
4. **Sequential Versioning (`X.Y.Z`):**
   - Increment the version number by `0.0.1` after **every** change or development request.
   - Start the first functional development version at **`0.0.1`**.
   - Rollover rule: after `0.0.9`, increment to **`0.1.0`**, then continue incrementing by `0.0.1` (`0.1.1`, ..., `0.1.9` → `0.2.0`; `0.9.9` → `1.0.0`).
5. **Branch-Per-Version Policy (No PR / No Merge):**
   - Commit and push **every version to its own GitHub branch** using the naming convention `v<X.Y.Z>` (e.g., `v0.0.1`, `v0.0.2`, `v0.1.0`).
   - **Do NOT create a Pull Request (PR)** and **do NOT merge** branches automatically.

> See [`.agent/rules/02-versioning-and-git.md`](.agent/rules/02-versioning-and-git.md) for full details.

### 3. Documentation, Help Guides & Specifications
6. **README & Version Changelog:**
   - Update [`README.md`](README.md) with all necessary project information after every version.
   - Always include/update the **Version History / Changelog** section describing the exact changes introduced in each version.
8. **Bilingual Help Documentation / User Guide:**
   - Continuously create and update user-facing help documentation intended to be integrated into the web app as Help Text / User Guide.
   - Maintain **both Norwegian and English** versions in sync:
     - Norwegian: [`docs/help/brukerveiledning.no.md`](docs/help/brukerveiledning.no.md)
     - English: [`docs/help/user-guide.en.md`](docs/help/user-guide.en.md)
9. **Product Requirements & Technical Specifications (Cross-Platform Continuity):**
   - Continuously create and update [`docs/PRD.md`](docs/PRD.md) and [`docs/SPECIFICATIONS.md`](docs/SPECIFICATIONS.md) so development can be seamlessly resumed from other platforms or tools at any time.

> See [`.agent/rules/03-documentation-and-specs.md`](.agent/rules/03-documentation-and-specs.md) for full details.

### 4. Clarification & Skill Selection
7. **Always Ask When Unclear:**
   - Always ask clarifying questions whenever requirements, design choices, edge cases, or instructions are unclear or ambiguous. Do not make silent assumptions.
10. **Skill Discovery & User Selection:**
    - If the user has not already specified or selected skills for the current development task, list all installed and available skills that may be relevant, and ask the user to choose which skills should be used before proceeding.

> See [`.agent/rules/04-communication-and-skills.md`](.agent/rules/04-communication-and-skills.md) for full details.

---

## Language Convention

| File Category | Language |
| --- | --- |
| Rules, technical docs, `README.md`, `docs/PRD.md`, `docs/SPECIFICATIONS.md`, code & comments | **English** |
| Help documentation / User Guide (`docs/help/`) | **Norwegian (`brukerveiledning.no.md`) AND English (`user-guide.en.md`)** |

---

## Repository Structure

```text
.
├── AGENTS.md                        # Root development rules (Antigravity & cross-platform)
├── README.md                        # Project overview, setup, and version changelog
├── .agent/
│   └── rules/
│       ├── 01-agent-models.md       # Model & effort rules for orchestrator and sub-agents
│       ├── 02-versioning-and-git.md # Versioning scheme and Git/GitHub branch rules
│       ├── 03-documentation-and-specs.md # README, PRD, specs, and bilingual help guide rules
│       └── 04-communication-and-skills.md # Clarification policy and skill selection workflow
└── docs/
    ├── PRD.md                       # Product Requirements Document
    ├── SPECIFICATIONS.md            # Technical Specifications & handoff state
    └── help/
        ├── brukerveiledning.no.md   # User Guide / Help Text (Norwegian)
        └── user-guide.en.md         # User Guide / Help Text (English)
```

---

## Mandatory Per-Request Workflow Checklist

Before starting and before finishing **every** development or change request, verify:

- [ ] **Clarifications (Rule 7):** Are all requirements unambiguous? If not, ask the user first.
- [ ] **Skills (Rule 10):** Has the user selected skills for this work? If not, list relevant installed skills and let the user choose.
- [ ] **Models (Rules 1–3):** Planning/orchestration uses Neon (Extra High); dev sub-agents/swarm use Neon (High); Git/GitHub sub-agent uses Hydrogen (High).
- [ ] **Implementation:** Changes are built and verified.
- [ ] **Documentation (Rules 6, 8, 9):**
  - [ ] `docs/PRD.md` updated (if product scope/requirements changed).
  - [ ] `docs/SPECIFICATIONS.md` updated (architecture, decisions, current version, handoff state).
  - [ ] `docs/help/brukerveiledning.no.md` and `docs/help/user-guide.en.md` updated in sync.
  - [ ] `README.md` updated including the new version entry in the changelog.
- [ ] **Versioning & Git (Rules 4, 5):**
  - [ ] Version incremented properly (`0.0.1` → ... → `0.0.9` → `0.1.0` → ...).
  - [ ] Committed and pushed to its own branch `v<X.Y.Z>` on GitHub.
  - [ ] **No PR created and no merge performed.**
