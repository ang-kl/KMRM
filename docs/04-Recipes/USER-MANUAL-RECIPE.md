# Recipe: User Manual

## Purpose

The User Manual Recipe defines how to manufacture a User Manual Knowledge Product from source-grounded Knowledge Objects.

This recipe is generic. It is not specific to GIA, but it is intended to be sufficient for a GIA User Manual implementation profile.

## Target Product

Knowledge Product type: User Manual

A User Manual explains how users operate a product, complete tasks, understand features, recover from common problems, and navigate product workflows.

## Required Ingredients

A User Manual Recipe SHOULD require the following Knowledge Object types or specialisations:

| Ingredient | Requirement |
|---|---|
| Product Identity | Required |
| Product Purpose | Required |
| Feature | Required |
| Workflow | Required where user tasks exist |
| Screen or Interface | Required where UI exists |
| User Action | Required |
| System Response | Required where behaviour is described |
| Business Rule | Required where rules affect user behaviour |
| Configuration or Setting | Required where user-visible |
| Constraint or Limitation | Required where material |
| Error or Recovery Path | Recommended |
| Glossary Term | Recommended |
| Screenshot or Visual Asset | Optional but recommended for UI-heavy products |

## Required Relationships

The Recipe SHOULD use Relationships such as:

- Product contains Feature;
- Feature appears on Screen;
- Feature participates in Workflow;
- Workflow has Step;
- Step requires User Action;
- User Action produces System Response;
- Feature governed by Business Rule;
- Error mitigated by Recovery Path;
- Term defines Glossary Term.

## Preconditions

Assembly SHOULD NOT begin until:

- Source Baseline exists;
- Product Identity object exists;
- key Feature objects exist;
- user-facing Workflow objects exist or absence is recorded;
- required Relationships exist or missing relationship gaps are recorded;
- source grounding exists for material behaviour claims; and
- blocking ambiguity has been escalated.

## Assembly Structure

A User Manual SHOULD include:

1. product overview;
2. intended use;
3. access or launch instructions;
4. navigation overview;
5. feature guide;
6. task-based workflows;
7. settings and configuration;
8. common errors and recovery;
9. limitations;
10. glossary;
11. support or escalation path; and
12. version and source baseline note.

A lightweight User Manual MAY omit sections not applicable to the Product Baseline.

## Assembly Rules

The Assembly Cell SHALL:

- use source-grounded Feature and Workflow objects;
- distinguish confirmed behaviour from inferred behaviour;
- avoid unsupported claims;
- avoid duplicating the same explanation across many sections;
- use controlled terminology where defined;
- preserve cross-references where useful;
- mark missing screenshots or assets as gaps; and
- produce a draft Knowledge Product before Packaging.

## Required Quality Gates

The User Manual Recipe SHALL require:

- Source Grounding Gate;
- Recipe Conformance Gate;
- Completeness Gate;
- Terminology Gate;
- Traceability Gate; and
- Publishing Readiness Gate before Publication.

It SHOULD also require:

- Broken Link Gate;
- Screenshot or Asset Gate where visual references are used;
- Human Review Gate for public or user-facing manuals.

## Packaging Expectations

A User Manual Package SHOULD include:

- HTML or Markdown pages;
- navigation index;
- table of contents;
- version label;
- Product Baseline reference;
- asset references;
- link report;
- Package manifest; and
- validation summary.

## Publishing Expectations

A User Manual Publication SHOULD record:

- Publication version;
- channel or URL;
- Product Baseline;
- Recipe version;
- validation status;
- publication timestamp; and
- supersession or rollback reference where applicable.

## Completion Criteria

The User Manual Recipe is complete when:

- required sections exist or justified omissions are recorded;
- material user-facing features are represented;
- workflows are source-grounded;
- required Quality Gates pass or Waivers are recorded;
- Package is created; and
- Publication record is created if published.
