# Decisions

## D-001 — Product reasoning and implementation are separate phases

### Decision

Product Kernel explicitly separates product reasoning from implementation.

### Why

AI agents are extremely capable at implementing an ambiguous request.
That does not mean the ambiguity should have been resolved by code.

### Consequence

The workflow must be able to pause implementation and return to
product reasoning.

---

## D-002 — Layers is used diagnostically, not procedurally

### Decision

Do not require all seven Layers to be traversed for every feature.

### Why

Layers is designed around identifying the current bottleneck.

### Consequence

The agent should select the smallest useful reasoning intervention.
