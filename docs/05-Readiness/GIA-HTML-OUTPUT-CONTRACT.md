# GIA HTML Output Contract

## Purpose

This document defines the minimum output contract for GIA online HTML Knowledge Products manufactured by a KMRM-conforming Document Factory implementation.

The contract applies to:

1. GIA online HTML User Manual;
2. GIA online HTML Training Guide.

This document does not contain generated HTML output.

## Output Contract Principle

An HTML Knowledge Product Package SHOULD be navigable, versioned, source-baseline aware, validation-aware, and publication-ready.

A Package SHALL NOT be treated as publishable unless required Quality Gates pass or Waivers are recorded.

## Required Package Structure

Each GIA HTML Package SHOULD include:

```text
package-root/
├── index.html
├── manifest.json
├── validation-summary.html or validation-summary.json
├── source-baseline.html or source-baseline.json
├── assets/
├── sections/
└── link-report.json
```

An implementation MAY use another structure if it preserves equivalent navigation, traceability, packaging, and validation semantics.

## User Manual HTML Minimum Sections

The GIA User Manual Package SHOULD include pages or sections for:

1. product overview;
2. intended use;
3. access or launch instructions;
4. navigation overview;
5. feature guide;
6. task-based workflows;
7. settings or configuration where user-visible;
8. common errors and recovery;
9. limitations;
10. glossary;
11. support or escalation path;
12. source baseline note; and
13. validation summary.

Sections MAY be omitted only if omission is recorded and justified by the Product Baseline.

## Training Guide HTML Minimum Sections

The GIA Training Guide Package SHOULD include pages or sections for:

1. training overview;
2. learner prerequisites;
3. learning objectives;
4. module structure;
5. lesson plans;
6. guided exercises;
7. independent practice;
8. common mistakes;
9. troubleshooting or recovery;
10. assessment or check-for-understanding;
11. trainer notes where applicable;
12. glossary;
13. source baseline note; and
14. validation summary.

Sections MAY be omitted only if omission is recorded and justified by the Product Baseline.

## Required Metadata

Each HTML Package SHOULD declare:

- Package identifier;
- Knowledge Product type;
- product name;
- Package version;
- Source Baseline identifier;
- Production Recipe identifier and version;
- Manufacturing Run identifier;
- validation status;
- publication status;
- generated timestamp;
- human review status; and
- known gaps.

## Manifest Requirements

The Package manifest SHOULD include:

```yaml
package_id: "gia-user-manual-html-YYYYMMDD-NNN"
product_type: "User Manual | Training Guide"
product_name: "GIA / Soleat"
source_baseline_id: "gia-baseline-YYYYMMDD-NNN"
manufacturing_run_id: "gia-run-YYYYMMDD-NNN"
recipe_id: "user-manual | training-guide"
recipe_version: "<version>"
validation_status: "pass | pass-with-waiver | fail | draft"
publication_status: "draft | publication-ready | published"
entry_point: "index.html"
sections: []
assets: []
known_gaps: []
waivers: []
```

## Navigation Requirements

Each HTML Package SHOULD provide:

- landing or index page;
- table of contents;
- previous and next navigation where sequential learning applies;
- section-level anchors;
- glossary access where glossary terms exist;
- link to source baseline note;
- link to validation summary; and
- link to support or escalation information where applicable.

## Traceability Requirements

An HTML Package SHOULD preserve traceability without overwhelming the ordinary reader.

Traceability MAY be exposed through:

- source baseline note;
- validation summary;
- section metadata;
- footnote-style evidence references;
- manifest records;
- separate evidence appendix; or
- internal machine-readable metadata.

A user-facing HTML page MAY hide low-level evidence detail, but the Package SHOULD retain evidence traceability in the manifest or supporting files.

## Asset Requirements

If screenshots, icons, diagrams, or videos are referenced, the Package SHOULD record:

- asset identifier;
- file path or URL;
- related Knowledge Object;
- source or generation status;
- alt text requirement;
- missing asset status; and
- validation status.

Missing but recommended assets SHOULD appear in the asset gap list.

## Validation Summary Requirements

The validation summary SHOULD include:

- Quality Gates applied;
- pass/fail/warning status;
- Waivers;
- unresolved ambiguity;
- missing required ingredients;
- source-grounding warnings;
- broken links;
- asset gaps;
- human review status; and
- publication readiness recommendation.

## Accessibility Expectations

A GIA HTML Package SHOULD support basic accessibility expectations, including:

- semantic headings;
- readable navigation;
- meaningful link text;
- alt text for informative images;
- sufficient keyboard navigation assumptions;
- clear page titles; and
- no reliance on colour alone for meaning.

## Publication Readiness

A GIA HTML Package is publication-ready only when:

- required sections exist or omissions are justified;
- manifest exists;
- Source Baseline reference exists;
- validation summary exists;
- required Quality Gates pass or Waivers are recorded;
- broken critical links are resolved or waived;
- asset gaps are recorded;
- human review status is recorded; and
- publication channel assumptions are explicit.

## Boundary

This contract SHALL NOT require generated HTML output to be stored in KMRM.

Generated GIA HTML output SHOULD be stored in the Document Factory implementation repository, an output repository, or a publication channel selected by the implementation.
