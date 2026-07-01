# GIA Source Baseline

## Purpose

This document defines the generic source-baseline requirements that a Document Factory implementation SHOULD satisfy before manufacturing a GIA online HTML User Manual or GIA online HTML Training Guide.

GIA is used here as a validation ground. This document SHALL NOT store GIA source data, generated manuals, generated training guides, source extraction code, or implementation-specific prompts.

## Source Baseline Definition

A Source Baseline is a declared snapshot of source material used for a Manufacturing Run.

For GIA, the Source Baseline SHOULD identify:

- repository full name;
- default branch or selected branch;
- commit SHA or release tag;
- source intake timestamp;
- included source areas;
- excluded source areas;
- source access method;
- known source limitations;
- unresolved ambiguities; and
- responsible Source Intake Worker.

## Minimum Baseline Record

A GIA Source Baseline SHOULD contain the following fields.

```yaml
source_baseline_id: "gia-baseline-YYYYMMDD-NNN"
product_name: "GIA / Soleat"
source_system: "GitHub repository"
repository_full_name: "ang-kl/gia"
branch_or_ref: "<branch, tag, or SHA>"
commit_sha: "<resolved commit SHA>"
intake_worker: "Source Intake Worker"
intake_timestamp: "<ISO-8601 timestamp>"
implementation: "Document Factory"
intended_products:
  - "GIA online HTML User Manual"
  - "GIA online HTML Training Guide"
included_sources: []
excluded_sources: []
known_gaps: []
unresolved_ambiguities: []
review_status: "draft | reviewed | approved"
```

## Required Source Areas

A GIA source intake process SHOULD inspect source areas sufficient to identify product behaviour, user workflows, interface surfaces, existing documentation, and implementation constraints.

The implementation SHOULD consider:

| Source Area | Purpose |
|---|---|
| README or project overview files | Product identity and high-level purpose. |
| Build plans | Architecture decisions, scope, constraints, and handoff context. |
| `doc/Journal` or equivalent | Change history, decisions, and operational notes. |
| `doc/Register` or equivalent | Feature, issue, or change records where available. |
| Web application directories | Screens, interface behaviour, and user workflows. |
| Bot or server entrypoints | User interaction logic and workflow routing. |
| Configuration files | Environment assumptions and product constraints. |
| Tests or validation scripts | Expected behaviour and known assertions. |
| Assets and media | Screenshots, icons, diagrams, and publication assets. |

A source area MAY be omitted if it is irrelevant, inaccessible, duplicative, unsafe to process, or outside the Manufacturing Run scope. Omissions SHOULD be recorded.

## Source Inclusion Rules

The Source Intake Worker SHOULD classify each candidate source as:

- included;
- excluded;
- deferred;
- unknown;
- unsafe to process; or
- requires human review.

Each excluded or deferred source SHOULD include a reason.

## Source Evidence Requirements

Evidence extracted from the Source Baseline SHOULD preserve:

- source path or identifier;
- line range, object key, commit reference, or equivalent location;
- excerpt or pointer;
- extraction timestamp;
- extraction worker;
- confidence status; and
- relationship to candidate Knowledge Objects.

## Baseline Stability

A Manufacturing Run SHOULD use one declared Source Baseline.

If sources change during the run, the implementation SHOULD either:

1. continue using the declared baseline and record the newer source as deferred; or
2. create a new baseline and restart affected manufacturing stages.

## Baseline Quality Gate

Before assembly begins, the Source Baseline SHOULD pass a Source Baseline Gate.

The Source Baseline Gate SHOULD check:

- repository identity is declared;
- source ref is resolved;
- included and excluded source areas are recorded;
- intended Knowledge Products are declared;
- known gaps and ambiguities are recorded;
- minimum product identity evidence exists;
- minimum user-facing feature evidence exists or absence is recorded;
- source limitations are explicit; and
- human review status is declared where required.

## Boundary

A Source Baseline SHALL NOT by itself authorise publication.

A Source Baseline only establishes the source snapshot for downstream extraction, object normalisation, relationship mapping, assembly, validation, packaging, and publishing.

## Completion Criteria

A GIA Source Baseline is ready when:

- source identity is explicit;
- source scope is explicit;
- exclusions are justified;
- Evidence extraction can begin;
- unresolved ambiguity is recorded;
- target products are identified; and
- the baseline can be cited by Packages and Publications.
