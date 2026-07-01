# Company Policies Pattern

## Purpose

The Company Policies Pattern defines reusable governance policies for a knowledge manufacturing implementation.

The term company is metaphorical. A conforming implementation MAY use these policies whether it is operated by a solo builder, team, organisation, AI agents, scripts, or hybrid workers.

## Policy Principle

A policy SHALL state a durable rule that constrains Worker Profiles, Production Cells, Manufacturing Pipelines, or Publications.

Policies SHOULD be explicit, reviewable, versioned, and testable where possible.

## Minimum Policy Set

A Document Factory-like implementation SHOULD define policies for:

1. source grounding;
2. provenance preservation;
3. terminology control;
4. non-invention;
5. validation before publication;
6. waiver handling;
7. versioning;
8. access boundaries;
9. human review; and
10. release readiness.

## Source Grounding Policy

A Worker Profile SHALL distinguish source-grounded content from generated phrasing, inference, and unresolved ambiguity.

A Knowledge Product SHOULD identify the Knowledge Objects and Evidence used to manufacture it.

## Non-Invention Policy

A Worker Profile SHALL NOT present unsupported product behaviour, business rules, procedures, or claims as source-grounded knowledge.

If a needed fact is unavailable, the Worker Profile SHOULD mark it as missing, ambiguous, or requiring review.

## Provenance Policy

A Manufacturing Pipeline SHALL preserve provenance across extraction, normalisation, classification, relationship mapping, assembly, validation, packaging, and publishing.

A pipeline SHALL NOT discard provenance merely because output text has been rewritten, summarised, translated, or reformatted.

## Terminology Policy

A Worker Profile SHOULD use controlled terminology from the applicable terminology source.

A Worker Profile SHOULD NOT introduce new terms into publishable Knowledge Products without review when terminology consistency is required.

## Validation Policy

A Knowledge Product SHALL pass required Quality Gates before publication unless a Waiver is explicitly recorded.

A validation result SHOULD record:

- Quality Gate identifier;
- status;
- evidence checked;
- failed checks;
- warnings;
- reviewer or worker identity; and
- timestamp or run identifier.

## Waiver Policy

A Waiver MAY permit progress despite a failed or incomplete Quality Gate.

A Waiver SHALL record:

- waived requirement;
- reason;
- scope;
- expiry or review condition;
- responsible approver; and
- affected Products or Publications.

## Access Boundary Policy

A Worker Profile SHALL operate only on permitted sources, tools, objects, and outputs.

A Worker Profile SHALL NOT modify source systems, publish products, approve waivers, or change recipes unless its profile explicitly grants that authority.

## Human Review Policy

Human review SHOULD be required when a Knowledge Product affects:

- user-facing guidance;
- training outcomes;
- compliance;
- safety;
- financial decisions;
- external publication;
- organisational policy; or
- irreversible release actions.

## Performance Policy

Worker performance SHOULD be reviewed against quality, traceability, completeness, rework rate, and boundary compliance.

Performance review SHALL NOT redefine the KMRM model. It MAY improve Worker Profiles, skills, recipes, checklists, or implementation behaviour.

## Policy Versioning

Policies SHOULD be versioned when used for repeatable Manufacturing Runs.

A Publication SHOULD record which policy version or baseline applied at release time.
