# Worker Boundaries

## Purpose

Worker Boundaries define what Worker Profiles may and may not do within a knowledge manufacturing implementation.

Boundaries protect source grounding, provenance, traceability, quality, safety, and human accountability.

## Principle

A Worker Profile SHALL have explicit boundaries before it performs repeatable or automated work.

A Worker Profile SHALL NOT assume authority from capability alone.

For example, a worker may be capable of writing, but that does not authorise it to publish. A worker may be capable of validating, but that does not authorise it to waive failed gates.

## Boundary Categories

A conforming implementation SHOULD define boundaries for:

| Boundary Category | Purpose |
|---|---|
| Source Boundary | Which Knowledge Sources may be accessed. |
| Evidence Boundary | What may count as Evidence. |
| Object Boundary | Which Knowledge Objects may be created, edited, or retired. |
| Relationship Boundary | Which Relationships may be created or modified. |
| Recipe Boundary | Which Recipes may be selected or changed. |
| Validation Boundary | Which Quality Gates may be applied or waived. |
| Publication Boundary | Which Packages may be published and where. |
| Tool Boundary | Which tools, systems, or repositories may be used. |
| Memory Boundary | Which memory may be read or updated. |
| Decision Boundary | Which decisions require human review or escalation. |

## Universal Prohibitions

Unless explicitly authorised, a Worker Profile SHALL NOT:

- invent unsupported source-grounded claims;
- treat memory as Evidence without traceability;
- remove provenance;
- bypass required Quality Gates;
- waive failed gates;
- publish Packages;
- modify source systems;
- alter Production Recipes;
- redefine policies;
- hide uncertainty;
- suppress conflicting Evidence; or
- exceed permitted source, tool, or memory access.

## Boundary Declaration

A Worker Profile SHOULD declare boundaries in the following form:

```text
Worker Boundary
├── permitted sources
├── permitted inputs
├── permitted outputs
├── permitted tools
├── permitted memory
├── permitted decisions
├── prohibited actions
├── escalation triggers
└── review requirements
```

## Escalation Triggers

A Worker Profile SHALL escalate when it encounters:

- ambiguous source evidence;
- conflicting Knowledge Objects;
- missing required inputs;
- failed Quality Gates;
- unsupported product behaviour;
- access outside permitted scope;
- Recipe conflict;
- terminology conflict;
- publication risk;
- compliance risk; or
- user-facing uncertainty that materially affects understanding.

## Boundary Crossing

Boundary crossing MAY occur only through explicit authorisation.

An implementation SHOULD record:

- boundary crossed;
- reason;
- authority;
- duration;
- affected objects or products;
- review requirement; and
- expiry condition.

## Separation of Duties

Where risk is material, a conforming implementation SHOULD separate:

- extraction from assembly;
- assembly from validation;
- validation from waiver approval;
- packaging from publishing;
- source modification from publication; and
- maintenance analysis from automatic regeneration and release.

## AI Worker Boundaries

If a Worker Profile is implemented as an AI agent, the implementation SHOULD define:

- accessible tools;
- accessible sources;
- memory scope;
- output schema;
- maximum action authority;
- review points;
- prohibited claims;
- hallucination handling;
- uncertainty marking; and
- stop conditions.

AI implementation boundaries SHALL NOT redefine the KMRM Worker Profile. They implement the profile in a specific runtime.

## Boundary Review

Boundary definitions SHOULD be reviewed when:

- a Worker Profile gains new tools;
- a new source system is connected;
- a new Knowledge Product type is introduced;
- a Quality Gate changes;
- a publication channel changes;
- a boundary violation occurs; or
- automation maturity increases.
