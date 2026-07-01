# Publishing

## Purpose

Publishing is the Manufacturing Stage that releases or delivers a Package to a declared channel, location, or consuming system.

Publishing creates a Publication record. A Package is not a Publication until it has been released, delivered, or otherwise made available according to a declared Publishing rule.

## Definition

A Publication SHALL identify:

- Publication identifier;
- Package identifier;
- Knowledge Product identifier;
- Product Baseline;
- Publication channel or location;
- Publication version;
- publication timestamp or release marker;
- validation status;
- responsible actor or system where known; and
- rollback or supersession status where applicable.

## Publishing Objective

Publishing SHOULD ensure that a Package is delivered in a way that preserves:

1. version clarity;
2. publication traceability;
3. access expectations;
4. channel integrity;
5. validation status;
6. rollback or supersession path;
7. retention expectations; and
8. user-facing correctness where applicable.

## Publication Channels

A Publication MAY target channels such as:

- public website;
- private website;
- static HTML site;
- help centre;
- document portal;
- learning management system;
- internal knowledge base;
- file release;
- API endpoint;
- AI retrieval corpus;
- print-ready archive; or
- implementation-specific channel.

KMRM does not prescribe one publication channel.

## Publishing Preconditions

Publishing SHALL require:

- Package exists;
- Product Baseline is recorded;
- required Quality Gates have passed or been waived;
- Publication target is declared;
- publication version is declared; and
- access or distribution assumptions are known where material.

Publishing SHOULD NOT proceed if the Package has unresolved blocking failures.

## Publication Record

A Publication record SHOULD include:

- Publication identifier;
- Package identifier;
- Package checksum or version reference where applicable;
- Knowledge Product identifier;
- Recipe version;
- Source Baseline;
- Manufacturing Run identifier;
- publication timestamp;
- channel or location;
- responsible actor or system;
- validation summary;
- known limitations;
- rollback reference;
- supersession reference; and
- retention or archival policy where applicable.

## Publishing Quality Gates

Publishing SHOULD apply Quality Gates appropriate to the channel.

Publishing Quality Gates MAY test:

- Package completeness;
- channel compatibility;
- access permissions;
- broken links;
- missing assets;
- correct version label;
- metadata availability;
- validation report availability;
- rollback readiness; and
- publication record completeness.

## Versioning

A Publication SHALL have a version, timestamp, release marker, or equivalent identity sufficient to distinguish it from prior and future Publications.

A Publication SHOULD declare whether it is:

- draft;
- preview;
- approved;
- released;
- superseded;
- deprecated; or
- withdrawn.

## Supersession

When a Publication is replaced, the new Publication SHOULD reference the prior Publication.

The prior Publication SHOULD be marked as superseded, deprecated, withdrawn, or retained according to the implementation's governance rules.

## Rollback

A Publishing process SHOULD define whether rollback is possible.

If rollback is possible, the Publication record SHOULD identify the rollback target or prior valid Publication.

If rollback is not possible, the Publication record SHOULD state that limitation where material.

## Access and Distribution

Publishing SHOULD record access assumptions when access affects use, safety, compliance, confidentiality, or operational correctness.

Access assumptions MAY include:

- public;
- private;
- internal;
- restricted;
- role-based;
- time-limited; or
- implementation-specific distribution rules.

## Publishing Failure

If Publishing fails, the failure record SHOULD include:

- Package identifier;
- Publication target;
- failed step;
- cause, if known;
- whether repackaging is required;
- whether revalidation is required;
- whether retry is permitted;
- whether rollback occurred; and
- recommended next action.

## Implementation Independence

Publishing MAY be performed by manual release, static site deployment, file upload, content management system, learning platform, build pipeline, API call, or other mechanism.

KMRM specifies Publication identity, baseline, validation status, and traceability. It does not require a particular publishing technology.
