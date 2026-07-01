# Quality Gate

## Purpose

A Quality Gate is a validation checkpoint that determines whether a Knowledge Object, Relationship, Knowledge Product, Package, or Publication may progress to the next Manufacturing Stage.

Quality Gates make knowledge manufacturing auditable, reviewable, and safer to automate.

## Definition

A Quality Gate SHALL define:

- gate identifier;
- gate name;
- purpose;
- target item type;
- requirement being tested;
- required input evidence or metadata;
- pass criteria;
- fail criteria;
- Waiver rules;
- output result; and
- lifecycle effect.

## Gate Types

KMRM defines the following standard Quality Gate types.

| Gate Type | Purpose |
|---|---|
| Source Grounding Gate | Verifies that claims or objects can be traced to Evidence or Knowledge Sources. |
| Provenance Gate | Verifies that origin and transformation history are preserved. |
| Traceability Gate | Verifies that outputs can be traced to source objects, recipes, and manufacturing runs. |
| Completeness Gate | Verifies that required ingredients, sections, or objects are present. |
| Consistency Gate | Verifies that related knowledge does not conflict without explanation. |
| Relationship Gate | Verifies that required Relationships exist and are valid. |
| Terminology Gate | Verifies that controlled vocabulary is used consistently. |
| Recipe Conformance Gate | Verifies that output follows the selected Production Recipe. |
| Packaging Gate | Verifies that the Package meets format and channel requirements. |
| Publishing Readiness Gate | Verifies that Publication requirements are satisfied. |
| Human Review Gate | Records required human approval where applicable. |
| Waiver Gate | Verifies that any exception has been explicitly authorised and recorded. |

An implementation MAY define additional Quality Gate types.

## Gate Result

A Quality Gate SHALL produce one of the following results:

| Result | Meaning |
|---|---|
| Passed | Requirement satisfied. |
| Failed | Requirement not satisfied. |
| Waived | Requirement not satisfied but authorised to proceed under recorded exception. |
| Blocked | Gate cannot be evaluated because required input is missing or ambiguous. |
| Not Applicable | Gate does not apply to the target item. |
| Not Evaluated | Gate has not yet been run. |

A failed required Quality Gate SHALL NOT be treated as passed.

## Required Gate Record

A Quality Gate result SHOULD record:

- gate identifier;
- target item identifier;
- Manufacturing Run identifier, if applicable;
- evaluator or system;
- timestamp or version;
- result;
- evidence inspected;
- findings;
- failed checks;
- Waiver reference, if any; and
- recommended next action.

## Gate Severity

A Quality Gate MAY have severity.

| Severity | Meaning |
|---|---|
| Blocking | Failure prevents progression unless waived. |
| Major | Failure should prevent Publication unless resolved or waived. |
| Minor | Failure should be corrected but may not block progression. |
| Advisory | Finding is informational or improvement-oriented. |

A Production Recipe SHALL identify which Quality Gates are required and which severities block progression.

## Source Grounding Requirement

A Quality Gate that validates source grounding SHALL distinguish between:

- direct Evidence;
- inferred Evidence;
- supporting context;
- generated wording; and
- unsupported claim.

Unsupported claims SHOULD fail source-grounding validation unless clearly marked as unresolved, speculative, or implementation-generated content.

## Waiver Discipline

A Waiver SHALL be explicit.

A Waiver SHOULD record:

- failed gate;
- reason for Waiver;
- approving actor or system;
- risk statement;
- affected item;
- expiry condition or review date where applicable; and
- whether Publication is still permitted.

A Waiver SHALL NOT erase the failed gate result.

## Gate Placement

Quality Gates MAY occur:

- before Assembly;
- during Assembly;
- after Assembly;
- before Packaging;
- before Publishing;
- during Maintenance; or
- during revalidation after change.

A Manufacturing Pipeline SHOULD place Quality Gates as early as practical to prevent defective knowledge from moving downstream.

## Gate Composition

Quality Gates MAY be composed into gate sets.

A gate set MAY represent the validation requirements for a Production Recipe, Product type, Package format, or Publication channel.

## Human Review

A Human Review Gate MAY be required for outputs affecting users, training, compliance, safety, legal obligations, financial decisions, or organisational policy.

KMRM does not specify who the reviewer must be. That belongs to the implementation or governance profile.

## Quality Gate Principle

Quality Gates are not mere proofreading checks. They are manufacturing controls that protect source grounding, provenance, traceability, correctness, and publication readiness.
