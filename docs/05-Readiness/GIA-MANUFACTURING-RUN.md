# GIA Manufacturing Run Profile

## Purpose

This document defines the minimum Manufacturing Run profile for producing a GIA online HTML User Manual and GIA online HTML Training Guide through a KMRM-conforming Document Factory implementation.

This document is a readiness profile. It does not implement the run, execute adapters, generate HTML, or store generated outputs.

## Manufacturing Run Definition

A Manufacturing Run is a declared execution of Production Recipes against a Source Baseline to create one or more Knowledge Products.

For the first GIA run, the intended Knowledge Products are:

1. GIA online HTML User Manual;
2. GIA online HTML Training Guide.

## Minimum Run Record

A GIA Manufacturing Run SHOULD declare:

```yaml
manufacturing_run_id: "gia-run-YYYYMMDD-NNN"
source_baseline_id: "gia-baseline-YYYYMMDD-NNN"
implementation: "Document Factory"
run_type: "initial-manufacture | refresh | partial-refresh | validation-only"
recipes:
  - "User Manual Recipe"
  - "Training Guide Recipe"
worker_profiles:
  - "Factory Orchestrator"
  - "Source Intake Worker"
  - "Evidence Extractor"
  - "Object Normaliser"
  - "Object Classifier"
  - "Relationship Mapper"
  - "Recipe Planner"
  - "User Manual Assembler"
  - "Training Guide Assembler"
  - "Quality Validator"
  - "Package Builder"
  - "Publisher or publication-ready packager"
quality_gates: []
expected_packages: []
review_status: "draft | reviewed | approved"
```

## Required Production Cells

The first GIA run SHOULD include the following Production Cells:

| Production Cell | Required Purpose |
|---|---|
| Intake Cell | Declare source scope and baseline. |
| Extraction Cell | Extract Evidence from source material. |
| Normalisation Cell | Create candidate Knowledge Objects. |
| Classification Cell | Classify objects by type, state, and profile. |
| Relationship Cell | Map objects into explicit relationships. |
| Planning Cell | Select recipes, gates, and product targets. |
| Assembly Cell | Manufacture draft User Manual and Training Guide. |
| Validation Cell | Apply required Quality Gates. |
| Packaging Cell | Build HTML-ready packages and manifests. |
| Publishing Cell | Create Publication record or publication-ready status. |

## Required Worker Profiles

The first GIA run SHOULD include the minimum permanent Worker Profiles already defined in KMRM:

- Factory Orchestrator;
- Source Intake Worker;
- Evidence Extractor;
- Object Normaliser;
- Object Classifier;
- Relationship Mapper;
- Recipe Planner;
- User Manual Assembler;
- Training Guide Assembler;
- Quality Validator;
- Package Builder; and
- Publisher or publication-ready packager.

## Stage Handoffs

Each stage handoff SHOULD produce a handoff record.

A handoff record SHOULD identify:

- source stage;
- target stage;
- inputs delivered;
- outputs delivered;
- known gaps;
- failed checks;
- unresolved ambiguity;
- responsible worker; and
- next required action.

## First-Run Quality Gates

The first GIA run SHOULD apply at least:

1. Source Baseline Gate;
2. Source Grounding Gate;
3. Provenance Gate;
4. Traceability Gate;
5. Relationship Gate;
6. Recipe Conformance Gate;
7. Completeness Gate;
8. Terminology Gate;
9. Asset Gap Gate;
10. Packaging Gate;
11. Publishing Readiness Gate; and
12. Human Review Gate.

## Run Boundaries

The first GIA Manufacturing Run SHALL NOT:

- modify the GIA source repository;
- infer product behaviour without marking inference;
- publish generated HTML without required review;
- suppress missing source evidence;
- treat generated text as Evidence;
- bypass required Quality Gates without Waiver; or
- store generated GIA output in KMRM.

## Expected Intermediate Outputs

A GIA run SHOULD produce or simulate:

- Source Baseline record;
- Evidence records;
- candidate Knowledge Object inventory;
- Relationship inventory;
- missing input report;
- recipe plan;
- draft User Manual Knowledge Product;
- draft Training Guide Knowledge Product;
- validation report;
- package manifest; and
- publication readiness record.

## Completion Criteria

The GIA Manufacturing Run is complete when:

- both target Products are assembled or justified as incomplete;
- required Quality Gates pass or Waivers are recorded;
- Package manifests exist;
- Publication readiness is recorded;
- gaps are listed;
- generated outputs remain outside KMRM; and
- source baseline traceability is preserved.
