# Philosophy

## The problem is changing

Traditional software tools assumed that people perform most product reasoning and most implementation work.

AI coding agents change that division of labour.

Agents can now:

* inspect unfamiliar codebases
* create interfaces
* change architecture
* implement features
* write tests
* debug failures
* run development tools
* evaluate their own work
* iterate rapidly

This creates a new problem.

The bottleneck shifts from:

> Can the system produce the code?

towards:

> Does the system understand what it should be producing?

## Code is not the whole product

A codebase contains implementation knowledge.

It does not necessarily contain:

* why the product exists
* why a particular interaction was chosen
* what users actually need
* which assumptions are unvalidated
* why a concept has a particular name
* which tradeoffs were deliberate
* which questions remain unresolved

Those things often live temporarily inside human heads and AI conversations.

Product Kernel treats them as persistent project knowledge.

## Product context as infrastructure

The phrase "context" is often used loosely in AI systems.

Product Kernel gives it a more specific role.

Context is the information that allows an agent to make a better decision than it could make from the immediate prompt and code alone.

That includes:

* intent
* knowledge
* state
* constraints
* decisions
* unresolved questions

## Autonomy requires boundaries

Greater autonomy does not mean giving an agent permission to invent product direction.

The useful form of autonomy is:

> **Freedom of execution inside a sufficiently understood problem space.**

The agent should be able to make routine decisions without interruption.

The agent should not silently make consequential decisions that change what the product is.

## The product reasoning problem

When a UI is wrong, the natural response is often to edit the UI.

That is not always correct.

A useful diagnostic hierarchy is:

```text
surface
  ↓
interaction
  ↓
conceptual model
  ↓
strategy
  ↓
user need
  ↓
domain
  ↓
observed behaviour
```

Layers provides the primary conceptual inspiration for this diagnostic approach.

The important principle is not the hierarchy itself.

It is the habit of asking:

> Is the problem actually at the level where it first appears?

## Persistent evolution

A project should become more understandable over time, not less.

Every major iteration should add useful knowledge while removing uncertainty.

The ideal long-term effect is:

```text
more decisions
+
more evidence
+
more context
+
less repeated reasoning
+
less accidental inconsistency
```

That is the purpose of the system.
