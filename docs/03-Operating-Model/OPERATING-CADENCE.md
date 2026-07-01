# Operating Cadence

## Purpose

Operating Cadence defines recurring review, planning, validation, and maintenance rhythms for a knowledge manufacturing implementation.

This model does not require a literal weekly meeting or human-only process. It defines the kinds of coordination events that keep Manufacturing Runs disciplined and traceable.

## Principle

A conforming implementation SHOULD make operating rhythm explicit when manufacturing is repeated, automated, or used for publishable outputs.

Operating Cadence SHOULD support:

- planning;
- work allocation;
- risk review;
- quality review;
- publication readiness;
- maintenance; and
- continuous improvement.

## Reference Cadence Events

| Event | Purpose | Typical Owner |
|---|---|---|
| Intake Review | Confirm source scope and Source Baseline. | Source Intake Worker |
| Manufacturing Planning | Select Products, Recipes, Workers, and Quality Gates. | Factory Orchestrator |
| Handoff Review | Confirm each Production Cell has required inputs. | Factory Orchestrator |
| Quality Review | Review validation results, defects, Waivers, and readiness. | Quality Validator |
| Publication Review | Confirm Package, manifest, version, and release preconditions. | Publisher |
| Maintenance Review | Detect source changes and affected Knowledge Products. | Maintenance Analyst |
| Performance Review | Review worker performance, defect patterns, and process improvements. | Human Accountable Owner or Factory Orchestrator |

## Weekly Factory Review Pattern

A Document Factory-like implementation MAY use a weekly review pattern.

```text
Factory Orchestrator
  ↓
Source Intake status
  ↓
Knowledge Object changes
  ↓
Recipe and Product status
  ↓
Quality Gate status
  ↓
Publication readiness
  ↓
Risks and Waivers
  ↓
Assignments and next Manufacturing Runs
```

The weekly pattern is OPTIONAL. The implementation MAY use daily, per-PR, per-release, or event-driven cadence instead.

## Event Records

A recurring operating event SHOULD produce a record when it affects manufacturing behaviour.

An event record MAY include:

- event type;
- date or run identifier;
- source baseline;
- affected Products;
- decisions made;
- open risks;
- assigned Worker Profiles;
- Quality Gate status;
- Waivers; and
- next actions.

## Cadence Boundaries

An operating event SHALL NOT by itself authorise:

- source invention;
- Quality Gate bypass;
- publication without readiness;
- source system modification; or
- unrecorded Recipe change.

Authority must be defined through Worker Profiles, Policies, Quality Gates, and Waivers.

## Automation

An implementation MAY automate operating cadence events.

Automated cadence SHOULD still produce reviewable records when it triggers Manufacturing Runs, changes baselines, updates Products, or proposes Publications.

## Minimum Cadence for User Manual and Training Guide Manufacturing

For a User Manual and Training Guide production line, an implementation SHOULD define at least:

1. Source Baseline review;
2. Recipe readiness review;
3. Quality Gate review;
4. Publication readiness review; and
5. Maintenance impact review.
