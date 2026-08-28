# Product Kernel

## What is this?

Product Kernel is a meta-context framework for AI-native product design and development.

It combines:

* structured product reasoning
* persistent project context
* autonomous implementation
* review and validation

The aim is to give AI coding agents enough durable understanding to do more than execute isolated prompts. They should be able to understand the product they are operating within, preserve important decisions, and build within explicit constraints.

## Why does it exist?

AI coding agents are increasingly capable of producing sophisticated software.

The limiting factor is often no longer raw implementation capability.

The harder problem is maintaining coherent product understanding across time.

An agent may need to understand:

* what the product is trying to achieve
* who it is for
* what users are actually doing
* what important concepts and objects mean
* why previous decisions were made
* which constraints are deliberate
* what has already been tried
* what is currently being built
* what remains uncertain

Without persistent context, each session partially reconstructs the product from incomplete evidence.

Product Kernel treats this knowledge as project infrastructure.

## Core thesis

> An autonomous agent needs more than instructions. It needs a persistent model of the product it is operating within.

## Primary influences

Product Kernel is independently developed but heavily influenced by:

* Layers by Jamie Mill
* Archē by Josh Millgate

Layers provides much of the product reasoning model.

Archē provides much of the persistent-context and development-workflow inspiration.

Product Kernel combines these ideas into an independent system focused on AI-native product development.

## Current status

Experimental and evolving.

This repository is being developed as a public methodology and working system rather than as a finished framework.

## Current objective

Establish a lightweight, reusable system that allows an AI agent to:

1. understand an existing project
2. identify unresolved product decisions
3. reason at the appropriate level
4. preserve important decisions
5. execute implementation work within constraints
6. validate the resulting product
7. update project context so the next session starts from reality rather than from scratch

## Non-goal

Product Kernel is not intended to make every software task procedural.

Simple work should remain simple.

The framework exists to improve decisions where ambiguity, complexity or accumulated context make autonomous execution less reliable.
