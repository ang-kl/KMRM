# Skill Model

## Purpose

The Skill Model defines the capabilities required to operate Production Cells and Worker Profiles.

Skills describe what work must be performed. Skills do not prescribe whether the work is performed by a human, AI agent, service, script, or team.

## Skill Definition

A Skill SHALL define:

- skill name;
- purpose;
- related Production Cell;
- required inputs;
- expected outputs;
- quality expectations;
- boundary constraints; and
- escalation triggers.

## Skill Categories

KMRM defines the following standard skill categories.

| Skill Category | Purpose |
|---|---|
| Source Skills | Locate, inspect, and scope Knowledge Sources. |
| Evidence Skills | Extract, cite, and preserve Evidence. |
| Object Skills | Create, normalise, classify, and maintain Knowledge Objects. |
| Relationship Skills | Identify, create, validate, and update Relationships. |
| Recipe Skills | select, interpret, and apply Production Recipes. |
| Assembly Skills | Manufacture draft Knowledge Products from objects and recipes. |
| Validation Skills | Apply Quality Gates and report results. |
| Packaging Skills | Prepare Products for formats or channels. |
| Publishing Skills | Release Packages as Publications and record Publication metadata. |
| Maintenance Skills | Detect changes and determine affected Products. |
| Governance Skills | Manage Waivers, reviews, risks, and accountability. |

## Core Skill Set

A minimum Document Factory-like implementation SHOULD define skills for:

1. source intake;
2. evidence extraction;
3. object normalisation;
4. object classification;
5. relationship mapping;
6. recipe planning;
7. manual assembly;
8. training assembly;
9. source-grounding validation;
10. traceability validation;
11. package building; and
12. publication readiness checking.

## Skill Boundaries

A Skill SHALL NOT authorise boundary crossing by itself.

For example:

- evidence extraction skill does not authorise publication;
- product assembly skill does not authorise source invention;
- packaging skill does not authorise failed Quality Gates to be ignored;
- publishing skill does not authorise source system modification.

## Skill Maturity

An implementation MAY classify skill maturity using levels such as:

| Level | Meaning |
|---|---|
| L0 | Not available. |
| L1 | Manual or ad hoc. |
| L2 | Repeatable with checklist. |
| L3 | Defined by Worker Profile and Quality Gate. |
| L4 | Automated with review. |
| L5 | Automated, monitored, and continuously improved. |

KMRM does not require this maturity scale, but implementations SHOULD declare skill maturity when automation risk is material.

## Skill Evidence

A Worker Profile SHOULD be able to show evidence that a skill was applied.

Skill evidence MAY include:

- extracted Evidence records;
- Knowledge Object diffs;
- Relationship records;
- validation reports;
- Package manifests;
- Publication records;
- logs;
- review notes; or
- Waiver records.

## Skill Reuse

Skills SHOULD be reusable across Knowledge Product types.

For example, source-grounding validation should apply to a User Manual, Training Guide, Support Guide, and AI Context Package, even though each Product has a different Recipe.

## AI Skill Implementation

If an AI system implements a Skill, the implementation SHOULD define:

- tool access;
- source access;
- memory scope;
- output schema;
- prohibited behaviours;
- validation requirements;
- escalation triggers; and
- human review points.

These implementation details SHALL NOT redefine the KMRM Skill itself.
