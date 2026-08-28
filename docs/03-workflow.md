# Workflow

Product Kernel uses a flexible workflow rather than a mandatory sequence for every task.

## Step 1 — Receive the request

Start with the actual request and inspect existing project context.

Do not assume that the request accurately identifies the underlying problem.

## Step 2 — Determine the task type

Classify the work broadly as:

* straightforward implementation
* bug or correction
* product reasoning
* mixed product and implementation work

### Straightforward implementation

Proceed when the intent is already clear.

### Product reasoning

Use the relevant reasoning method before implementation.

### Mixed work

Separate the product decision from the implementation work.

## Step 3 — Check existing context

Before significant work, inspect relevant:

* project context
* principles
* current state
* decisions
* open questions
* feature context
* technical constraints

Do not ask the user to repeat information that already exists in the repository.

## Step 4 — Orient when necessary

If the problem is unclear, determine where the uncertainty lives.

Ask:

* Is this really a surface problem?
* Is the interaction model clear?
* Is the conceptual model clear?
* Is the product strategy clear?
* Are user needs understood?
* Is the domain clear?
* What evidence actually supports our assumptions?

## Step 5 — Reason

Use the lightest appropriate reasoning intervention.

Resolve the decisions necessary to move forward.

Do not solve unrelated uncertainties.

## Step 6 — Capture

When a meaningful decision is made, record:

* what was decided
* why
* consequences
* relevant evidence
* remaining uncertainty

Do not create documentation merely to satisfy a process.

## Step 7 — Specify

Translate sufficiently resolved product intent into an implementation-ready feature or task specification.

The specification should contain enough information for autonomous execution without recreating the entire reasoning conversation.

## Step 8 — Build

Implement against the established context.

The agent may make routine implementation decisions autonomously.

The agent should not silently make major product decisions.

## Step 9 — Review

Check the implementation against:

* original intent
* relevant decisions
* project principles
* technical constraints
* design conventions

## Step 10 — Validate

Use the appropriate combination of:

* automated tests
* static analysis
* component testing
* browser testing
* manual UAT
* evidence from actual usage

## Step 11 — Update context

Update:

* current state
* decisions
* feature context
* open questions
* implementation notes

Only update documents that genuinely changed.

## Step 12 — Repeat

The result of validation becomes part of the new project state.

The next iteration begins with a better-informed context.

## When to stop and reason again

Return to product reasoning if:

* implementation reveals contradictory assumptions
* a feature becomes unexpectedly complex
* the UI requires repeated patches
* terminology becomes inconsistent
* the data model starts fighting the intended behaviour
* the scope changes materially
* a previously implicit decision becomes consequential

Do not force an implementation through a problem that is actually a reasoning problem.
