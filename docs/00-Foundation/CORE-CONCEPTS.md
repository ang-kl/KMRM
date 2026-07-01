# Core Concepts

KMRM is built on a small set of core concepts. These concepts are intended to remain stable across implementations, product domains, and output formats.

## Concept Stack

```text
Knowledge Source
        ↓
Evidence
        ↓
Knowledge Object
        ↓
Relationship
        ↓
Knowledge Graph or equivalent structure
        ↓
Production Recipe
        ↓
Manufacturing Pipeline
        ↓
Quality Gate
        ↓
Knowledge Product
        ↓
Publication
```

## 1. Knowledge Source

A Knowledge Source is any origin from which knowledge may be extracted.

A Knowledge Source MAY be:

- a repository;
- a file;
- a document;
- a database;
- an issue tracker;
- a commit;
- a message;
- a media asset;
- a meeting note;
- a transcript;
- an observation; or
- another source system.

A Knowledge Source SHALL be identifiable when it is used to support a Knowledge Object, Relationship, or Knowledge Product.

## 2. Evidence

Evidence is a specific source-grounded item that supports a Knowledge Object, Relationship, or claim.

Evidence SHOULD record:

- source identifier;
- location within the source;
- extraction timestamp or version;
- relevant excerpt, pointer, or reference;
- confidence or status where applicable; and
- whether the evidence is direct, inferred, or supporting context.

## 3. Knowledge Object

A Knowledge Object is the primary unit of structured knowledge.

A Knowledge Object SHALL have:

- an identifier;
- a type;
- a lifecycle state;
- provenance;
- metadata; and
- zero or more Relationships.

A Knowledge Object SHOULD have one or more Evidence records when it is used for manufacturing a Knowledge Product.

## 4. Relationship

A Relationship is an explicit typed link between model elements.

Relationships MAY connect:

- one Knowledge Object to another;
- a Knowledge Object to Evidence;
- a Knowledge Object to a Knowledge Product;
- a Knowledge Product to a Production Recipe;
- a Production Recipe to a Quality Gate; or
- other model elements defined by a conforming implementation.

Relationships SHALL be explicit when they affect manufacturing, validation, or publication.

## 5. Knowledge Graph

A Knowledge Graph is a representation of Knowledge Objects and Relationships.

KMRM does not require one graph database or graph technology. A conforming implementation MAY represent the graph through files, tables, graph stores, indexes, or another equivalent structure.

The required concept is relationship traceability, not a particular storage engine.

## 6. Production Recipe

A Production Recipe is a repeatable specification for manufacturing a Knowledge Product.

A Production Recipe SHOULD define:

- required input object types;
- optional input object types;
- assembly steps;
- required Quality Gates;
- output structure;
- packaging expectations; and
- publication requirements.

A Production Recipe SHALL NOT be replaced by an AI prompt. A prompt MAY execute part of a recipe in an implementation.

## 7. Manufacturing Pipeline

A Manufacturing Pipeline is the ordered process that transforms Knowledge Sources and Knowledge Objects into Knowledge Products.

A Manufacturing Pipeline MAY include:

- Extraction;
- Normalisation;
- Classification;
- Relationship Building;
- Assembly;
- Validation;
- Packaging; and
- Publishing.

A Manufacturing Pipeline SHALL preserve provenance across stages.

## 8. Quality Gate

A Quality Gate is a validation checkpoint.

A Quality Gate MAY test:

- source grounding;
- provenance completeness;
- relationship validity;
- terminology consistency;
- completeness;
- non-duplication;
- formatting;
- version compatibility;
- publication readiness; and
- human review status.

A Knowledge Product SHALL NOT be treated as publishable until required Quality Gates have passed or been explicitly waived.

## 9. Knowledge Product

A Knowledge Product is a manufactured output.

Examples include:

- user manual;
- training guide;
- curriculum;
- support guide;
- release notes;
- policy manual;
- API documentation;
- AI context package;
- media script; and
- compliance pack.

A Knowledge Product SHALL be traceable to its Production Recipe and source Knowledge Objects.

## 10. Publication

A Publication is a released or delivered instance of a Knowledge Product.

A Publication SHOULD record:

- product identifier;
- version;
- format;
- channel or location;
- publication timestamp;
- source baseline;
- recipe version;
- validation status; and
- responsible actor or system.

## Primitive Principle

KMRM SHOULD keep the universal core small. Domain-specific ideas such as Feature, Screen, API, Lesson, Policy, Sermon Note, or Support Article SHOULD be represented as specialisations of Knowledge Object or Knowledge Product, rather than as required core primitives.
