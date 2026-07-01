# Concept Map

This document gives the initial KMRM v0.1 concept map. It is a non-executable reference diagram that shows how the major concepts relate.

## High-Level Flow

```text
Raw Knowledge
        ↓
Knowledge Source
        ↓
Evidence
        ↓
Knowledge Object
        ↓
Relationship
        ↓
Knowledge Graph or equivalent relationship structure
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

## Layered Model

```text
Layer 1: Source Layer
  Raw Knowledge
  Knowledge Source
  Evidence

Layer 2: Representation Layer
  Knowledge Object
  Metadata
  Provenance
  Lifecycle State

Layer 3: Relationship Layer
  Relationship
  Relationship Type
  Knowledge Graph or equivalent structure

Layer 4: Manufacturing Layer
  Production Recipe
  Production Cell
  Manufacturing Pipeline
  Quality Gate

Layer 5: Output Layer
  Knowledge Product
  Package
  Publication
```

## Concept Relationships

| Source Concept | Relationship | Target Concept |
|---|---|---|
| Knowledge Source | provides | Evidence |
| Evidence | supports | Knowledge Object |
| Knowledge Object | has | Metadata |
| Knowledge Object | retains | Provenance |
| Knowledge Object | participates in | Relationship |
| Relationship | connects | Knowledge Object |
| Knowledge Graph | represents | Knowledge Object and Relationship |
| Production Recipe | specifies required inputs from | Knowledge Object |
| Production Recipe | defines | Manufacturing Pipeline |
| Manufacturing Pipeline | contains | Production Cell |
| Manufacturing Pipeline | applies | Quality Gate |
| Quality Gate | validates | Knowledge Object or Knowledge Product |
| Production Recipe | manufactures | Knowledge Product |
| Knowledge Product | is released as | Publication |
| Publication | references | Recipe version and source baseline |

## Manufacturing View

```text
Knowledge Sources
        ↓ Extraction
Evidence
        ↓ Normalisation
Knowledge Objects
        ↓ Classification
Typed Knowledge Objects
        ↓ Relationship Building
Knowledge Graph or equivalent structure
        ↓ Assembly by Recipe
Draft Knowledge Product
        ↓ Quality Gates
Validated Knowledge Product
        ↓ Packaging
Packaged Knowledge Product
        ↓ Publishing
Publication
```

## Object-Centred View

KMRM is object-centred rather than document-centred.

```text
Knowledge Object
  ├── identity
  ├── type
  ├── metadata
  ├── provenance
  ├── evidence
  ├── lifecycle state
  └── relationships
```

Documents, manuals, guides, courses, policies, and AI context packages are Knowledge Products manufactured from Knowledge Objects. They are not the primary organising unit of the reference model.

## Implementation Note

A conforming implementation MAY store these concepts in files, tables, graph databases, document databases, indexes, or other structures.

KMRM requires preservation of semantics, provenance, traceability, and validation behaviour. It does not require a particular storage technology.
