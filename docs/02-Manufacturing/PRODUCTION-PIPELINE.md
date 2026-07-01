# Production Pipeline

## Purpose

A Production Pipeline is an ordered manufacturing process that transforms Knowledge Sources, Evidence, Knowledge Objects, and Relationships into Knowledge Products, Packages, or Publications.

A Production Pipeline defines process order, handoffs, required Quality Gates, and traceability expectations.

## Definition

A Production Pipeline SHALL define:

- pipeline name;
- pipeline purpose;
- input requirements;
- output target;
- Manufacturing Stages;
- Production Cells or equivalent capabilities;
- required Quality Gates;
- provenance requirements;
- failure handling;
- Waiver rules; and
- completion criteria.

## Pipeline Pattern

A standard KMRM Production Pipeline SHOULD follow this pattern unless a justified profile defines otherwise.

```text
1. Intake
2. Extraction
3. Normalisation
4. Classification
5. Relationship Building
6. Planning
7. Assembly
8. Validation
9. Packaging
10. Publishing
11. Maintenance
```

An implementation MAY omit, combine, or repeat stages, but it SHALL preserve provenance and validation semantics.

## Stage Requirements

### 1. Intake

Intake SHALL declare the Source Baseline and manufacturing scope.

Intake SHOULD identify:

- included Knowledge Sources;
- excluded Knowledge Sources;
- source versions;
- source limitations;
- target Knowledge Products; and
- initial ambiguity.

### 2. Extraction

Extraction SHALL identify Evidence from Knowledge Sources.

Extraction SHOULD preserve source location, version, and context.

### 3. Normalisation

Normalisation SHALL convert extracted material into consistent structure without erasing source meaning.

Normalisation SHOULD record material transformations.

### 4. Classification

Classification SHALL assign types, categories, states, or profiles needed for later manufacturing.

Classification SHOULD distinguish certain, inferred, and uncertain assignments.

### 5. Relationship Building

Relationship Building SHALL create explicit Relationships required for manufacturing or validation.

Relationship Building SHOULD identify relationship confidence or evidence where appropriate.

### 6. Planning

Planning SHALL select the Production Recipe, target Knowledge Product, required Quality Gates, and Packaging target.

Planning SHOULD detect missing inputs before Assembly begins.

### 7. Assembly

Assembly SHALL manufacture a draft Knowledge Product according to the selected Production Recipe.

Assembly SHALL distinguish generated wording from source-grounded claims.

### 8. Validation

Validation SHALL apply required Quality Gates.

Validation SHALL produce a validation result for each required Quality Gate.

### 9. Packaging

Packaging SHALL prepare the validated Knowledge Product for a declared output format or channel.

Packaging SHOULD preserve Product Baseline and recipe information.

### 10. Publishing

Publishing SHALL release or deliver the Package as a Publication.

Publishing SHALL record the Publication location, version, channel, or delivery target where applicable.

### 11. Maintenance

Maintenance SHOULD identify affected Knowledge Products when Knowledge Sources, Knowledge Objects, Relationships, Recipes, or Quality Gates change.

## Pipeline Metadata

A Production Pipeline SHOULD carry metadata including:

- pipeline identifier;
- pipeline version;
- owner or responsible actor;
- Production Recipe reference;
- Source Baseline reference;
- target Product type;
- required Quality Gates;
- Packaging format;
- Publication target;
- execution state; and
- completion timestamp where applicable.

## Pipeline States

A Production Pipeline MAY use the following lifecycle states:

| State | Meaning |
|---|---|
| Draft | Pipeline is being designed. |
| Ready | Pipeline can be executed. |
| Running | Pipeline is currently executing. |
| Blocked | Pipeline cannot proceed due to missing input, failed gate, or unresolved ambiguity. |
| Validated | Required Quality Gates have passed. |
| Packaged | Output has been prepared for publication. |
| Published | Output has been released or delivered. |
| Superseded | Pipeline version has been replaced. |
| Retired | Pipeline is no longer intended for use. |

## Failure Handling

A Production Pipeline SHALL define how failures are handled.

Failures MAY result in:

- retry;
- quarantine;
- human review;
- source correction;
- Recipe revision;
- Quality Gate revision;
- Waiver; or
- termination of the Manufacturing Run.

A failed required Quality Gate SHALL NOT be silently ignored.

## Reproducibility

A Production Pipeline SHOULD be reproducible when given the same Source Baseline, Production Recipe version, Quality Gate set, and Packaging target.

If reproducibility is not possible, the implementation SHOULD record why.

## Implementation Independence

A Production Pipeline MAY be implemented through scripts, workflow engines, human procedures, AI orchestration, document processes, or hybrid systems.

KMRM specifies required semantics, not the execution technology.
