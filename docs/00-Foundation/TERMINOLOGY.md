# Terminology

This document defines controlled vocabulary for KMRM. Future KMRM documents SHOULD use these terms consistently.

## Normative Keywords

The following terms indicate requirement strength:

| Term | Meaning |
|---|---|
| SHALL | Mandatory requirement. |
| SHALL NOT | Mandatory prohibition. |
| SHOULD | Recommended requirement unless there is a justified reason to deviate. |
| SHOULD NOT | Recommended prohibition unless there is a justified reason to deviate. |
| MAY | Permitted option. |
| OPTIONAL | Permitted but not required. |

## Core Terms

| Term | Definition |
|---|---|
| Adapter | A component in an implementation that connects a source system to a knowledge manufacturing system. An Adapter is not part of the reference model core. |
| Assembly | The manufacturing stage that combines Knowledge Objects and related material according to a Production Recipe. |
| Classification | The manufacturing stage that assigns types, categories, states, or profiles to Knowledge Objects. |
| Conforming Implementation | A system that implements the required KMRM concepts and preserves required semantics such as provenance and traceability. |
| Evidence | A specific source-grounded item that supports a Knowledge Object, Relationship, decision, or generated claim. |
| Extraction | The manufacturing stage that identifies and captures relevant knowledge from Knowledge Sources. |
| Implementation | A concrete system, runtime, pipeline, tool, or platform that applies KMRM. |
| Knowledge | Structured or unstructured meaning that may be extracted, represented, related, validated, manufactured, and published. |
| Knowledge Graph | A representation of Knowledge Objects and Relationships. A Knowledge Graph is useful but is not the only possible implementation form. |
| Knowledge Object | The primary unit of structured knowledge in KMRM. A Knowledge Object represents an identifiable item of knowledge with metadata, provenance, and relationships. |
| Knowledge Product | A finished or publishable output manufactured from Knowledge Objects through a Production Recipe and Manufacturing Pipeline. |
| Knowledge Source | Any system, file, record, artefact, observation, conversation, media item, repository, database, or document from which knowledge may be extracted. |
| Lifecycle State | A recognised state in the life of a Knowledge Object, Relationship, Product, Recipe, or Publication. |
| Manufacturing Model | The KMRM specification layer that defines how Knowledge Sources, Evidence, Knowledge Objects, Relationships, Recipes, Pipelines, Quality Gates, Packaging, and Publishing interact to manufacture Knowledge Products. |
| Manufacturing Pipeline | A sequence of manufacturing stages that transforms Knowledge Sources or Knowledge Objects into Knowledge Products. |
| Manufacturing Run | One execution instance of a Manufacturing Pipeline against a declared source baseline, recipe version, and output target. |
| Manufacturing Stage | A named transformation or validation step within a Manufacturing Pipeline. |
| Metadata | Structured descriptive information about a Knowledge Source, Knowledge Object, Relationship, Product, Recipe, or Publication. |
| Normalisation | The manufacturing stage that converts extracted material into consistent structure, terminology, and format. |
| Package | A prepared form of a Knowledge Product for a specific format, channel, or publication target. |
| Packaging | The manufacturing stage that prepares a Knowledge Product for a specific format, channel, or consumption context. |
| Product Baseline | The declared set of Knowledge Objects, source versions, recipe versions, and validation results used to produce a Knowledge Product. |
| Production Cell | A specialised manufacturing capability that performs one or more stages such as Extraction, Classification, Assembly, Validation, Packaging, or Publishing. |
| Production Recipe | A repeatable specification that defines required inputs, steps, checks, and outputs for manufacturing a Knowledge Product. |
| Provenance | The record of origin, evidence, source path, extraction context, transformation history, and authorship or system responsibility for a knowledge item. |
| Publication | A released or delivered instance of a Knowledge Product in a specific format, location, version, or channel. |
| Publishing | The manufacturing stage that releases or delivers a Package to a declared channel, location, or consuming system. |
| Quality Gate | A validation checkpoint that a Knowledge Object, Relationship, Product, Package, or Publication must pass before progressing to the next stage. |
| Raw Knowledge | Knowledge before it has been extracted, structured, classified, or validated by a conforming implementation. |
| Reference Model | An implementation-independent specification of concepts, relationships, rules, and lifecycle expectations. |
| Relationship | An explicit typed link between two or more Knowledge Objects or between a Knowledge Object and another model element. |
| Source Baseline | The declared set of Knowledge Sources and versions used as input to a Manufacturing Run. |
| Source Grounding | The property that a claim, object, relationship, or product can be traced back to Evidence or a Knowledge Source. |
| Traceability | The ability to follow a Knowledge Product, claim, object, relationship, or decision back to its sources, evidence, transformations, and validation history. |
| Validation | The manufacturing stage that checks completeness, correctness, consistency, provenance, traceability, and conformance to required standards. |
| Validation Ground | A real source system, repository, corpus, product, or domain used to test whether KMRM can represent and manufacture useful outputs. |
| Waiver | An explicit recorded exception that permits a Knowledge Object, Product, Package, or Publication to proceed despite an unmet recommendation or failed Quality Gate. |

## Reserved Implementation Terms

The following terms MAY appear in implementation repositories but SHOULD NOT be treated as KMRM core primitives:

- agent;
- AIOS;
- bot;
- branch;
- embedding;
- large language model;
- prompt;
- vector database;
- web application; and
- workflow runner.

These may be useful implementation details, but KMRM SHALL remain valid without them.
