# Decisions

This file records durable decisions about Product Kernel itself.

These are framework decisions, not ordinary implementation tasks.

---

## D-001 — Separate product reasoning from implementation

### Decision

Product Kernel explicitly separates product reasoning from implementation.

### Why

AI agents can implement ambiguous requests extremely well. That does not mean the ambiguity should have been resolved by code.

### Consequence

The workflow must be able to pause implementation and return to product reasoning whenever a meaningful unresolved decision appears.

### Status

Decided

---

## D-002 — Use Layers diagnostically rather than procedurally

### Decision

Product Kernel should not require all Layers to be traversed for every feature.

### Why

The purpose of the Layers model is to identify where the current problem actually exists.

### Consequence

Use the smallest useful reasoning intervention.

### Status

Decided

---

## D-003 — Persistent context is part of the product-development system

### Decision

Project context should be version-controlled alongside the codebase.

### Why

Important product and technical decisions need to survive individual conversations and sessions.

### Consequence

Context is treated as project infrastructure rather than temporary notes.

### Status

Decided

---

## D-004 — Capture decisions rather than transcripts

### Decision

Durable context should store useful residue from reasoning rather than raw conversation history.

### Why

The purpose of context is future decision support, not historical reproduction.

### Consequence

Context documents should prioritise conclusions, rationale, consequences, constraints and open questions.

### Status

Decided

---

## D-005 — Validation includes the real product

### Decision

Automated tests are necessary but insufficient.

### Why

Implementation correctness does not prove that the user experience or product behaviour is correct.

### Consequence

The workflow should include browser or equivalent real-environment validation.

### Status

Decided

---

## D-006 — Open questions are first-class context

### Decision

Unresolved decisions should be recorded explicitly rather than being silently resolved by the agent.

### Why

Uncertainty that is visible can be reasoned about. Uncertainty hidden inside implementation becomes expensive to discover later.

### Consequence

`OPEN-QUESTIONS.md` is part of the canonical context structure.

### Status

Decided

---

## D-007 — Product Kernel should remain agent-oriented rather than vendor-specific

### Decision

The core methodology should not depend conceptually on Claude Code.

### Why

The underlying problem is broader than one agent or interface.

### Consequence

Claude-specific skills and commands may exist, but the conceptual model should remain portable.

### Status

Decided
