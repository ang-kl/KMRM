# Recipe: Training Guide

## Purpose

The Training Guide Recipe defines how to manufacture a Training Guide Knowledge Product from source-grounded Knowledge Objects.

This recipe is generic. It is not specific to GIA, but it is intended to be sufficient for a GIA Training Guide implementation profile.

## Target Product

Knowledge Product type: Training Guide

A Training Guide helps learners acquire practical competence in using, supporting, teaching, or operating a product.

## Required Ingredients

A Training Guide Recipe SHOULD require the following Knowledge Object types or specialisations:

| Ingredient | Requirement |
|---|---|
| Product Identity | Required |
| Product Purpose | Required |
| Feature | Required |
| Workflow | Required |
| Task | Required |
| Skill or Competency | Required |
| Learning Objective | Required |
| Lesson | Required |
| Exercise | Required |
| Assessment Item | Recommended |
| Scenario | Recommended |
| Common Error | Recommended |
| Recovery Path | Recommended |
| Glossary Term | Recommended |
| Visual Asset | Optional but recommended |

## Required Relationships

The Recipe SHOULD use Relationships such as:

- Product contains Feature;
- Feature supports Task;
- Task requires Skill;
- Skill maps to Learning Objective;
- Learning Objective belongs to Lesson;
- Lesson includes Exercise;
- Exercise uses Scenario;
- Assessment Item tests Learning Objective;
- Common Error relates to Recovery Path;
- Glossary Term supports Lesson.

## Preconditions

Assembly SHOULD NOT begin until:

- Source Baseline exists;
- Product Identity object exists;
- target learner context is declared;
- key Feature and Workflow objects exist;
- source-grounded tasks are identified;
- Learning Objectives are grounded in actual product behaviour;
- required Relationships exist or missing relationship gaps are recorded; and
- blocking ambiguity has been escalated.

## Assembly Structure

A Training Guide SHOULD include:

1. training overview;
2. learner prerequisites;
3. learning objectives;
4. module structure;
5. lesson plans;
6. step-by-step exercises;
7. guided practice;
8. independent practice;
9. common mistakes;
10. troubleshooting or recovery;
11. assessment or check-for-understanding;
12. trainer notes where applicable;
13. glossary; and
14. version and source baseline note.

A lightweight Training Guide MAY omit sections not applicable to the Product Baseline.

## Assembly Rules

The Assembly Cell SHALL:

- base lessons on source-grounded product behaviour;
- distinguish training interpretation from source evidence;
- avoid inventing features, workflows, or competencies;
- map each major exercise to a Feature, Workflow, or Task;
- map each assessment item to a Learning Objective;
- preserve terminology consistency;
- mark missing screenshots or media as gaps; and
- produce a draft Knowledge Product before Packaging.

## Required Quality Gates

The Training Guide Recipe SHALL require:

- Source Grounding Gate;
- Recipe Conformance Gate;
- Completeness Gate;
- Learning Objective Gate;
- Exercise Traceability Gate;
- Terminology Gate;
- Traceability Gate; and
- Publishing Readiness Gate before Publication.

It SHOULD also require:

- Human Review Gate for instructor-facing or public training;
- Accessibility Gate where learners consume digital material;
- Asset Gate where screenshots, videos, or diagrams are referenced.

## Packaging Expectations

A Training Guide Package SHOULD include:

- HTML or Markdown pages;
- module navigation;
- lesson index;
- exercise files or instructions;
- assessment items;
- trainer notes where applicable;
- version label;
- Product Baseline reference;
- asset references;
- Package manifest; and
- validation summary.

## Publishing Expectations

A Training Guide Publication SHOULD record:

- Publication version;
- channel or URL;
- target learner context;
- Product Baseline;
- Recipe version;
- validation status;
- publication timestamp; and
- supersession or rollback reference where applicable.

## Completion Criteria

The Training Guide Recipe is complete when:

- required modules and lessons exist or justified omissions are recorded;
- exercises map to source-grounded tasks;
- learning objectives are explicit;
- assessment or check-for-understanding items exist where required;
- required Quality Gates pass or Waivers are recorded;
- Package is created; and
- Publication record is created if published.
