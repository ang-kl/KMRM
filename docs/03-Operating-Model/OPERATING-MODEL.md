# Operating Model

## Purpose

The Operating Model defines how a conforming implementation may assign stable responsibilities, worker profiles, skills, boundaries, and governance to the Production Cells defined by KMRM.

The Operating Model does not prescribe one organisation, one AI agent framework, one runtime, or one vendor. It defines how responsibilities should be bounded so that knowledge manufacturing remains traceable, reviewable, and safe to automate.

## Relationship to the Manufacturing Model

The Operating Model SHALL conform to the Manufacturing Model.

```text
KMRM Manufacturing Model
        ↓ defines work boundaries
Production Cells
        ↓ may be operated by
Worker Profiles
        ↓ may be implemented as
Humans, AI agents, services, teams, or hybrid systems
```

A worker SHALL NOT define the manufacturing process. The Manufacturing Model defines the process; workers operate within it.

## Operating Principles

A conforming implementation SHOULD observe the following principles:

1. assign workers to Production Cells rather than unbounded tasks;
2. define explicit worker skills and limits;
3. prevent workers from silently crossing cell boundaries;
4. preserve provenance and traceability across handoffs;
5. require Quality Gates before Packaging and Publishing;
6. distinguish source-grounded knowledge from generated phrasing;
7. record Waivers rather than hiding failed checks; and
8. keep human accountability where risk is material.

## Worker Profile

A Worker Profile describes a stable capability assigned to one or more Production Cells.

A Worker Profile SHALL define:

- profile name;
- purpose;
- assigned Production Cell or Cells;
- required skills;
- permitted inputs;
- permitted outputs;
- operating boundaries;
- escalation triggers;
- Quality Gate duties;
- provenance duties; and
- prohibited actions.

A Worker Profile MAY be implemented by:

- a human role;
- an AI agent;
- an automated service;
- a script;
- a team;
- a review board; or
- a hybrid arrangement.

## Permanent Worker Profiles

A permanent worker profile is a reusable Worker Profile that remains part of an implementation across many Manufacturing Runs.

Permanent worker profiles SHOULD be stable enough to support repeated production and review.

A permanent worker profile SHALL NOT be granted unbounded authority merely because it persists across runs.

## Standard Operating Roles

A conforming implementation MAY define the following standard Worker Profiles:

| Worker Profile | Primary Cell Alignment |
|---|---|
| Factory Orchestrator | Planning, scheduling, handoff control |
| Source Intake Worker | Intake Cell |
| Evidence Extractor | Extraction Cell |
| Object Normaliser | Normalisation Cell |
| Object Classifier | Classification Cell |
| Relationship Mapper | Relationship Cell |
| Recipe Planner | Planning Cell |
| Product Assembler | Assembly Cell |
| Quality Validator | Validation Cell |
| Package Builder | Packaging Cell |
| Publisher | Publishing Cell |
| Maintenance Analyst | Maintenance Cell |

An implementation MAY rename these profiles, provided their responsibilities remain bounded and traceable.

## Authority Boundaries

Worker Profiles SHOULD operate with least necessary authority.

A Worker Profile SHALL NOT:

- invent unsupported source claims;
- erase provenance;
- mark failed required Quality Gates as passed;
- publish without required Publication criteria;
- alter source systems outside its declared scope;
- redefine a Production Recipe during a Manufacturing Run without recording the change; or
- bypass required human review where governance requires it.

## Handoff Discipline

Worker Profiles SHOULD hand off structured outputs, not loose conversation.

A handoff SHOULD include:

- item identifier;
- lifecycle state;
- source grounding status;
- provenance reference;
- validation status;
- unresolved ambiguity;
- failed or waived gates; and
- next required cell.

## Human Review

An implementation SHOULD require human review when outputs affect:

- public-facing documentation;
- training materials;
- compliance;
- operational procedures;
- legal or financial decisions;
- user safety;
- reputation; or
- source systems.

KMRM does not prescribe the human reviewer. Implementations define reviewer identity and authority.

## AI Implementation Note

AI agents MAY operate Worker Profiles. When they do, the implementation SHOULD define:

- model or system identity;
- allowed tools;
- memory scope;
- source access scope;
- output format;
- escalation behaviour;
- retry limits;
- logging expectations; and
- review requirements.

These are implementation concerns and SHALL NOT be required by the KMRM reference model itself.
