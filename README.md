# Product Kernel

**A meta-context vibecoding framework for autonomous design + development.**

AI coding agents can design and build increasingly sophisticated software. The problem is no longer simply getting an agent to write code. The harder problem is giving it enough persistent understanding to make good product decisions while it works.

Product Kernel is a lightweight operating system for that.

It connects **product reasoning, persistent context, autonomous implementation, and validation** into one continuous workflow.

```text
              PRODUCT INTENT
                    │
                    ▼
              PRODUCT REASONING
                    │
                    ▼
             PERSISTENT CONTEXT
                    │
                    ▼
          AUTONOMOUS DESIGN + DEV
                    │
                    ▼
             REVIEW + VALIDATION
                    │
                    ▼
             UPDATED CONTEXT
                    │
                    └───────────┐
                                ▼
                         NEXT ITERATION
```

## The idea

Most AI development workflows start here:

```text
"Build this UI."
        ↓
      Claude
        ↓
       Code
```

That works until the product becomes complicated.

At that point, the agent needs to understand things that rarely fit inside a single prompt:

* what the product is trying to achieve
* who it is for
* what users are actually doing
* what important concepts and objects mean
* why previous decisions were made
* how the product should behave
* what constraints are non-negotiable
* what is currently being built
* what has already been tried
* what changed since the last session

Product Kernel treats that information as **first-class project infrastructure**.

## Three systems

### 01 — Think

Use structured product reasoning before implementation when the problem is ambiguous or consequential.

The core principle is:

> Don't let an unresolved product decision become an implementation decision by accident.

The methodology is heavily influenced by **Layers by Jamie Mill**, particularly its approach to reasoning across observation, domain, user needs, strategy, conceptual model, interaction and surface.

Layers should not be treated as a rigid checklist. Use the layer that contains the actual problem.

A UI that feels wrong may be a UI problem.

Or it may be a conceptual-model problem disguised as a UI problem.

## 02 — Remember

Important decisions should survive the conversation that produced them.

Product Kernel maintains durable project context covering areas such as:

```text
context/
├── project/
├── design/
├── features/
├── technical/
└── developer/
```

This becomes the persistent memory surrounding the codebase.

The conversation is the working surface.

The repository is the memory.

Capture decisions, constraints, terminology, models and useful state rather than entire conversations.

This part is heavily influenced by **Archē by Josh Millgate**, particularly its approach to persistent project context and context-driven development workflows.

## 03 — Build

Once product decisions are sufficiently resolved, the work moves into implementation.

The development loop is deliberately more disciplined than:

```text
prompt → code → ship
```

Instead:

```text
scope
  ↓
specify
  ↓
build
  ↓
review
  ↓
test
  ↓
browser / UAT
  ↓
update context
```

When implementation exposes a deeper product ambiguity, move back into reasoning instead of patching around the problem.

This creates a loop rather than a pipeline.

## The operating principle

Product Kernel separates three things that AI-assisted development often collapses together:

### Intent

**What should exist, and why?**

### Context

**What does the agent need to know in order to make good decisions?**

### Execution

**How should the system actually be implemented and validated?**

The agent can then operate autonomously within a set of explicit product and technical constraints.

```text
             INTENT
                │
                ▼
             CONTEXT
                │
                ▼
            EXECUTION
                │
                ▼
           VALIDATION
                │
                ▼
             CONTEXT
```

## When to use it

Use the methodology when:

* a feature is ambiguous
* several reasonable product directions exist
* the UI keeps becoming more complicated
* terminology is inconsistent
* users are misunderstanding something
* Claude keeps fixing symptoms rather than causes
* a feature involves meaningful states, objects or relationships
* a decision will be expensive to reverse later
* a project spans many AI sessions
* several people or agents need shared context

Do not add ceremony to trivial work.

A typo does not need product strategy.

A spacing adjustment does not need a conceptual-model workshop.

The goal is to apply deeper reasoning **only where it changes the quality of the outcome**.

## The deeper principle

The most important idea in this project is simple:

> **AI agents do not just need instructions. They need a model of the product they are operating inside.**

As agents become more autonomous, persistent context becomes increasingly important.

Without it, every session partially reconstructs the product from scratch.

With it, the agent can build on accumulated decisions instead of repeatedly rediscovering them.

## Relationship to Layers and Archē

Product Kernel is an independent synthesis of ideas from existing work.

### Layers

[Jamie Mill](https://layers.jamiemill.com/)

Provides the product-design reasoning model.

### Archē

[Josh Millgate](https://github.com/joshmillgate/arche)

Provides the persistent project-context and development workflow model.

Product Kernel combines these ideas into a single workflow focused on AI-native product development.

It does not attempt to replace either project.

## Project structure

A typical implementation can look like:

```text
project/
├── src/
│
├── context/
│   ├── project/
│   ├── design/
│   ├── features/
│   ├── technical/
│   └── developer/
│
├── .claude/
│   ├── skills/
│   └── commands/
│
├── README.md
├── LICENSE
└── .gitignore
```

The exact structure is intentionally flexible.

The principle matters more than the folder names:

**important product knowledge should live somewhere persistent, legible and version-controlled.**

## Example

A request such as:

> "Let users save cards as templates."

looks like an implementation task.

Before writing code, the system may need to resolve:

```text
What is a card?

What is a template?

Is a template a copy, a preset, or another first-class object?

Can a template be edited?

Can a card continue to inherit from a template?

What happens when the source changes?

What happens when a template is deleted?

What states can a template occupy?

How does the user discover and manage templates?
```

Those decisions affect the data model, interaction model, UI, and implementation.

The methodology therefore tries to resolve the important conceptual decisions first, preserve them in project context, and then let the coding agent execute against them.

## Design principles

### Don't jump straight to the screen

A screen is the visible expression of deeper decisions.

### Treat the conceptual model as first-class

Objects, relationships, states and terminology often matter more than individual components.

### Capture decisions, not transcripts

The useful residue of a design conversation should survive.

### Use the lightest process that solves the problem

Methodology should reduce uncertainty, not create bureaucracy.

### Let agents operate within explicit constraints

Autonomy works better when intent, context and boundaries are clear.

### Pull back when the UI becomes a patchwork

Repeated surface fixes are often evidence of a deeper problem.

### Keep context synchronized with reality

Documentation that describes a previous version of the product is worse than no documentation.

### Validate the actual product

Generated code is not proof that the experience works.

## Status

Early and experimental.

This project is being developed in public as an evolving personal methodology for AI-native product development.

Expect the structure, terminology and workflow to change as it is used on real products.

## License

MIT
