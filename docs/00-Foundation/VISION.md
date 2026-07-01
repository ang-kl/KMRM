# Vision

## Purpose

KMRM exists to provide a stable reference model for knowledge manufacturing: the disciplined transformation of raw knowledge into traceable, validated, and reusable knowledge products.

The long-term vision is that knowledge systems can manufacture manuals, training guides, policies, support articles, AI context packages, curricula, and other outputs from shared source-grounded knowledge without losing provenance or meaning.

## Desired Future State

A conforming implementation of KMRM SHOULD be able to:

1. ingest knowledge from multiple source systems;
2. convert source material into structured Knowledge Objects;
3. preserve evidence and provenance for each object;
4. link objects through explicit relationships;
5. assemble outputs through repeatable Production Recipes;
6. validate outputs through Quality Gates;
7. publish Knowledge Products in multiple formats; and
8. update affected products when source knowledge changes.

## Strategic Separation

KMRM SHALL remain separate from its implementations.

```text
Reference model
  KMRM

Implementation
  Document Factory or another conforming system

Adapters
  GIA adapter, NTUC adapter, church adapter, or other source adapters

Knowledge products
  manuals, guides, courses, support articles, AI context packages, and other outputs
```

## Non-Goals

KMRM SHALL NOT define:

- one product domain;
- one software application;
- one AI agent organisation;
- one user interface;
- one database technology;
- one documentation format;
- one vendor model; or
- one repository layout for all implementations.

## Reference Implementation Direction

Document Factory MAY become the first implementation of KMRM. GIA MAY become the first validation ground used to test whether KMRM can support real product knowledge, source evidence, manual generation, and training guide generation.

GIA SHALL NOT determine the universal model. It MAY expose weaknesses in the model that require revision.
