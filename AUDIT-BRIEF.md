# Product Kernel: Architecture Audit & Redesign

You are auditing the current Product Kernel repository before it becomes a stable public methodology.

The repository already contains an initial set of documents, context files, templates, and Claude instructions.

**Treat everything currently committed as Draft v0.1. Nothing is canonical merely because it already exists.**

Your job is to rigorously audit the current system, challenge its assumptions, compare it against the ideas that inspired it, and then redesign it into a stronger, simpler and more coherent system.

Do not optimise for preserving existing work.

Optimise for the quality of the resulting framework.

## Important instruction

The current repository has already been committed to Git.

That does NOT mean the current architecture is approved.

You have permission to:

* rewrite documents completely
* merge documents
* split documents
* rename files
* move files
* delete files
* introduce new files
* change the folder structure
* change terminology
* change the workflow
* change the decision model
* change the autonomy model
* change the skill architecture
* challenge the core thesis
* conclude that some current ideas should be abandoned

Do not make changes merely for the sake of being different.

Preserve something only when you can justify why it belongs.

The current repository should be treated as a prototype of the methodology itself.

## Source material

The current project has been inspired primarily by:

### Layers

Jamie Mill

https://layers.jamiemill.com/

Layers provides the main conceptual influence for product-design reasoning and diagnosis.

Important ideas to evaluate include:

* layered product reasoning
* orientation before intervention
* identifying the level at which a problem actually exists
* conceptual model as a load-bearing design concern
* targeted reasoning rather than mechanically traversing every layer
* distinction between observation, interpretation, decision and implementation

### Archē

Josh Millgate

https://github.com/joshmillgate/arche

Archē provides the main influence for persistent project context and disciplined AI-assisted development.

Important ideas to evaluate include:

* persistent project context
* context directories
* project state
* feature context
* technical/developer context
* structured development workflow
* context synchronisation
* AI-oriented commands and agents

Do not assume either project should be reproduced.

Determine what should actually be borrowed, what should remain external, and what Product Kernel uniquely contributes.

## Current Product Kernel thesis

The current thesis is:

> An autonomous agent needs more than instructions. It needs a persistent model of the product it is operating within.

The project currently describes itself as:

> A meta-context vibecoding framework for autonomous design + development.

The current conceptual loop is:

```text id="9mtm7e"
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
      ↓
next iteration
```

Challenge this model.

It may be correct.

It may be incomplete.

It may need a fundamentally different abstraction.

## Current repository

Start by inspecting the entire repository.

Read all existing:

* README files
* context files
* docs
* templates
* Claude skills
* agent instructions
* configuration
* examples
* package metadata
* Git history where useful

Do not assume the current folder structure is optimal.

First understand what currently exists.

Then audit it.

---

# 1. Executive verdict

Give a blunt assessment of the current project.

Answer:

* Is there actually a strong idea here?
* Is Product Kernel meaningfully distinct?
* What is the strongest part?
* What is currently confused?
* What is unnecessarily elaborate?
* What is missing?
* Would you personally keep developing this?
* What would need to change for it to become genuinely useful rather than another collection of AI prompts and Markdown files?

Do not optimise for encouragement.

---

# 2. Identify the real problem

Challenge the project's current framing.

Determine whether the real problem is primarily:

* lack of persistent context
* poor product reasoning
* context loss across sessions
* accidental product decisions during implementation
* lack of agent memory
* weak design-to-code handoff
* poor validation
* insufficient project state
* something else

Do not assume the current thesis is the deepest formulation.

Find the strongest underlying problem.

---

# 3. Challenge the name and positioning

Audit:

* Product Kernel
* meta-context
* vibecoding
* autonomous
* design + development
* framework
* operating system
* methodology
* protocol
* system

Determine what this project actually is.

Possible categories:

* methodology
* framework
* skill system
* project convention
* agent runtime layer
* context architecture
* product-development operating model
* developer tool
* something else

Recommend the strongest positioning at the project's current maturity.

Do not optimise for hypothetical future scale.

---

# 4. Audit the current repository architecture

Inspect the existing repository and produce a table like:

| Existing item | Keep | Rewrite | Merge | Split | Rename | Delete | Reason |
| ------------- | ---- | ------- | ----- | ----- | ------ | ------ | ------ |

Evaluate whether each current artifact has a clear purpose.

Look for:

* duplicated information
* competing sources of truth
* unnecessary documents
* unclear naming
* context versus documentation confusion
* framework versus project confusion
* agent instructions mixed with product knowledge
* templates that encode the wrong abstraction
* README material that belongs elsewhere
* information that agents need but currently cannot easily retrieve

---

# 5. Design the correct repository architecture

Do not merely improve the current folder tree.

Design the architecture from first principles.

Explicitly distinguish between:

### Framework knowledge

What Product Kernel itself believes and teaches.

### Project knowledge

What a particular project using Product Kernel knows.

### Agent behaviour

How the agent should operate.

### Human-facing documentation

What a person needs to understand the system.

### Templates

Reusable structures for creating new project knowledge.

### Examples

Demonstrations of the methodology in practice.

Determine whether these should live together or separately.

---

# 6. Re-evaluate docs/ versus context/

This distinction is currently assumed to be important.

Challenge it.

Ask:

* Does this distinction genuinely help agents?
* Does it primarily help humans?
* Is it too much taxonomy?
* Should the framework itself use a different structure?
* Should some files move?
* Should context be flatter?
* Should context be more structured?
* Should there be a single canonical context index?

Design the smallest architecture that preserves the useful distinction.

---

# 7. Re-evaluate "context"

The current model distinguishes:

* intent
* knowledge
* state
* constraints
* decisions
* open questions

Challenge this aggressively.

Determine whether context should instead distinguish concepts such as:

* intent
* evidence
* assumptions
* decisions
* invariants
* state
* constraints
* relationships
* history
* uncertainty

Determine whether some of these are:

* document types
* metadata
* properties
* views
* different states of the same object

Consider whether context is fundamentally:

* a document set
* a knowledge graph
* a structured record system
* a hierarchy
* a hybrid

Do not over-engineer.

The desired result is the minimum abstraction that meaningfully improves agent behaviour.

---

# 8. Re-evaluate the decision model

The current model is:

```text id="g2pk3z"
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

Do not accept this automatically.

Determine whether the model should instead represent:

* decision
* evidence
* confidence
* status
* scope
* owner
* dependencies
* supersession
* validity
* revisit conditions

Challenge the distinction between a "decision" and an "assumption".

Determine whether validation belongs to the decision itself or to evidence supporting the decision.

Determine how an agent should handle:

* conflicting decisions
* superseded decisions
* stale decisions
* conditional decisions
* decisions with weak evidence
* decisions that are intentionally provisional

Propose a better model if one exists.

---

# 9. Re-evaluate open questions

The project currently treats open questions as first-class context.

Determine whether this is genuinely useful.

Challenge:

* when something should become an open question
* whether open questions should have priority
* whether they should have owners
* whether they should expire
* when they should be promoted into active reasoning
* whether unresolved questions can block autonomous implementation

Define a useful distinction between:

* harmless uncertainty
* important uncertainty
* blocking uncertainty

---

# 10. Re-evaluate autonomy

The project currently proposes that agents should act autonomously within explicit boundaries.

Turn that into something operational.

Determine whether autonomy should depend on variables such as:

* uncertainty
* impact
* reversibility
* confidence
* scope
* precedent
* evidence
* cost of being wrong

Test whether a simple model can determine:

> Proceed autonomously.

versus:

> Surface this decision.

versus:

> Invoke deeper reasoning.

Do not leave autonomy as aspirational language.

It should be something an agent could actually apply.

---

# 11. Re-evaluate Layers integration

Determine exactly how Product Kernel should interact with Layers.

Possible models include:

### Model A

Product Kernel directly incorporates Layers as its reasoning system.

### Model B

Product Kernel treats Layers as an optional external methodology.

### Model C

Product Kernel creates a generalized reasoning layer inspired by Layers.

### Model D

Product Kernel delegates product reasoning entirely to Layers.

### Model E

Something else.

Evaluate these.

Determine the cleanest boundary.

Do not reproduce Layers unnecessarily.

Do not create a weaker version of something that should remain delegated.

---

# 12. Re-evaluate Archē integration

Do the same for Archē.

Determine whether Product Kernel should:

* extend Archē
* complement Archē
* replace parts of Archē
* stay orthogonal to Archē
* integrate conceptually while remaining implementation-independent

Identify exactly what Product Kernel adds.

The strongest architecture may be:

```text id="33hp4m"
Layers
   ↓
reasoning
   ↓
Product Kernel
   ↓
context + decisions + autonomy boundary
   ↓
Archē / other execution workflow
   ↓
implementation
```

But do not assume this is correct.

Test it.

---

# 13. Identify the true core primitive

Determine what the central primitive of Product Kernel actually is.

Candidates include:

* context
* decision
* intent
* product model
* project state
* evidence
* task
* specification
* agent session
* something else

A strong framework usually has a small number of important primitives.

Identify the minimum set.

---

# 14. Challenge the workflow

The current conceptual workflow is:

```text id="dq4c1c"
orient
→ identify uncertainty
→ reason
→ decide
→ capture
→ specify
→ build
→ review
→ validate
→ update context
```

Test whether this is actually the correct loop.

Look for:

* redundant steps
* missing steps
* places where reasoning should happen asynchronously
* situations where specification is unnecessary
* situations where validation should happen earlier
* circumstances where implementation should feed reasoning
* circumstances where evidence should update a prior decision

Determine whether the workflow should be:

* linear
* recursive
* state-driven
* event-driven
* hybrid

---

# 15. Challenge the "don't jump straight to UI" principle

This is currently one of the strongest philosophical claims.

Test it.

Determine:

* when this principle is useful
* when it becomes counterproductive
* whether rapid prototyping can legitimately happen before conceptual clarity
* whether surface work can be used as a discovery mechanism
* whether the system should explicitly support probing through prototypes

Do not turn "reason before building" into dogma.

A strong system should support iterative discovery as well as deliberate reasoning.

---

# 16. Challenge validation

The current proposal distinguishes:

* model validation
* flow validation
* surface validation
* implementation validation
* real-world validation

Determine whether this is useful or over-modelled.

Consider whether validation should instead be represented as:

* evidence attached to decisions
* evidence attached to features
* tests
* observations
* experiments
* user feedback

Determine how validation changes context.

---

# 17. Challenge human involvement

Define the human's role precisely.

The framework should not produce fake approval gates.

Determine:

* what the human uniquely contributes
* where human judgement is actually necessary
* where the agent should simply proceed
* what requires explicit approval
* what requires only notification
* what can be completely autonomous

Consider whether the human is:

* decision maker
* evidence provider
* exception handler
* product owner
* reviewer
* supervisor

Do not assume the answer is "all of the above."

---

# 18. Challenge the skill architecture

Audit whether one main skill is better than many.

Consider:

```text id="jkdthc"
one general Product Kernel skill

versus

Product Kernel
├── orient
├── reason
├── decide
├── build
├── review
├── validate
└── sync
```

Determine where the boundaries should actually be.

Remember:

Skills should encode behaviour.

Context should encode project knowledge.

Templates should encode reusable structures.

Commands should provide useful human entry points.

Do not blur these concerns.

---

# 19. Challenge AGENTS.md and SKILL.md

Determine whether both are actually necessary.

Ask:

* Does one duplicate the other?
* What belongs in AGENTS.md?
* What belongs in SKILL.md?
* What should Claude discover dynamically?
* What should be globally available?
* What should only apply when the skill is invoked?

Propose the smallest useful arrangement.

---

# 20. Challenge documentation density

Assume a capable engineer opens the repository for the first time.

They should understand:

* what the project is
* why it exists
* how it works
* where the important context lives
* how to use it
* how to contribute

within a few minutes.

Identify any current documentation that creates more cognitive load than value.

Prefer:

* fewer stronger documents
* indexes
* clear references
* explicit boundaries

over a large taxonomy of Markdown files.

---

# 21. Stress test with scenarios

Run the current architecture against at least these cases.

## A — UI complaint

User:

> Make this settings screen simpler.

Determine how the system should respond.

## B — Ambiguous feature

User:

> Add saved templates.

Nobody has defined what a template is.

## C — Contradictory context

Two documents describe different product behaviour.

## D — Code/context conflict

The implementation contradicts a documented decision.

## E — Old decision

A decision made six months ago now appears wrong.

## F — Implementation choice with product implications

Claude can implement a feature three ways, each with different UX consequences.

## G — Scope explosion

A small feature turns into a new subsystem.

## H — User absence

The user leaves the project for two weeks.

## I — Multiple agents

A second AI coding agent joins the project.

## J — Layers unavailable

The agent has Product Kernel but no access to Layers.

## K — Rapid prototyping

The product is highly visual and the fastest way to discover the problem is to build a rough prototype first.

## L — Routine implementation

A clearly specified feature needs a large amount of straightforward coding.

For each case, determine whether the current architecture works.

---

# 22. Look for missing primitives

After reviewing everything, explicitly identify missing concepts.

Consider:

* assumptions
* evidence
* confidence
* provenance
* contradictions
* supersession
* temporal validity
* scope
* invariants
* dependencies
* experiments
* observations
* hypotheses
* reversible versus irreversible decisions
* change impact
* context retrieval
* context compression
* memory decay
* context health
* context conflict detection

Do not add concepts simply because they sound sophisticated.

Only recommend a concept if it solves a concrete problem.

---

# 23. Design v0.1 again from first principles

After the audit, ignore the current repository structure.

Design what you believe Product Kernel v0.1 should actually be.

Provide:

### Core thesis

One concise statement.

### Core primitives

The smallest meaningful set.

### Mental model

The strongest conceptual diagram.

### Context architecture

The minimum useful structure.

### Decision model

The strongest practical model.

### Autonomy model

A usable escalation rule.

### Workflow

The actual operating loop.

### Layers relationship

The cleanest integration boundary.

### Archē relationship

The cleanest integration boundary.

### Human role

The actual human/agent boundary.

### Skill architecture

The minimum useful skills.

### Command architecture

Only commands that earn their existence.

### Repository structure

A complete revised tree.

---

# 24. Separate v0.1 from future ambition

Explicitly divide your recommendation into:

## MUST HAVE

Required to test the methodology.

## SHOULD HAVE

Useful but not essential.

## FUTURE

Interesting ideas that should not yet be built.

Do not let speculative infrastructure dominate v0.1.

---

# 25. Produce an explicit migration plan

Because the current repository is already committed, tell me exactly what to do with it.

Provide:

### Keep

Existing files that remain substantially correct.

### Rewrite

Files that should be replaced.

### Merge

Files that should become one document.

### Split

Files that contain multiple concepts.

### Rename

Files whose names are misleading.

### Delete

Files that should disappear.

### Add

New files that are genuinely necessary.

For every change, explain why.

---

# 26. Rewrite the important files

Do not stop at critique.

For every file that materially changes, provide the complete replacement Markdown.

Use this format:

```text
FILE: path/to/file.md

[complete file contents]
```

Do not provide fragments.

Do not merely describe what should change.

For the most important files, produce production-quality Markdown that can be pasted directly into the repository.

---

# 27. Design the ideal first-use experience

Imagine somebody clones this repository and wants to use Product Kernel on an unrelated product.

Describe the exact experience.

For example:

```text id="92w9ty"
clone
↓
install / copy
↓
initialise project context
↓
agent reads context
↓
user gives first task
↓
agent determines whether reasoning is necessary
↓
agent works
↓
context evolves
```

Determine what must happen automatically versus manually.

---

# 28. Define the minimum useful Product Kernel

At the end of the audit, answer:

> What is the smallest thing we could build that would prove this idea works?

This should be much smaller than the full framework if possible.

The proof should ideally involve one real project and several realistic product-development scenarios.

---

# 29. Measure usefulness

Do not invent vanity metrics.

Propose practical qualitative or behavioural tests.

Examples may include:

* Can a fresh session recover project state quickly?
* Does the agent make fewer accidental product decisions?
* Does it detect deeper product problems?
* Does it preserve important decisions?
* Does context remain coherent as the project changes?
* Does the workflow feel lighter rather than heavier?
* Can another person understand the project without being present for the original conversations?

Determine the smallest useful evaluation set.

---

# 30. Final recommendation

Finish with:

## The strongest version of Product Kernel

A concise description of what you now believe the project actually is.

## What I would build next

A deliberately small implementation sequence.

## What I would NOT build yet

Explicitly protect against premature complexity.

## The one idea worth defending

Identify the single insight that makes this project worth existing.

## The one idea worth killing

Identify the weakest or most misleading current assumption.

---

# Review style

Be adversarial but constructive.

Do not praise ideas merely because they are elegant.

Do not preserve existing architecture because effort has already been invested.

Do not invent complexity.

Do not assume every concept needs a file.

Do not assume every workflow needs a command.

Do not assume more autonomy is always better.

Do not assume more documentation is always better.

Prefer:

* clear boundaries
* small numbers of strong primitives
* explicit uncertainty
* durable knowledge
* useful retrieval
* evidence
* reversibility
* meaningful autonomy
* real validation
* low ceremony

The objective is to transform the current committed repository from a promising first draft into a coherent, testable v0.1 system.

The repository already exists.

**Audit it first. Challenge it second. Redesign it third. Only then rewrite the files.**

Do not treat the existing structure as the answer merely because it is already committed.
