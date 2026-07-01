# Manufacturing Model

## Purpose

The Manufacturing Model defines how KMRM transforms Knowledge Sources and Knowledge Objects into Knowledge Products through repeatable, traceable, and validated manufacturing stages.

The Manufacturing Model is implementation-independent. It does not require any specific runtime, AI model, database, workflow engine, repository, or user interface.

## Model Summary

```text
Knowledge Sources
        ↓
Evidence
        ↓
Knowledge Objects
        ↓
Relationships
        ↓
Production Recipe
        ↓
Manufacturing Pipeline
        ↓
Quality Gates
        ↓
Package
        ↓
Publication
```

## Manufacturing Objective

A conforming implementation SHALL manufacture Knowledge Products in a way that preserves:

1. source grounding;
2. provenance;
3. traceability;
4. relationship integrity;
5. recipe conformance;
6. validation status;
7. lifecycle state; and
8. publication baseline.

## Manufacturing Stages

A Manufacturing Pipeline MAY include the following stages.

| Stage | Purpose | Typical Output |
|---|---|---|
| Intake | Declare the Knowledge Sources and Source Baseline. | Source Baseline |
| Extraction | Capture relevant Evidence from Knowledge Sources. | Evidence records |
| Normalisation | Convert extracted material into consistent structure. | Normalised Evidence or draft Knowledge Objects |
| Classification | Assign object types, states, categories, and profiles. | Typed Knowledge Objects |
| Relationship Building | Establish explicit Relationships between Knowledge Objects. | Relationship set or Knowledge Graph |
| Planning | Select Recipes, outputs, and required Quality Gates. | Manufacturing plan |
| Assembly | Combine Knowledge Objects according to a Production Recipe. | Draft Knowledge Product |
| Validation | Apply Quality Gates. | Validation report |
| Packaging | Prepare the validated Product for a format or channel. | Package |
| Publishing | Release or deliver the Package. | Publication |
| Maintenance | Update affected Products when sources, objects, or recipes change. | Revised Product or Publication |

A conforming implementation MAY combine stages or split stages into finer-grained operations, provided the required semantics are preserved.

## Manufacturing Run

A Manufacturing Run is one execution instance of a Manufacturing Pipeline.

A Manufacturing Run SHALL identify:

- the Source Baseline;
- the Production Recipe version;
- the target Knowledge Product;
- required Quality Gates;
- selected Packaging target;
- intended Publication channel, if applicable;
- execution timestamp or version; and
- responsible actor or system where known.

A Manufacturing Run SHOULD produce a record sufficient to explain how the resulting Knowledge Product was manufactured.

## Source Baseline

A Source Baseline declares the Knowledge Sources and source versions used in a Manufacturing Run.

A Source Baseline SHOULD include:

- source identifiers;
- source version references;
- extraction time or snapshot time;
- access assumptions;
- excluded sources, if material;
- known source limitations; and
- unresolved ambiguity.

A Knowledge Product SHALL NOT be treated as reproducible unless its Source Baseline is known or intentionally waived.

## Manufacturing Inputs

A Manufacturing Pipeline MAY consume:

- Knowledge Sources;
- Evidence;
- Knowledge Objects;
- Relationships;
- Metadata;
- Production Recipes;
- Quality Gate specifications;
- Packaging requirements; and
- Publication requirements.

A Manufacturing Pipeline SHALL distinguish between source-grounded inputs and generated or inferred material.

## Manufacturing Outputs

A Manufacturing Pipeline MAY produce:

- Evidence records;
- Knowledge Objects;
- Relationships;
- validation reports;
- Knowledge Products;
- Packages;
- Publications;
- maintenance notices; and
- waiver records.

Every output that affects a Knowledge Product SHOULD be traceable to the Manufacturing Run that produced it.

## Manufacturing Constraints

A conforming implementation SHALL NOT:

- discard provenance without recording a Waiver;
- present unverified generated content as source-grounded evidence;
- treat a failed required Quality Gate as passed;
- publish a Package without a known Product Baseline or recorded Waiver; or
- allow implementation-specific shortcuts to redefine the KMRM core model.

## AI and Automation

AI systems, automation, scripts, human reviewers, or mixed teams MAY perform Manufacturing Stages.

KMRM does not define permanent agents, job titles, prompts, or vendor-specific tooling. Those belong to implementations or implementation profiles.

The Manufacturing Model defines the work that must be preserved and validated, not the worker that performs it.

## Relationship to Document Factory

Document Factory MAY implement this Manufacturing Model by providing runtime components, production cells, recipes, validators, publishers, and adapters.

Such implementation details SHALL remain outside KMRM unless they are documented as non-normative examples.
