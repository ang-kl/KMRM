# Permanent Workers

## Purpose

Permanent Workers are stable Worker Profiles used repeatedly by an implementation across Manufacturing Runs.

Permanent Workers are implementation-facing. They are defined here as a reference operating pattern, not as a requirement that every KMRM implementation must use AI agents or permanent staffing.

## Principle

Permanent Workers SHALL be mapped to Production Cells.

Permanent Workers SHALL NOT define their own manufacturing logic outside the KMRM Manufacturing Model.

## Reference Permanent Worker Set

A Document Factory-like implementation SHOULD begin with the following permanent Worker Profiles.

| Permanent Worker | Primary Production Cell | Main Purpose |
|---|---|---|
| Factory Orchestrator | Planning / handoff control | Coordinates Manufacturing Runs and enforces handoff discipline. |
| Source Intake Worker | Intake Cell | Declares source scope and Source Baseline. |
| Evidence Extractor | Extraction Cell | Captures Evidence from Knowledge Sources. |
| Object Normaliser | Normalisation Cell | Converts Evidence into structured candidate Knowledge Objects. |
| Object Classifier | Classification Cell | Assigns types, states, and profiles to Knowledge Objects. |
| Relationship Mapper | Relationship Cell | Creates and validates explicit Relationships. |
| Recipe Planner | Planning Cell | Selects Production Recipes and required Quality Gates. |
| User Manual Assembler | Assembly Cell | Manufactures User Manual Knowledge Products. |
| Training Guide Assembler | Assembly Cell | Manufactures Training Guide Knowledge Products. |
| Quality Validator | Validation Cell | Applies Quality Gates and produces validation results. |
| Package Builder | Packaging Cell | Builds format-specific Packages. |
| Publisher | Publishing Cell | Releases Packages as Publications. |
| Maintenance Analyst | Maintenance Cell | Detects change impact and affected Products. |

## Factory Orchestrator

### Purpose

Coordinates the Manufacturing Run.

### Required Skills

- production planning;
- dependency tracking;
- handoff control;
- Quality Gate awareness;
- escalation management;
- Waiver tracking.

### Boundaries

The Factory Orchestrator SHALL NOT invent Knowledge Objects, mark Quality Gates as passed, or publish Packages.

## Source Intake Worker

### Purpose

Defines the Source Baseline.

### Required Skills

- source scoping;
- repository inspection;
- source version identification;
- exclusion recording;
- baseline declaration.

### Boundaries

The Source Intake Worker SHALL NOT interpret source meaning beyond intake metadata unless also operating an Extraction Cell.

## Evidence Extractor

### Purpose

Finds Evidence inside Knowledge Sources.

### Required Skills

- source reading;
- evidence citation;
- excerpt selection;
- location recording;
- ambiguity marking.

### Boundaries

The Evidence Extractor SHALL NOT convert unsupported assumptions into Evidence.

## Object Normaliser

### Purpose

Converts Evidence into structured candidate Knowledge Objects.

### Required Skills

- data structuring;
- metadata mapping;
- terminology control;
- duplicate detection;
- provenance preservation.

### Boundaries

The Object Normaliser SHALL NOT discard source context that affects meaning.

## Object Classifier

### Purpose

Assigns object type, category, profile, and lifecycle state.

### Required Skills

- taxonomy use;
- confidence marking;
- object typing;
- lifecycle state assignment;
- ambiguity escalation.

### Boundaries

The Object Classifier SHALL NOT force uncertain classification without marking uncertainty.

## Relationship Mapper

### Purpose

Creates explicit Relationships between Knowledge Objects.

### Required Skills

- dependency mapping;
- evidence-supported linking;
- conflict identification;
- relationship typing;
- graph consistency checking.

### Boundaries

The Relationship Mapper SHALL NOT create unverifiable links as if they were confirmed.

## Recipe Planner

### Purpose

Selects the correct Production Recipe and required Quality Gates.

### Required Skills

- Recipe interpretation;
- product target analysis;
- required ingredient checking;
- missing-input detection;
- gate selection.

### Boundaries

The Recipe Planner SHALL NOT alter Recipes without recording version impact.

## User Manual Assembler

### Purpose

Manufactures a User Manual Knowledge Product from validated Knowledge Objects and Relationships.

### Required Skills

- procedural writing;
- feature explanation;
- navigation structure;
- task sequencing;
- source-grounded claim handling;
- cross-reference use.

### Boundaries

The User Manual Assembler SHALL NOT invent product behaviour or publish the manual.

## Training Guide Assembler

### Purpose

Manufactures a Training Guide Knowledge Product from validated Knowledge Objects and Relationships.

### Required Skills

- learning objective formation;
- lesson sequencing;
- exercise design;
- assessment drafting;
- instructor note structuring;
- source-grounded scenario use.

### Boundaries

The Training Guide Assembler SHALL NOT invent features, learner outcomes unsupported by the Product Baseline, or publish the guide.

## Quality Validator

### Purpose

Applies required Quality Gates.

### Required Skills

- source-grounding validation;
- traceability validation;
- completeness checking;
- terminology checking;
- Recipe conformance;
- validation reporting.

### Boundaries

The Quality Validator SHALL NOT waive failed gates unless assigned Waiver authority by the implementation.

## Package Builder

### Purpose

Creates Packages from validated Knowledge Products.

### Required Skills

- format preparation;
- manifest creation;
- link checking;
- asset bundling;
- navigation generation;
- accessibility checking.

### Boundaries

The Package Builder SHALL NOT package a failed Product as release-ready without Waiver record.

## Publisher

### Purpose

Releases Packages as Publications.

### Required Skills

- publication channel handling;
- version labelling;
- release record creation;
- rollback awareness;
- access assumption recording.

### Boundaries

The Publisher SHALL NOT release a Package without required Publication preconditions.

## Maintenance Analyst

### Purpose

Detects changes and determines affected Knowledge Products.

### Required Skills

- change impact analysis;
- baseline comparison;
- affected object detection;
- affected Recipe detection;
- revalidation planning.

### Boundaries

The Maintenance Analyst SHALL NOT silently regenerate and publish affected Products without required Pipeline execution.

## Minimum Set for GIA Readiness

For a GIA User Manual and Training Guide manufacturing line, the minimum permanent workers SHOULD be:

1. Factory Orchestrator;
2. Source Intake Worker;
3. Evidence Extractor;
4. Object Normaliser;
5. Object Classifier;
6. Relationship Mapper;
7. Recipe Planner;
8. User Manual Assembler;
9. Training Guide Assembler;
10. Quality Validator;
11. Package Builder; and
12. Publisher.
