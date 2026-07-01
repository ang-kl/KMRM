# Contractor Workers

## Purpose

Contractor Workers are temporary Worker Profiles used for specialised, bounded work within a knowledge manufacturing implementation.

They may represent human contractors, specialist AI agents, external services, temporary scripts, reviewers, translators, designers, or subject-matter experts.

## Principle

A Contractor Worker SHALL have a defined scope, boundary, review requirement, and exit condition.

Contractor Workers SHALL NOT become permanent authorities unless converted into Permanent Workers through an explicit Worker Profile decision.

## When to Use Contractor Workers

A conforming implementation MAY use Contractor Workers for:

- translation;
- legal review;
- compliance review;
- accessibility review;
- subject-matter validation;
- visual design;
- media production;
- specialised technical review;
- security review;
- localisation;
- temporary publication support; or
- one-off migration work.

## Required Contractor Profile

A Contractor Worker SHALL define:

- contractor identifier;
- purpose;
- permitted Production Cell or work area;
- permitted inputs;
- permitted outputs;
- required Skills;
- prohibited actions;
- review requirement;
- expiry condition;
- responsible sponsor; and
- required handoff artefacts.

## Authority

A Contractor Worker SHOULD have the minimum authority needed to complete the assigned work.

A Contractor Worker SHALL NOT publish, waive Quality Gates, alter source systems, change Production Recipes, or redefine Worker Profiles unless explicitly authorised.

## Handoff Requirements

A Contractor Worker SHOULD produce a handoff record when work affects Knowledge Objects, Knowledge Products, Quality Gates, Packages, or Publications.

A handoff record MAY include:

- work completed;
- inputs used;
- outputs produced;
- assumptions;
- unresolved issues;
- risks;
- evidence references;
- review requirements; and
- recommended next action.

## Review

Contractor Worker output SHOULD be reviewed by a Permanent Worker or Human Accountable Owner before it is used in a publishable Knowledge Product.

If contractor work is specialised and high-risk, review SHOULD include an appropriately qualified reviewer.

## Memory and Retention

Contractor Workers SHOULD receive only the memory and source access required for their limited purpose.

Temporary memory, credentials, or working notes SHOULD be retired, archived, or revoked when the Contractor Worker exits.

## Exit Condition

A Contractor Worker SHALL have an exit condition.

Examples include:

- deliverable accepted;
- review completed;
- time period ended;
- scope cancelled;
- risk threshold exceeded;
- replacement by Permanent Worker; or
- implementation decision to terminate access.

## Boundary Violations

A Contractor Worker boundary violation SHOULD trigger review.

Examples include:

- using unauthorised sources;
- creating unsupported claims;
- altering recipe logic;
- publishing without authority;
- retaining memory outside scope;
- bypassing review; or
- modifying source systems without permission.
