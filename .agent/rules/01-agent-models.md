---
trigger: always_on
description: Model and reasoning effort selection rules for planning, orchestration, development sub-agents, and Git/GitHub operations.
---

# Rule 01: Agent Models & Orchestration

All AI agent execution in this project must follow these model and reasoning effort assignments:

| Role / Responsibility | Model | Reasoning Effort |
| --- | --- | --- |
| **Planning & Orchestration** (main coordinator, architecture, task breakdown, review) | **Neon** | **Extra High** (*Ekstra høy*) |
| **Development & Implementation** (sub-agents or agent swarm writing/testing code and docs) | **Neon** | **High** (*Høy*) |
| **Git & GitHub Operations** (sub-agent handling branching, commits, pushes, status checks) | **Hydrogen** | **High** (*Høy*) |

## Operational Guidelines

1. **Orchestrator:** Keep high-level planning, specification updates, ambiguity detection, and final verification on **Neon (Extra High)**.
2. **Implementation Sub-agents / Swarm:** Delegate coding, refactoring, test writing, and modular implementation tasks to sub-agents configured with **Neon (High)**.
3. **Git / GitHub Sub-agent:** Delegate repository versioning, branch creation (`v<X.Y.Z>`), staging, committing, and pushing to a dedicated Git/GitHub sub-agent configured with **Hydrogen (High)**.
4. If the runtime environment does not expose these exact model tier identifiers programmatically, note the active platform mapping transparently while adhering to the same separation of roles.
