# Git and Change Management

Product Kernel treats version control as part of project memory.

## Why Git matters here

When context and implementation live in the same repository, Git preserves not only code history but also the evolution of product thinking.

A useful commit history should make it possible to understand:

- what changed
- why it changed
- which feature it belonged to
- whether a decision was introduced, revised or removed

## Keep changes coherent

Avoid mixing unrelated work into the same change.

A change that:

- alters a product concept
- redesigns a component
- changes a sound system
- refactors unrelated code

should generally be separated unless those changes are materially dependent.

## Feature branches

Use branches for meaningful feature or change work.

A branch should represent a coherent unit of work that can be reviewed independently.

## Pull requests

A pull request should make it easy to understand:

- what changed
- why
- relevant product decisions
- known tradeoffs
- how it was tested

## Context changes belong with the work they describe

When a feature changes project assumptions or decisions, update the relevant context as part of the same work.

Do not knowingly merge implementation that contradicts the repository's documented state.

## Commit messages

Prefer concise, meaningful messages that describe the change.

Examples:

```text
feat: add reusable card templates
fix: preserve template state during duplication
docs: clarify template lifecycle
refactor: extract template state management
```

## Review principle

Git history should help answer:

> Why does this exist this way?

It should not merely answer:

> Which files changed?