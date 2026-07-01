# Production Recipe

## Purpose

A Production Recipe is a repeatable specification for manufacturing a Knowledge Product.

A Production Recipe defines the required ingredients, assembly steps, Quality Gates, Packaging expectations, and Publication requirements for one type of Knowledge Product.

## Definition

A Production Recipe SHALL define:

- recipe identifier;
- recipe name;
- recipe version;
- target Knowledge Product type;
- required input Knowledge Object types;
- optional input Knowledge Object types;
- required Relationships;
- Assembly rules;
- required Quality Gates;
- Packaging expectations;
- Publication expectations, if applicable; and
- failure or Waiver handling.

## Recipe Is Not a Prompt

A Production Recipe SHALL NOT be replaced by a prompt.

A prompt MAY be used by an implementation to perform a step within a Production Recipe. The recipe remains the governing specification.

This distinction preserves implementation independence and prevents vendor-specific instructions from becoming the reference model.

## Recipe Structure

A Production Recipe SHOULD follow this structure:

```text
Recipe
├── Identity
├── Purpose
├── Target Product
├── Ingredients
├── Preconditions
├── Assembly Steps
├── Quality Gates
├── Packaging Rules
├── Publishing Rules
├── Traceability Rules
├── Waiver Rules
└── Completion Criteria
```

## Ingredients

Recipe ingredients MAY include:

- Knowledge Objects;
- Evidence;
- Relationships;
- Metadata;
- examples;
- source excerpts;
- glossary terms;
- prior Publications;
- validation reports; and
- implementation-specific artefacts.

Each required ingredient SHOULD specify:

- object type or source type;
- minimum required state;
- required provenance level;
- required relationship type;
- completeness expectation; and
- fallback behaviour if missing.

## Preconditions

A Production Recipe SHALL define the conditions required before Assembly may begin.

Preconditions MAY include:

- Source Baseline exists;
- required Knowledge Objects exist;
- required Evidence exists;
- required Relationships exist;
- terminology has been validated;
- no blocking ambiguity remains; and
- required prior Quality Gates have passed.

## Assembly Rules

Assembly rules define how ingredients become a draft Knowledge Product.

Assembly rules SHOULD specify:

- required product structure;
- section ordering;
- claim grounding requirements;
- use of examples;
- treatment of uncertainty;
- permitted inference;
- prohibited invention;
- cross-reference rules; and
- output style constraints where relevant.

## Quality Gates

A Production Recipe SHALL identify required Quality Gates.

A recipe MAY also identify recommended or optional Quality Gates.

Required Quality Gates SHALL pass or be explicitly waived before the Knowledge Product is treated as publishable.

## Packaging Rules

Packaging rules define how the Knowledge Product is prepared for output.

Packaging rules MAY specify:

- format;
- file structure;
- navigation structure;
- accessibility expectations;
- metadata inclusion;
- version label;
- citation or provenance display; and
- channel-specific requirements.

## Publishing Rules

Publishing rules define whether and how a Package may become a Publication.

Publishing rules SHOULD specify:

- publication channel;
- approval requirement;
- release version;
- audience or consumption context where applicable;
- rollback expectation;
- retention expectation; and
- Publication record requirements.

## Traceability Rules

A Production Recipe SHALL define what traceability must be preserved in the resulting Knowledge Product or Product Baseline.

Traceability MAY be visible in the final Product or retained in manufacturing metadata, depending on Product type and Publication context.

## Waiver Rules

A Production Recipe SHOULD define which failures may be waived, who or what may approve a Waiver, and what must be recorded.

A Waiver SHOULD include:

- failed requirement;
- reason;
- approving actor or system;
- expiry or review condition;
- risk note; and
- affected Product or Publication.

## Completion Criteria

A Production Recipe SHALL define completion criteria.

Completion criteria MAY include:

- required sections generated;
- required objects represented;
- required Quality Gates passed;
- Product Baseline recorded;
- Package produced;
- Publication created; and
- maintenance hooks registered.

## Example Recipe Targets

Examples of Knowledge Products that may be manufactured by Production Recipes include:

- User Manual;
- Training Guide;
- Curriculum;
- FAQ;
- Support Guide;
- API Documentation;
- Release Notes;
- Policy Manual;
- AI Context Package; and
- Media Script.

These examples are not KMRM core primitives. They are Knowledge Product specialisations.
