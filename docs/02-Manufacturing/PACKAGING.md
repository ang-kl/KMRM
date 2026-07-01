# Packaging

## Purpose

Packaging is the Manufacturing Stage that prepares a validated Knowledge Product for a specific format, channel, or consumption context.

Packaging is distinct from Assembly. Assembly creates the Knowledge Product. Packaging prepares it for delivery.

## Definition

A Package is a prepared form of a Knowledge Product.

A Package SHALL identify:

- source Knowledge Product;
- Product Baseline;
- Package format;
- Packaging rules;
- Packaging timestamp or version;
- validation status;
- intended Publication channel, if known; and
- Packaging actor or system where known.

## Packaging Objective

Packaging SHOULD preserve:

1. product meaning;
2. provenance references;
3. traceability metadata;
4. version identity;
5. accessibility requirements where applicable;
6. navigation structure where applicable;
7. format integrity; and
8. publication readiness.

## Package Formats

A Package MAY target formats such as:

- HTML;
- Markdown;
- PDF;
- DOCX;
- slides;
- structured JSON;
- static website;
- help centre article set;
- learning management system import;
- AI context package;
- media script bundle; or
- implementation-specific format.

KMRM does not prescribe one packaging format.

## Packaging Inputs

Packaging MAY consume:

- validated Knowledge Product;
- Product Baseline;
- validation report;
- Packaging requirements;
- style rules;
- accessibility requirements;
- channel constraints;
- navigation requirements;
- asset references; and
- Publication requirements.

## Packaging Outputs

Packaging MAY produce:

- Package files;
- Package manifest;
- navigation index;
- asset bundle;
- metadata record;
- validation report;
- Publication-ready bundle; or
- Package failure report.

## Package Manifest

A Package SHOULD include or reference a manifest.

A Package manifest SHOULD record:

- Package identifier;
- Knowledge Product identifier;
- Knowledge Product version;
- Product Baseline;
- Recipe version;
- Package format;
- generated files or artefacts;
- included assets;
- required external dependencies;
- validation status;
- known limitations; and
- intended Publication channel.

## Packaging Quality Gates

Packaging SHOULD apply Quality Gates appropriate to the output format and channel.

Packaging Quality Gates MAY test:

- file completeness;
- navigation completeness;
- broken links;
- missing assets;
- metadata presence;
- accessibility requirements;
- format validity;
- citation or provenance display;
- version label correctness; and
- publication readiness.

## Separation from Publishing

Packaging SHALL NOT be treated as Publishing.

A Package may be ready for Publication but not yet released.

Publishing requires a Publication record or delivery event.

## Traceability in Packages

A Package SHALL preserve enough metadata to trace the packaged output back to:

- Knowledge Product;
- Production Recipe;
- Source Baseline;
- Manufacturing Run;
- required Quality Gates; and
- Packaging rules.

The traceability metadata MAY be visible to end users or retained in an internal manifest, depending on the Product type and Publication context.

## Packaging Failure

If Packaging fails, the result SHOULD record:

- failed Packaging rule;
- affected file or artefact;
- cause, if known;
- whether reassembly is required;
- whether revalidation is required;
- whether a Waiver is allowed; and
- recommended next action.

## Implementation Independence

Packaging MAY be performed by static site generators, document converters, scripts, manual procedures, AI systems, build pipelines, or other tools.

KMRM requires preservation of Package identity, baseline, validation state, and traceability. It does not require a particular packaging technology.
