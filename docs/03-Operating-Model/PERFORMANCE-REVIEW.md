# Performance Review

## Purpose

Performance Review defines how a conforming implementation may evaluate Worker Profiles, Skills, Production Cells, Recipes, and Manufacturing Pipelines.

Performance Review is intended to improve manufacturing quality, not to replace source grounding, provenance, or Quality Gates.

## Principle

Performance Review SHALL focus on observable manufacturing behaviour.

A review SHOULD consider:

- traceability quality;
- source-grounding accuracy;
- completeness;
- consistency;
- defect rate;
- rework rate;
- boundary compliance;
- escalation quality;
- timeliness; and
- publication readiness impact.

## Review Targets

A conforming implementation MAY review:

- Worker Profiles;
- Skills;
- Production Cells;
- Production Recipes;
- Manufacturing Pipelines;
- Quality Gates;
- Packages;
- Publications; and
- overall Manufacturing Runs.

## Worker Performance Metrics

Worker Profiles MAY be evaluated using metrics such as:

| Metric | Meaning |
|---|---|
| Source-Grounding Accuracy | Whether outputs remain supported by Evidence. |
| Provenance Completeness | Whether required provenance is preserved. |
| Boundary Compliance | Whether the worker stayed within permitted authority. |
| Escalation Quality | Whether ambiguity, conflict, or risk was raised appropriately. |
| Rework Rate | How often outputs required correction. |
| Quality Gate Pass Rate | Whether outputs passed required gates. |
| Defect Recurrence | Whether known defect patterns repeat. |
| Timeliness | Whether work completed within expected operating cadence. |

## Performance Evidence

Performance Review SHOULD use evidence such as:

- validation reports;
- Quality Gate results;
- Waiver records;
- defect logs;
- rework records;
- publication records;
- source baseline comparisons;
- review comments;
- user feedback; and
- audit trails.

## Improvement Actions

A Performance Review MAY result in:

- Worker Profile revision;
- Skill definition revision;
- Recipe revision;
- Quality Gate revision;
- policy clarification;
- additional human review;
- memory update;
- retraining or recalibration in implementation-specific systems; or
- retirement of a Worker Profile.

## Boundary

Performance Review SHALL NOT authorise a Worker Profile to bypass Quality Gates, invent source-grounded claims, alter Recipes without change control, or publish without required approval.

## AI Worker Review

If a Worker Profile is implemented as an AI agent, Performance Review SHOULD include:

- tool-use accuracy;
- source access discipline;
- hallucination or invention incidents;
- boundary violations;
- citation and evidence quality;
- prompt or configuration drift;
- memory contamination risk; and
- human override frequency.

These implementation-specific observations SHALL NOT redefine the KMRM Worker Profile. They MAY improve the implementation of that profile.

## Review Frequency

A conforming implementation SHOULD define when Performance Review occurs.

Review MAY be:

- per Manufacturing Run;
- per Publication;
- per release;
- weekly;
- monthly;
- after defects;
- after Waivers; or
- after major source changes.

## Minimum Review for Publication Systems

If an implementation publishes user-facing Knowledge Products, it SHOULD review at least:

1. source-grounding failures;
2. failed or waived Quality Gates;
3. publication defects;
4. recurring terminology errors;
5. unsupported claims; and
6. missing provenance.
