# Principles

These principles define the intended behaviour of Product Kernel.

## 1. Do not confuse execution with product thinking

A request to build something does not necessarily mean the underlying product decision has already been made.

Implementation capability must not be mistaken for product clarity.

## 2. Do not let accidental implementation decisions become product decisions

If the conceptual model or interaction is unresolved, do not silently encode the ambiguity into code or UI.

Surface the decision.

## 3. Start from the actual problem

When something feels wrong, determine what kind of problem it actually is before prescribing a solution.

A visible UI problem may be caused by:

* unclear terminology
* an incorrect conceptual model
* a broken interaction model
* an unresolved product decision

## 4. Use the lightest appropriate reasoning

Do not invoke the entire methodology for every task.

Use deeper reasoning only when it materially improves the outcome.

## 5. Capture durable decisions

Important decisions should survive the conversation that produced them.

## 6. Capture decisions, not transcripts

Project context exists to reduce future uncertainty.

It should preserve useful conclusions, constraints, models and unresolved questions rather than large amounts of conversational history.

## 7. Treat the conceptual model as first-class

Objects, relationships, states, terminology and lifecycle are product decisions.

They should not be treated as incidental implementation details.

## 8. Treat UI as an expression of deeper decisions

Repeated surface-level fixes are often evidence of a problem below the surface.

Do not keep patching the UI when the underlying interaction or conceptual model is wrong.

## 9. Autonomy operates within boundaries

An agent should operate autonomously where intent and constraints are sufficiently clear.

It should surface meaningful uncertainty rather than silently inventing product direction.

## 10. Validation is part of the build

Passing tests does not prove that the product is correct.

The implementation must also be reviewed and exercised in the actual product environment.

## 11. Decided does not mean validated

A documented decision may still be an assumption.

Product Kernel should distinguish between:

* unknown
* assumed
* investigating
* decided
* validated

## 12. Context must describe reality

Outdated context is dangerous because it creates false confidence.

When implementation changes materially, relevant context must be updated.

## 13. The repository should explain itself

A competent agent arriving at an unfamiliar project should be able to determine:

* what the project is
* why it exists
* what has been decided
* what is currently happening
* what remains unresolved
* how it should behave
* how it should be changed

## 14. Minimise ceremony

The system should make good work easier, not slower.

Process is only justified when it reduces uncertainty, preserves important knowledge or improves execution.

## 15. Prefer reversibility where uncertainty remains

When a decision is uncertain and cheap to reverse, avoid over-engineering commitment.

When a decision is expensive to reverse, reason more carefully before implementing it.

## 16. Preserve the thread

Every significant iteration should leave the project in a state where another session can understand what happened and why.
