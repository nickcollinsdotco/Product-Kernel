# Open Questions

This file contains unresolved decisions about Product Kernel.

These are not ordinary tasks.

An open question represents uncertainty that may affect the shape, philosophy or future architecture of the system.

---

## Q-001 — What should Product Kernel own versus delegate?

There is currently a conceptual overlap with Archē.

Question:

Should Product Kernel eventually own the full reasoning-to-validation lifecycle, or should it primarily be the product reasoning and context layer that can delegate execution to systems such as Archē?

Status: Open

---

## Q-002 — What is the canonical unit of context?

Possibilities include:

* documents
* structured records
* linked records
* a hybrid system

Current bias:

Keep the underlying representation simple and human-readable unless real use demonstrates the need for more structure.

Status: Open

---

## Q-003 — How autonomous should an agent be?

The system needs a clear boundary between:

* decisions the agent can make autonomously
* decisions the agent can make within explicit constraints
* decisions that require human confirmation
* decisions that should trigger deeper product reasoning

Status: Open

---

## Q-004 — How much should context be automatically updated?

Potential approaches:

* manual synchronisation
* agent-generated summaries
* automatic state extraction
* hybrid

Current bias:

Automate routine updates but keep meaningful product decisions explicit.

Status: Open

---

## Q-005 — Should Product Kernel reproduce the Layers skills?

Current position:

No.

Product Kernel should use Layers as an influence and integrate with its reasoning model, but should avoid unnecessarily duplicating or republishing another project's implementation.

Status: Open

---

## Q-006 — Should Product Kernel reproduce the Archē workflow?

Current position:

No.

Archē is a strong reference model for project memory and development workflow. Product Kernel should develop its own abstraction around reasoning, context and autonomy rather than becoming an Archē fork.

Status: Open

---

## Q-007 — What is the minimum viable Product Kernel?

The system should be tested without assuming that a large number of skills, commands, agents or integrations are necessary.

Question:

What is the smallest set of files and instructions that produces a measurable improvement in AI-assisted product work?

Status: Open

---

## Q-008 — How should evidence affect decisions?

A decision may be:

* assumed
* reasoned
* observed
* tested
* validated

Question:

Should evidence and confidence become explicit metadata in the decision system?

Status: Open

---

## Q-009 — How should Product Kernel represent contradictions?

A mature project will eventually contain conflicting context.

Question:

How should an agent detect and surface contradictions between:

* current code
* documented decisions
* design guidance
* feature specifications
* project principles

Status: Open
