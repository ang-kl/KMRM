# Worker Profile

## Purpose

A Worker Profile defines the stable responsibilities, skills, inputs, outputs, and boundaries of a worker that operates one or more Production Cells.

A Worker Profile may later be implemented as a human role, AI agent, service, script, team, or hybrid operating unit.

## Required Structure

A Worker Profile SHALL define:

```text
Worker Profile
├── Identity
├── Purpose
├── Cell Alignment
├── Required Skills
├── Inputs
├── Outputs
├── Boundaries
├── Quality Gate Duties
├── Provenance Duties
├── Escalation Rules
├── Prohibited Actions
└── Review Requirements
```

## Identity

Identity SHOULD include:

- profile identifier;
- profile name;
- profile version;
- owning implementation or profile set;
- active or retired status; and
- related Production Cells.

## Cell Alignment

Every Worker Profile SHALL identify the Production Cell or Cells it operates.

If a Worker Profile spans multiple cells, the profile SHALL define when it is operating in each cell and what boundaries apply in each context.

## Required Skills

Required skills SHOULD be expressed as capabilities rather than technologies.

Examples include:

- source inspection;
- evidence extraction;
- terminology control;
- object classification;
- relationship mapping;
- recipe planning;
- product assembly;
- validation;
- packaging;
- publishing;
- change impact analysis; and
- ambiguity escalation.

A skill MAY later be implemented by AI, human judgement, deterministic code, or another mechanism.

## Inputs

A Worker Profile SHALL define permitted inputs.

Inputs SHOULD declare whether they are:

- source-grounded;
- inferred;
- generated;
- manually supplied;
- validated;
- unvalidated; or
- implementation-specific.

## Outputs

A Worker Profile SHALL define permitted outputs.

Outputs SHOULD be typed as:

- Evidence;
- Knowledge Object;
- Relationship;
- Manufacturing Plan;
- Knowledge Product;
- Quality Gate result;
- Package;
- Publication;
- Waiver; or
- implementation-specific artefact.

## Boundaries

A Worker Profile SHALL define what the worker SHALL NOT do.

Boundary statements SHOULD be explicit, testable, and aligned to Production Cell responsibilities.

## Escalation Rules

A Worker Profile SHOULD escalate when:

- required inputs are missing;
- source evidence conflicts;
- source grounding is insufficient;
- required Quality Gates fail;
- a Recipe cannot be satisfied;
- a Publication target is ambiguous;
- a boundary would be crossed; or
- human review is required.

## Quality Gate Duties

A Worker Profile MAY own, trigger, or respond to Quality Gates.

A Worker Profile SHALL NOT mark a required Quality Gate as passed unless its pass criteria are satisfied.

## Provenance Duties

A Worker Profile SHALL preserve provenance required by its Production Cell.

If the worker transforms, summarises, assembles, or packages content, it SHOULD record enough information to maintain traceability to source Knowledge Objects and Evidence.

## Prohibited Actions

A Worker Profile SHALL NOT:

- invent unsupported source claims;
- hide uncertainty;
- silently remove provenance;
- publish without required validation;
- bypass human review where required;
- modify source systems outside its authority;
- change Recipes without recording version impact; or
- treat generated content as Evidence.

## Review Requirements

A Worker Profile SHOULD declare whether its outputs require:

- no review;
- peer review;
- automated validation;
- human approval;
- owner approval;
- legal or compliance approval; or
- implementation-specific governance.

## Template

```markdown
# Worker Profile: <Name>

## Purpose

## Cell Alignment

## Required Skills

## Permitted Inputs

## Permitted Outputs

## Boundaries

## Quality Gate Duties

## Provenance Duties

## Escalation Rules

## Prohibited Actions

## Review Requirements
```
