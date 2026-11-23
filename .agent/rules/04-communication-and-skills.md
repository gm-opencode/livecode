---
trigger: always_on
description: Rules requiring clarifying questions on ambiguity and presenting available skills for user selection.
---

# Rule 04: Clarifications & Skill Selection

## 1. Always Ask Clarifying Questions (Rule 7)

- **Never guess** when requirements, user intent, edge cases, design preferences, or technical trade-offs are unclear.
- Before implementing ambiguous tasks, stop and ask concise, concrete questions (prefer structured choices with a recommended default when helpful).
- Record confirmed decisions in `docs/PRD.md` or `docs/SPECIFICATIONS.md` so the same question does not need to be asked twice across sessions or platforms.

## 2. Skill Discovery & User Selection (Rule 10)

- Whenever starting a development task or new workstream where the user has **not** explicitly specified or already selected which skills to use:
  1. Inspect all installed and available skills (e.g., via `list_skills`).
  2. Filter and list the available skills that may be relevant to the requested work, including a brief description of each.
  3. Ask the user to select which skill(s) they want enabled/used for this development work before proceeding with implementation.
- Once the user has selected skills for a task or project phase, record the active skill choices in `docs/SPECIFICATIONS.md` (under *Active Skills / Tooling*) and honor them until the user changes them or a new phase begins.
