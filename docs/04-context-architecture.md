# Context Architecture

## What context means

In Product Kernel, context is the durable information an agent needs to make good decisions within a project.

Context is not synonymous with documentation.

Documentation explains things.

Context exists specifically to influence future decisions.

## Four primary categories

### Intent

Why the project exists and what it is trying to achieve.

Examples:

* vision
* goals
* product strategy
* principles
* desired outcomes

### Knowledge

What the project has learned or established.

Examples:

* domain knowledge
* conceptual models
* terminology
* design conventions
* technical architecture
* evidence

### State

What is true about the project right now.

Examples:

* current feature
* current milestone
* work in progress
* known issues
* recent changes

### Constraints

What the agent must respect.

Examples:

* product principles
* architectural boundaries
* technical limitations
* accessibility requirements
* design-system rules
* security requirements

## Context should also distinguish decisions from questions

A useful project memory system needs both.

### Decision

Something that has been deliberately selected.

### Open question

Something that remains unresolved.

Do not convert an open question into a decision merely to make the documentation look complete.

## Suggested structure

```text
context/
├── PROJECT.md
├── PRINCIPLES.md
├── CURRENT-STATE.md
├── DECISIONS.md
├── OPEN-QUESTIONS.md
├── ROADMAP.md
│
├── design/
│   ├── product-model.md
│   ├── interaction-model.md
│   ├── design-principles.md
│   └── terminology.md
│
├── features/
│   ├── feature-name.md
│   └── ...
│
├── technical/
│   ├── architecture.md
│   ├── conventions.md
│   └── tooling.md
│
└── research/
    ├── observations.md
    └── references.md
```

The exact structure is flexible.

The principles are more important than the filenames.

## Context quality

Good context is:

* current
* specific
* concise
* decision-oriented
* internally consistent
* useful to a future session

Bad context is:

* duplicated
* vague
* stale
* excessively verbose
* contradictory
* generated simply because a workflow step requested a file

## Context hierarchy

When information conflicts, prefer:

1. explicit current project intent
2. explicit current decisions
3. current implementation evidence
4. current feature specifications
5. older documentation
6. assumptions

If the conflict cannot be resolved, surface it rather than choosing silently.

## Context and code

Code is the source of truth for what the system currently implements.

Context is the source of truth for documented intent, rationale and constraints.

When the two disagree, that disagreement is itself useful information.

The agent should determine whether:

* code is outdated
* context is outdated
* implementation is wrong
* the decision has changed

Do not silently rewrite one to match the other without understanding why they differ.
