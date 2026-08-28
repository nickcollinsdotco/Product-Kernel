# Decision System

Product Kernel treats decisions as explicit project objects.

## Decision lifecycle

A useful default lifecycle is:

```text
UNKNOWN
   ↓
ASSUMED
   ↓
INVESTIGATING
   ↓
DECIDED
   ↓
VALIDATED
```

These states describe knowledge quality, not workflow progress.

## Unknown

We do not currently know the answer.

Example:

> We do not know whether users understand the difference between a template and a card.

## Assumed

We have a working hypothesis but insufficient evidence.

Example:

> We assume users expect a saved template to remain independent from the original card.

Assumptions should be visible rather than disguised as decisions.

## Investigating

We are actively gathering information.

Possible evidence includes:

* user research
* behavioural observation
* competitive analysis
* prototype testing
* technical experiments
* browser testing

## Decided

The project has deliberately selected a direction.

A decision should normally include:

### Decision

What was chosen.

### Why

The rationale.

### Evidence

What informed the choice.

### Consequence

What this means for design, product and implementation.

### Status

Decided.

## Validated

The decision has been tested against meaningful evidence.

Validation does not necessarily mean permanent truth.

It means the decision has survived the relevant test.

## Decision template

```md
# Decision: [Name]

## Decision

[What was decided]

## Why

[Why this direction was selected]

## Evidence

[What evidence informed the decision]

## Consequences

[What follows from the decision]

## Revisit when

[What new evidence or condition would justify reopening it]

## Status

Decided
```

## Reopening decisions

A decision is not sacred.

It should be reconsidered when:

* new evidence contradicts it
* user behaviour changes
* product strategy changes
* technical constraints change materially
* another decision makes it inconsistent
* implementation exposes a flaw in the original reasoning

When reopening a decision, preserve the previous record rather than erasing history.

## Important rule

> A decision should make future work easier, not merely make the current conversation feel finished.
