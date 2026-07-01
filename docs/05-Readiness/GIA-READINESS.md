# GIA Readiness Checklist

## Purpose

This checklist defines when KMRM is ready to support a Document Factory implementation that manufactures an online HTML User Manual and online HTML Training Guide for GIA.

GIA remains a validation ground. This checklist does not place GIA-specific source data, generated manuals, or generated training guides inside KMRM.

## Readiness Target

The target implementation should be able to produce:

1. GIA online HTML User Manual;
2. GIA online HTML Training Guide;
3. Package manifests;
4. validation reports; and
5. Publication records or publication-ready bundles.

## Required KMRM Layers

The following KMRM layers SHOULD exist before GIA manufacturing begins.

| Layer | Required Status |
|---|---|
| Mission | Complete enough for implementation guidance |
| Vision | Complete enough for architectural alignment |
| Principles | Complete enough for boundary decisions |
| Terminology | Complete enough for controlled vocabulary |
| Core Concepts | Complete enough for object-centred modelling |
| Concept Map | Complete enough for implementation mapping |
| Manufacturing Model | Complete enough for pipeline design |
| Production Cell | Complete enough for worker boundaries |
| Production Pipeline | Complete enough for run design |
| Production Recipe | Complete enough for output manufacturing |
| Quality Gate | Complete enough for validation design |
| Packaging | Complete enough for HTML output packaging |
| Publishing | Complete enough for online release planning |
| Operating Model | Complete enough for worker profile mapping |
| Worker Profile | Complete enough for permanent worker design |
| Skill Model | Complete enough for capability assignment |
| Permanent Workers | Complete enough for implementation staffing |
| User Manual Recipe | Complete enough for manual manufacturing |
| Training Guide Recipe | Complete enough for guide manufacturing |

## Minimum Document Factory Capabilities

Before GIA manufacturing begins, Document Factory SHOULD implement or simulate the following capabilities:

1. Source Intake Worker;
2. Evidence Extractor;
3. Object Normaliser;
4. Object Classifier;
5. Relationship Mapper;
6. Recipe Planner;
7. User Manual Assembler;
8. Training Guide Assembler;
9. Quality Validator;
10. Package Builder; and
11. Publisher or publication-ready packager.

## Minimum GIA Source Inputs

A GIA adapter or source intake process SHOULD identify:

- repository identity;
- source branch or commit baseline;
- product identity;
- major product surfaces;
- user-facing features;
- workflows;
- screens or interface components;
- business rules;
- configuration and environment assumptions;
- existing documentation;
- known journals, registers, or build plans;
- relevant media or assets;
- known limitations; and
- unresolved ambiguity.

## Minimum Knowledge Objects for GIA

Before manufacturing the first User Manual and Training Guide, the GIA implementation SHOULD be able to create at least the following Knowledge Object types or specialisations:

- Product;
- Feature;
- Workflow;
- Screen or Interface;
- User Action;
- System Response;
- Business Rule;
- Configuration;
- Constraint;
- Error or Recovery Path;
- Glossary Term;
- Learning Objective;
- Lesson;
- Exercise; and
- Assessment Item.

## Minimum Relationships for GIA

The GIA implementation SHOULD be able to represent at least the following Relationships:

- Product contains Feature;
- Feature appears on Screen;
- Feature participates in Workflow;
- Workflow has Step;
- Step requires User Action;
- User Action produces System Response;
- Feature governed by Business Rule;
- Task requires Skill;
- Skill maps to Learning Objective;
- Learning Objective belongs to Lesson;
- Lesson includes Exercise;
- Exercise uses Feature or Workflow;
- Assessment Item tests Learning Objective.

## Required Quality Gates for First GIA Run

The first GIA manufacturing run SHOULD apply:

- Source Grounding Gate;
- Provenance Gate;
- Traceability Gate;
- Completeness Gate;
- Relationship Gate;
- Terminology Gate;
- Recipe Conformance Gate;
- Packaging Gate;
- Publishing Readiness Gate; and
- Human Review Gate.

## HTML Packaging Requirements

The first GIA HTML Packages SHOULD include:

- index page;
- navigation structure;
- section pages;
- version label;
- Product Baseline reference;
- Package manifest;
- validation summary;
- link report;
- asset gap list; and
- Publication readiness note.

## Definition of Ready

KMRM is ready for GIA when:

1. permanent worker boundaries are defined;
2. User Manual and Training Guide Recipes exist;
3. Quality Gates required by those Recipes are defined;
4. Packaging and Publishing expectations are defined;
5. GIA source intake requirements are explicit;
6. GIA minimum Knowledge Object types are declared;
7. GIA minimum Relationship types are declared;
8. first-run validation expectations are explicit; and
9. no generated GIA output is stored in KMRM.

## Next Repository Boundary

After this readiness point, work SHOULD move to a separate Document Factory implementation repository.

The Document Factory repository SHOULD contain:

- implementation runtime;
- production workers or AI agents;
- GIA adapter;
- source extraction scripts;
- object store or graph store;
- recipe execution logic;
- HTML templates;
- validators;
- package builders; and
- generated or publication-ready outputs.

KMRM SHOULD remain the governing reference model.
