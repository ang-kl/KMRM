# Worker Memory

## Purpose

Worker Memory defines how a conforming implementation may provide durable context to Worker Profiles without collapsing all knowledge into one unbounded context.

Worker Memory is an operating pattern. It does not prescribe one memory technology, vector store, database, file format, or AI framework.

## Principle

A Worker Profile SHOULD have access only to the memory required for its responsibilities.

Memory SHALL NOT replace Evidence, Provenance, or Traceability.

## Memory Types

A conforming implementation MAY define the following memory types.

| Memory Type | Purpose |
|---|---|
| Role Memory | Durable instructions and boundaries for a Worker Profile. |
| Skill Memory | Reusable knowledge about how a Skill is performed. |
| Product Memory | Validated knowledge about a Knowledge Product type or Product Profile. |
| Source Memory | Stable facts about a Knowledge Source or Source System. |
| Terminology Memory | Controlled vocabulary and naming rules. |
| Validation Memory | Quality Gate results, recurring defects, and waiver history. |
| Publication Memory | Release history, package manifests, and publication records. |
| Performance Memory | Metrics, review notes, rework patterns, and improvement actions. |

## Memory Boundaries

Worker Memory SHALL respect Worker Profile boundaries.

For example:

- an Evidence Extractor MAY access source-scoping and citation memory;
- a User Manual Assembler MAY access manual structure and style memory;
- a Training Guide Assembler MAY access learning design memory;
- a Quality Validator MAY access gate rules and defect history;
- a Publisher MAY access publication and packaging memory.

Access to memory SHALL NOT imply authority to perform actions outside the Worker Profile.

## Memory Versus Evidence

Memory MAY assist a Worker Profile, but Evidence remains the source-grounding mechanism.

A Worker Profile SHALL NOT treat memory as source evidence unless the memory itself contains traceable Evidence or references a validated Knowledge Object.

## Memory Freshness

An implementation SHOULD record freshness, version, or baseline information for memory used in Manufacturing Runs.

A Worker Profile SHOULD flag memory as stale when it conflicts with current Evidence or Source Baseline.

## Memory Update

Memory SHOULD be updated only through defined mechanisms.

An implementation SHOULD distinguish:

- validated memory;
- provisional memory;
- worker-local notes;
- implementation logs;
- performance feedback; and
- retired or superseded memory.

## Prohibited Memory Use

Worker Memory SHALL NOT be used to:

- bypass source grounding;
- invent product behaviour;
- override Quality Gates;
- hide uncertainty;
- publish without required checks;
- retain sensitive data beyond permitted scope; or
- erase conflicting Evidence.

## Minimal Memory for Document Factory-like Implementation

A Document Factory-like implementation SHOULD define at least:

1. role memory for each Permanent Worker;
2. terminology memory;
3. recipe memory;
4. validation memory;
5. publication memory; and
6. known ambiguity or defect memory.

## Human Review

Memory that materially changes manufacturing behaviour SHOULD be reviewable.

When memory affects output quality, validation, or publication, the implementation SHOULD maintain a change record.
