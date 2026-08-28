# Current State

Updated: 2026-08-29

## Framework maturity

Early experimental system.

The core ideas have been established, but the exact structure, skill architecture and workflow are still being developed through real use.

## Working

* Product reasoning is treated as distinct from implementation.
* Layers is used as the primary conceptual model for diagnosing product ambiguity.
* Archē is used as a major reference for persistent project context and disciplined build workflows.
* Important decisions are intended to be stored as durable Markdown.
* The repository is intended to be usable publicly, not only as a private personal workflow.
* The framework should support autonomous implementation without pretending that all product decisions can be delegated.

## Current direction

The system is being shaped around four connected capabilities:

1. Reason
2. Remember
3. Execute
4. Validate

The intended loop is:

```text
orient
→ identify uncertainty
→ reason
→ decide
→ capture
→ build
→ review
→ validate
→ update context
→ repeat
```

## In progress

* Canonical context architecture
* Product Kernel skill architecture
* Reasoning-to-build handoff
* Decision capture conventions
* Autonomous execution boundaries
* Validation model
* Worked examples

## Open design areas

* Exact relationship between Product Kernel and Archē
* Exact relationship between Product Kernel and Layers
* Which parts belong in core skills versus supporting skills
* Which commands are genuinely useful
* How much orchestration should be automated
* Whether context should remain purely Markdown or eventually gain structured metadata
* How framework context should differ from project-specific context
* How the system should behave across different AI coding agents

## Current bias

Prefer a small, composable system over a large framework.

Prove the methodology on real projects before adding infrastructure.

## Definition of progress

The project is progressing when the system demonstrably helps an AI agent:

* make fewer accidental product decisions
* preserve important reasoning across sessions
* identify deeper problems earlier
* implement within established constraints
* recover project state quickly
* produce better validated outcomes
