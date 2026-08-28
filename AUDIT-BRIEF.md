# Product Kernel: Architecture Audit & Challenge

You are auditing the proposed Product Kernel framework before it becomes the canonical repository structure.

Do not assume that the existing documents are correct.

Treat them as a strong draft that should be challenged.

Your job is to find weaknesses, contradictions, unnecessary complexity, missing concepts, bad abstractions, and places where the framework could become genuinely better.

## Context

Product Kernel is currently conceived as:

> A meta-context vibecoding framework for autonomous design + development.

The core thesis is:

> An autonomous agent needs more than instructions. It needs a persistent model of the product it is operating within.

The framework combines ideas inspired by:

* Layers by Jamie Mill
* Archē by Josh Millgate

The intended conceptual relationship is:

```text
Layers
    ↓
product reasoning
    ↓
decisions
    ↓
persistent context
    ↓
autonomous implementation
    ↓
validation
    ↓
updated context
```

Layers is primarily influencing the reasoning side.

Archē is primarily influencing the persistent-context and disciplined development side.

Product Kernel is intended to be an independent synthesis rather than a fork or wrapper around either project.

## Current proposed structure

```text
product-kernel/
├── README.md
├── LICENSE
├── AGENTS.md
│
├── context/
│   ├── PROJECT.md
│   ├── PRINCIPLES.md
│   ├── CURRENT-STATE.md
│   ├── DECISIONS.md
│   ├── OPEN-QUESTIONS.md
│   └── ROADMAP.md
│
├── docs/
│   ├── 01-philosophy.md
│   ├── 02-mental-model.md
│   ├── 03-workflow.md
│   ├── 04-context-architecture.md
│   ├── 05-decision-system.md
│   ├── 06-autonomy-model.md
│   ├── 07-validation.md
│   ├── 08-git-and-change-management.md
│   ├── 09-tooling.md
│   └── 10-influences.md
│
├── templates/
│   ├── decision.md
│   └── feature.md
│
└── .claude/
    └── skills/
        └── product-kernel/
            └── SKILL.md
```

## Audit objectives

Audit the entire proposed system, not just individual files.

### 1. Challenge the thesis

Determine whether the central thesis is actually strong.

Ask:

* Is "persistent product context" genuinely the core problem?
* Is Product Kernel solving a distinct problem from existing agent frameworks?
* Is this really a framework, a methodology, a skill system, a project convention, or something else?
* Is "meta-context" the right conceptual abstraction?
* Is "vibecoding" useful positioning or does it weaken credibility?
* Does "autonomous design + development" accurately describe the system?
* Is there a stronger framing that emerges from the material?

Do not preserve terminology merely because it already exists.

### 2. Compare the abstraction boundaries

Determine whether the current division between:

* Layers
* Product Kernel
* Archē
* Claude Code
* project code
* project context

is actually coherent.

Identify overlaps.

Identify missing boundaries.

Ask whether Product Kernel currently has a sufficiently distinct role.

The desired result is not:

```text
Layers + Archē = Product Kernel
```

unless that is genuinely the best abstraction.

Look for a stronger synthesis.

### 3. Challenge the context architecture

Audit the distinction between:

* docs/
* context/
* templates/
* AGENTS.md
* SKILL.md
* future commands

Determine whether these are truly different concerns or merely different folders containing overlapping Markdown.

Look specifically for:

* duplication
* conflicting sources of truth
* unnecessary hierarchy
* confusing terminology
* missing context categories
* poor retrieval ergonomics for agents
* documents that should be merged
* documents that should be split

Ask:

> If you were Claude arriving in a new repository, what is the minimum information you would actually need, in what order, and from where?

Design the architecture around that question.

### 4. Challenge the concept of "context"

The current model divides context into:

* intent
* knowledge
* state
* constraints
* decisions
* questions

Challenge that model.

Determine whether:

* these categories overlap
* additional categories are required
* some should be properties rather than documents
* evidence should be first-class
* confidence should be first-class
* provenance should be first-class
* temporal validity should be represented
* contradictions should be represented
* dependencies between decisions should be represented

Consider whether context is better understood as a graph, hierarchy, set of records, documents, or hybrid.

Do not over-engineer this.

The goal is to identify the minimum useful abstraction.

### 5. Challenge the decision model

The proposed lifecycle is:

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

Audit this critically.

Ask:

* Are these actually states?
* Are they mutually exclusive?
* Can a decision be both assumed and validated?
* Should evidence have its own lifecycle?
* Can a decision become invalid?
* Should decisions have owners?
* Should decisions have scope?
* Should decisions have dependencies?
* How should superseded decisions work?
* How does an agent know whether an old decision still applies?

Propose a better model if necessary.

### 6. Challenge autonomy

The framework currently distinguishes between:

* safe autonomous implementation
* decisions that should be surfaced

Audit this deeply.

Determine whether autonomy should be modelled around:

* uncertainty
* reversibility
* impact
* confidence
* scope
* established precedent

Consider whether Product Kernel needs an explicit "decision threshold" or escalation model.

Avoid hand-wavy language.

Make the model operational enough that an AI agent could use it.

### 7. Challenge the Layers integration

Do not assume Layers is the correct reasoning model simply because it is useful.

Determine:

* which parts of Layers are essential
* which parts are unnecessary for Product Kernel
* whether the seven layers map cleanly into an agent workflow
* whether Product Kernel should expose those layers directly
* whether the system should instead use them internally
* whether "orient" is sufficiently powerful
* whether there are missing reasoning stages before implementation

Pay particular attention to the distinction between:

* observation
* interpretation
* decision
* specification

Do not allow these concepts to blur together.

### 8. Challenge the Archē integration

Audit whether the framework is actually benefiting from Archē or simply reproducing it.

Determine:

* which Archē ideas should be preserved
* which should be omitted
* which should be reframed
* what Product Kernel uniquely adds
* whether the build workflow belongs inside Product Kernel at all

If Archē should remain a complementary execution layer, state exactly where the boundary should be.

### 9. Challenge the human role

The framework currently emphasises increasing agent autonomy.

Audit the human role carefully.

Determine:

* where human judgement remains essential
* where the human should approve
* where the human should provide evidence
* where the human is merely supervising
* where the human should be removed from the loop entirely

The system should not create performative human approval.

It should identify genuinely consequential decisions.

### 10. Challenge validation

The current model distinguishes:

* model validation
* flow validation
* surface validation
* implementation validation
* real-world validation

Audit this.

Determine whether:

* these are genuinely distinct
* evidence should be attached to decisions directly
* validation should modify decision state
* validation should modify context automatically
* product truth should be treated as provisional

Propose a stronger evidence model if appropriate.

### 11. Challenge the documentation strategy

Review every proposed file conceptually.

Determine:

* which documents are essential
* which are useful but optional
* which should not exist
* which information is duplicated
* which concepts are currently under-specified

Aim for a repository that is understandable in under five minutes by a competent engineer or designer.

Avoid documentation bloat.

### 12. Challenge naming

Audit:

* Product Kernel
* meta-context
* vibecoding
* autonomous design + development
* context
* decision
* state
* intent
* knowledge
* constraints
* workflow
* skill
* command

Identify terms that are:

* overloaded
* ambiguous
* fashionable but imprecise
* too generic
* unnecessarily academic

Propose better alternatives where useful.

### 13. Challenge the README

The README should communicate the idea extremely quickly.

Audit whether the current framing communicates:

* the problem
* the insight
* the system
* why it is different
* how it relates to Layers and Archē
* how someone would actually use it

Do not optimise only for clarity.

Optimise for a strong technical/product concept.

### 14. Challenge the skill architecture

The current proposal has one initial Product Kernel skill.

Determine whether that is correct.

Explore the boundary between:

* one general skill
* multiple specialised skills
* commands
* templates
* project context
* agent instructions

Avoid creating commands or skills simply because frameworks conventionally have them.

The system should earn each abstraction.

### 15. Challenge the public-project strategy

Assume this will be built publicly.

Evaluate whether the repository should optimise for:

* personal workflow
* open-source framework
* research project
* methodology
* agent skill library
* developer tool
* product-design system
* future package/tool

Determine which positioning is most defensible at the current stage.

Do not optimise for hypothetical scale.

### 16. Look for missing concepts

After auditing the existing model, identify ideas that are currently absent.

Potential areas include:

* evidence
* provenance
* confidence
* assumptions
* contradictions
* supersession
* dependencies
* scope
* temporal validity
* product invariants
* system invariants
* project ontology
* memory decay
* context retrieval
* context compression
* change detection
* decision impact
* reversibility

Only introduce a concept if it solves a real problem.

### 17. Attack the framework with failure scenarios

Test the proposed system mentally against concrete situations.

At minimum:

#### Scenario A

A designer says:

> "Make this settings screen simpler."

#### Scenario B

A developer says:

> "Add saved templates."

but nobody has decided what a template actually is.

#### Scenario C

Claude discovers that the code contradicts the documented product decision.

#### Scenario D

A design decision from six months ago is now obviously wrong.

#### Scenario E

Two context documents disagree.

#### Scenario F

Claude can implement a feature in three different technically valid ways with different product consequences.

#### Scenario G

A feature starts simple and expands into a new subsystem.

#### Scenario H

The user disappears for two weeks and returns to the repository.

#### Scenario I

A second AI agent joins the project.

#### Scenario J

A future agent has no access to Layers but still needs to operate correctly.

For each scenario, identify where the current architecture succeeds or fails.

### 18. Produce a better architecture

After the critique, produce a proposed v0.1 architecture.

Do not merely comment on the existing files.

Design a better system.

Include:

* revised repository structure
* revised context architecture
* revised document taxonomy
* revised decision model
* revised autonomy model
* revised validation model
* revised skill architecture
* revised agent entry point
* revised workflow

Prefer fewer concepts that are stronger.

### 19. Separate "must have now" from "future"

Divide the output into:

#### MUST HAVE

Necessary to test the methodology.

#### SHOULD HAVE

Useful but not required for first validation.

#### FUTURE

Potential extensions that should not be built yet.

This is important.

Do not let speculative architecture dominate the first version.

### 20. Rewrite, don't merely criticise

Where a document or concept is weak, produce the improved version.

For important changes, provide complete replacement Markdown rather than vague recommendations.

## Desired output

Produce a structured audit with these sections:

# Executive verdict

A blunt assessment of the current idea.

# What is genuinely strong

Identify the ideas worth preserving.

# What is weak

Identify bad abstractions, unnecessary complexity and contradictions.

# What is missing

Identify genuinely important omissions.

# Relationship to Layers

Explain the correct boundary.

# Relationship to Archē

Explain the correct boundary.

# Recommended architecture

Provide the revised system.

# Recommended repository structure

Provide the revised tree.

# Core mental model

Provide the strongest conceptual diagram.

# Context model

Provide the revised context taxonomy.

# Decision model

Provide the revised decision/evidence model.

# Autonomy model

Provide the revised escalation model.

# Workflow

Provide the revised end-to-end workflow.

# Skills and commands

Specify the minimum useful set.

# Documents

Identify which current documents should:

* remain
* change
* merge
* split
* disappear
* be added

# v0.1 scope

Define exactly what should exist before the system is tested on a real project.

# Future directions

Capture interesting ideas that should deliberately wait.

# Replacement files

For every document you believe should materially change, provide its complete replacement Markdown.

## Important review behaviour

Be intellectually adversarial.

Do not praise ideas simply because they are elegant.

Do not preserve abstractions because they already exist.

Do not invent complexity because it sounds sophisticated.

Prefer:

* clear boundaries
* fewer concepts
* explicit state
* durable knowledge
* strong retrieval
* reversible decisions
* meaningful autonomy
* real evidence

The purpose of this audit is to make Product Kernel substantially better before it becomes difficult to change.

The final recommendation should leave the project with a coherent v0.1 architecture that is small enough to test and strong enough to be worth testing.
