# Organisation Model

## Purpose

The Organisation Model defines how a conforming implementation may organise Worker Profiles, Production Cells, responsibilities, governance, and escalation paths.

This model does not require a literal company, department hierarchy, or AI agent framework. It provides a reference pattern for assigning durable responsibilities in a knowledge manufacturing system.

## Principle

An Organisation Model SHALL make responsibility explicit.

A conforming implementation SHOULD define:

- who or what coordinates a Manufacturing Run;
- which Worker Profiles operate each Production Cell;
- which Worker Profiles may approve, reject, waive, or publish;
- which decisions require human review;
- which actions are prohibited; and
- how escalation occurs when uncertainty, conflict, or risk is detected.

## Reference Organisation Pattern

A Document Factory-like implementation MAY use the following reference organisation pattern:

```text
Founder / Human Accountable Owner
        ↓
Factory Orchestrator
        ↓
Production Cells
        ├── Intake Cell
        ├── Extraction Cell
        ├── Normalisation Cell
        ├── Classification Cell
        ├── Relationship Cell
        ├── Planning Cell
        ├── Assembly Cell
        ├── Validation Cell
        ├── Packaging Cell
        ├── Publishing Cell
        └── Maintenance Cell
```

## Permanent Worker Alignment

Each Production Cell SHOULD be operated by one or more Permanent Workers.

A Permanent Worker SHALL have a Worker Profile before it performs repeatable work in a conforming implementation.

## Reference Office Pattern

An implementation MAY group Worker Profiles into offices for operational convenience.

```text
Factory Office
  Factory Orchestrator
  Recipe Planner
  Maintenance Analyst

Knowledge Office
  Source Intake Worker
  Evidence Extractor
  Object Normaliser
  Object Classifier
  Relationship Mapper

Product Office
  User Manual Assembler
  Training Guide Assembler

Quality Office
  Quality Validator

Publishing Office
  Package Builder
  Publisher
```

These offices are OPTIONAL. They SHALL NOT redefine the Production Cells or override the Manufacturing Model.

## Authority Boundaries

Authority SHALL be separated where risk is material.

An implementation SHOULD separate:

- evidence extraction from source invention;
- assembly from validation;
- validation from waiver approval;
- packaging from publishing;
- publishing from source modification; and
- maintenance analysis from automatic release.

## Human Accountability

A conforming implementation SHOULD identify a Human Accountable Owner when Knowledge Products affect users, training, operations, compliance, public communication, or financial decisions.

The Human Accountable Owner MAY delegate manufacturing work to Worker Profiles but remains accountable for approval policy and risk acceptance.

## Contractor Pattern

An implementation MAY use temporary Worker Profiles for specialised work such as translation, accessibility review, legal review, visual design, or domain expertise.

Temporary workers SHALL declare:

- limited purpose;
- permitted inputs;
- permitted outputs;
- review requirement;
- expiry condition; and
- prohibited actions.

## Non-Goals

The Organisation Model SHALL NOT prescribe:

- one company hierarchy;
- one staffing model;
- one AI framework;
- one vendor;
- one number of agents;
- one team size; or
- one implementation repository layout.
