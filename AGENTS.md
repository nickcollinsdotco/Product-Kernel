# AGENTS.md

## Project

Product Kernel is a meta-context framework for autonomous AI-assisted product design and development.

Read `context/PROJECT.md` for the project identity and intent.

## Before significant work

Read:

* `context/PROJECT.md`
* `context/PRINCIPLES.md`
* `context/CURRENT-STATE.md`
* `context/DECISIONS.md`
* `context/OPEN-QUESTIONS.md`

Then inspect relevant feature, design and technical context.

## Working principle

Do not assume that an implementation request contains a fully resolved product decision.

When meaningful ambiguity exists, identify it before encoding it into code or UI.

## Product reasoning

Use the Product Kernel methodology and Layers-inspired reasoning when:

* the problem is ambiguous
* multiple product directions are plausible
* terminology is unclear
* the conceptual model is unclear
* the interaction is uncertain
* repeated UI fixes are failing
* implementation complexity suggests a deeper product problem

Do not use the full methodology for trivial changes.

## Persistent context

Important decisions belong in durable project context.

Capture decisions, rationale, evidence, consequences and open questions.

Do not capture entire conversations.

## Implementation

Once product intent is sufficiently clear:

* implement coherently
* preserve established constraints
* keep unrelated work separate
* test the result
* review against the relevant context

## Validation

Do not treat passing tests as proof that the product is correct.

Use browser or real-product validation for meaningful UI and interaction work.

## Synchronisation

When work changes the documented project state, update the relevant context.

Outdated context is a defect.

## Escalation

Surface rather than silently decide when work would materially change:

* product intent
* conceptual model
* established terminology
* major scope
* major architecture
* important user or business behaviour

## Priority

When instructions conflict, prefer:

1. explicit current project intent
2. current documented decisions
3. current implementation evidence
4. feature-specific context
5. assumptions

If a conflict cannot be resolved confidently, make it visible rather than inventing certainty.
