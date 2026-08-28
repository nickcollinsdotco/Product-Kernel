# Tooling

Product Kernel is intentionally tool-agnostic at the conceptual level.

The methodology should work with different AI coding agents, development environments and project stacks.

## Current reference environment

The initial implementation is primarily designed around:

* Git
* GitHub
* Claude Code
* Markdown
* browser-based product validation

These are implementation choices for the current system, not requirements of the underlying methodology.

## Claude Code integration

Claude Code is useful because it can:

* inspect project files
* maintain persistent instructions
* execute commands
* edit code
* run tests
* use project-local skills
* work across multiple sessions

Product Kernel should expose its methodology through Claude-specific skills and commands where useful.

## Skills

Skills should contain reusable reasoning or execution behaviour.

A skill should answer:

> How should the agent perform this kind of work?

Skills should not become giant project knowledge dumps.

Project-specific knowledge belongs in `context/`.

## Commands

Commands are user-facing entry points into common workflows.

Examples may include:

```text
/pk-status
/pk-orient
/pk-reason
/pk-build
/pk-review
/pk-validate
/pk-sync
```

Commands should remain few and meaningful.

## Context

Context contains project knowledge.

It is not a replacement for source code.

## Future tooling

Possible future tooling includes:

* context linting
* contradiction detection
* automated context synchronisation
* project health checks
* context visualisation
* installation/bootstrap tooling
* support for additional coding agents

These should only be added when real use demonstrates their value.
