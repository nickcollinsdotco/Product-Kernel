# Mental Model

Product Kernel is built around four connected capabilities:

```text
REASON
  ↓
REMEMBER
  ↓
EXECUTE
  ↓
VALIDATE
  ↓
REMEMBER
```

This is a loop, not a linear pipeline.

## 1. Reason

Determine what needs to be understood before implementation can proceed safely.

Product reasoning may involve:

* observed behaviour
* domain understanding
* user needs
* product strategy
* conceptual model
* interaction structure
* surface design

Layers is the primary influence here.

The system should identify the active uncertainty rather than mechanically walking through every layer.

## 2. Remember

Store useful project knowledge in durable, version-controlled context.

This includes:

* project intent
* product principles
* decisions
* open questions
* current state
* feature knowledge
* technical constraints
* design conventions

Archē is the primary influence here.

## 3. Execute

Once intent and constraints are sufficiently clear, convert decisions into implementation.

Execution includes:

* specification
* planning
* coding
* refactoring
* testing
* review

The agent should be able to operate with significant autonomy here.

## 4. Validate

Determine whether the implementation is actually correct.

Validation should consider:

* conceptual correctness
* interaction correctness
* surface quality
* implementation correctness
* real-world behaviour

Validation can produce new evidence.

New evidence can invalidate earlier assumptions.

That evidence should therefore feed back into context.

## The complete loop

```text
                 ┌─────────────┐
                 │   CURRENT   │
                 │    STATE    │
                 └──────┬──────┘
                        ↓
                  ORIENT / OBSERVE
                        ↓
                FIND UNCERTAINTY
                        ↓
                   REASON
                        ↓
                    DECIDE
                        ↓
                  CAPTURE
                        ↓
                    BUILD
                        ↓
                   REVIEW
                        ↓
                  VALIDATE
                        ↓
                UPDATE CONTEXT
                        │
                        └──────────────→ NEW STATE
```

## Layers and Archē within Product Kernel

```text
                     PRODUCT KERNEL

       ┌──────────────────┼──────────────────┐
       │                  │                  │
       ▼                  ▼                  ▼
    REASON              REMEMBER           EXECUTE
       │                  │                  │
     Layers             Context            Build
       │                  │                workflow
       │                  │                  │
       └───────────┬──────┴──────────┬───────┘
                   │                 │
                   ▼                 ▼
                DECISIONS      IMPLEMENTATION
                   │                 │
                   └────────┬────────┘
                            ▼
                         VALIDATE
                            │
                            ▼
                       NEW CONTEXT
```

## The key distinction

Layers answers:

> What should we understand or decide?

Archē answers:

> How do we preserve context and run disciplined development?

Product Kernel is interested in the connective tissue:

> How does a product decision become durable context, then implementation, then validated knowledge?

That connective tissue is the core of this project.
