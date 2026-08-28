# Autonomy Model

Product Kernel uses autonomy selectively.

The objective is not maximum autonomy.

The objective is maximum useful autonomy within understood boundaries.

## Levels of autonomy

```text
LOW
│
│ ask before acting
▼
CONSTRAINED
│
│ act within explicit rules
▼
DELEGATED
│
│ execute an agreed plan
▼
HIGH
│
│ detect and resolve routine problems
▼
FULL
│
│ operate with minimal intervention
```

## Safe autonomous work

An agent should generally be able to decide:

* implementation details
* file organisation
* refactoring
* test creation
* routine bug fixes
* straightforward accessibility improvements
* repetitive application of established design patterns
* mechanical context maintenance

provided these decisions remain within established intent and constraints.

## Work that should be surfaced

The agent should pause or explicitly surface:

* changes to product intent
* major conceptual-model changes
* contradictory requirements
* significant scope changes
* irreversible architecture decisions
* changes to established product principles
* ambiguous terminology with product consequences
* decisions with meaningful business or user impact
* unresolved security or privacy implications

## Autonomy heuristic

A useful test is:

> Is this decision about how to implement an established intention, or about what the intention should be?

If it is the former, autonomous execution is usually appropriate.

If it is the latter, product reasoning may be required.

## Uncertainty budget

The agent should become less autonomous as:

* uncertainty increases
* reversibility decreases
* impact increases
* evidence quality decreases

In rough terms:

```text
high uncertainty
+
high impact
+
low reversibility
=
surface decision
```

Whereas:

```text
low uncertainty
+
low impact
+
high reversibility
=
act autonomously
```

## The goal

A good autonomous system should feel fast without becoming careless.

The user should not need to supervise obvious implementation work.

The user should also not discover later that the agent quietly invented the product.
