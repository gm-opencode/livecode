---
trigger: always_on
description: Rules for maintaining README.md changelog, bilingual user help documentation, PRD, and technical specifications.
---

# Rule 03: Documentation, Help Guides, PRD & Specifications

Every development iteration must keep project documentation, user guides, requirements, and technical specifications completely up to date.

## 1. `README.md` Updates (Rule 6)

- Keep `README.md` accurate with project description, setup/run instructions, architecture highlights, and links to key documentation.
- Maintain a dedicated **Version History / Changelog** section in `README.md`.
- For every new version (`v0.0.1`, `v0.0.2`, etc.), add an entry summarizing:
  - Version number and branch name (`v<X.Y.Z>`)
  - Date
  - Concise bullet list of all changes introduced in that version.

## 2. Bilingual Help Documentation / User Guide (Rule 8)

- Continuously create and update end-user help documentation that will later be embedded or loaded directly into the web application as **Help Text / User Guide**.
- Maintain **both Norwegian and English** files in parallel:
  - **Norwegian:** `docs/help/brukerveiledning.no.md`
  - **English:** `docs/help/user-guide.en.md`
- Formatting guidelines for easy future web-app integration:
  - Keep identical section structures and stable heading hierarchy across both languages.
  - Write clear, jargon-free explanations aimed at end users.
  - Whenever a UI feature, workflow, setting, or shortcut is added or modified, update **both** help files in the same version.

## 3. Product Requirements & Technical Specifications (Rule 9)

To ensure development can be effortlessly resumed from **any other AI platform, IDE, or developer workstation**, maintain:

1. **Product Requirements Document (`docs/PRD.md`):**
   - Product vision, goals, target users, user stories, functional & non-functional requirements, out-of-scope items, and open questions.
2. **Technical Specifications (`docs/SPECIFICATIONS.md`):**
   - Current version and active branch, tech stack, dependencies, system architecture, folder structure, data models, API contracts, UI/i18n structure, environment setup, test strategy, and architectural decision log.

## 4. Language Policy

- **English:** All technical documentation (`AGENTS.md`, `.agent/rules/*`, `README.md`, `docs/PRD.md`, `docs/SPECIFICATIONS.md`), commit messages, and code/comments.
- **Norwegian + English:** Help documentation / User Guide (`docs/help/brukerveiledning.no.md` and `docs/help/user-guide.en.md`).
