# Validation

Validation determines whether decisions and implementation hold up against evidence.

## Validation is layered

### 1. Model validation

Does the conceptual model make sense?

Questions:

- Are the objects correct?
- Are relationships understandable?
- Are states coherent?
- Is terminology consistent?
- Does the lifecycle make sense?

### 2. Flow validation

Does the interaction make sense?

Questions:

- Can users predict what will happen?
- Are important states covered?
- Is the sequence coherent?
- Are errors and recovery understandable?

### 3. Surface validation

Does the interface communicate the intended model and interaction?

Questions:

- Is hierarchy clear?
- Are controls discoverable?
- Are states represented appropriately?
- Does the visual design reinforce the conceptual structure?

### 4. Implementation validation

Does the software actually behave as specified?

Possible methods:

- unit tests
- integration tests
- static analysis
- type checking
- automated browser tests

### 5. Real-world validation

Does the product work in reality?

Possible evidence:

- manual UAT
- actual browser use
- user observation
- analytics
- support feedback
- experiments

## Tests are not product validation

A system can pass every automated test and still contain:

- the wrong product model
- confusing terminology
- a poor interaction flow
- an unnecessary feature
- a misleading interface

Tests establish implementation facts.

They do not automatically establish product truth.

## Validation produces knowledge

Validation should feed back into context.

For example:

```text
Decision:
Users can edit templates independently.

Validation:
Observed behaviour shows users expect template changes to affect
future cards but not existing cards.

Result:
Decision remains valid with clarified semantics.
```

Or:

```text
Decision:
A modal is sufficient for template management.

Validation:
The feature now requires browsing, searching, sorting and bulk actions.

Result:
Surface and interaction decision should be reconsidered.
```

## Definition of done

A feature should not be considered complete merely because code exists.

A useful completion test is:

- intended behaviour is understood
- important decisions are documented
- implementation is complete
- automated checks pass
- actual product behaviour has been reviewed
- relevant context has been updated