# Production Cell

## Purpose

A Production Cell is a specialised manufacturing capability that performs one or more Manufacturing Stages.

A Production Cell describes a bounded capability, not a job title, agent, department, or technology. A Production Cell MAY be implemented by a human, a software process, an AI system, a team, or a combination of these.

## Definition

A Production Cell SHALL have:

- a name;
- a purpose;
- declared inputs;
- declared outputs;
- operating boundaries;
- required Quality Gates or handoff checks;
- provenance obligations; and
- escalation or Waiver rules where applicable.

## Cell Boundary Principle

A Production Cell SHALL do only the work assigned to its boundary.

A Production Cell SHOULD NOT silently perform work belonging to another Production Cell unless the Manufacturing Pipeline explicitly permits combined execution.

This rule protects traceability and prevents hidden transformations.

## Required Cell Contract

A Production Cell contract SHOULD define:

| Field | Description |
|---|---|
| Cell Name | Stable name of the capability. |
| Purpose | Why the cell exists. |
| Inputs | What the cell may consume. |
| Outputs | What the cell must produce. |
| Boundaries | What the cell SHALL NOT do. |
| Preconditions | Required state before the cell may operate. |
| Postconditions | Required state after the cell operates. |
| Quality Gates | Validation checks owned or triggered by the cell. |
| Provenance Duties | What source or transformation records must be preserved. |
| Handoff Target | Next stage or cell in the Manufacturing Pipeline. |
| Waiver Rules | Conditions under which failure may be recorded and bypassed. |

## Standard Cell Families

KMRM defines the following standard cell families.

| Cell Family | Primary Purpose |
|---|---|
| Intake Cell | Declares source scope and Source Baseline. |
| Extraction Cell | Captures Evidence from Knowledge Sources. |
| Normalisation Cell | Converts extracted material into consistent structure. |
| Classification Cell | Assigns types, states, categories, and profiles. |
| Relationship Cell | Creates or verifies Relationships. |
| Planning Cell | Selects Recipes, outputs, and Quality Gates. |
| Assembly Cell | Manufactures draft Knowledge Products from Knowledge Objects. |
| Validation Cell | Applies Quality Gates and produces validation reports. |
| Packaging Cell | Prepares Products for specific formats or channels. |
| Publishing Cell | Releases Packages as Publications. |
| Maintenance Cell | Detects changes and identifies affected Products. |

An implementation MAY define additional cell families.

## Input and Output Discipline

A Production Cell SHALL declare whether each input is:

- source-grounded;
- inferred;
- generated;
- previously validated;
- manually supplied; or
- implementation-specific.

A Production Cell SHALL declare whether each output is:

- Evidence;
- Knowledge Object;
- Relationship;
- validation result;
- Knowledge Product;
- Package;
- Publication;
- Waiver; or
- other implementation-specific artefact.

## Handoff Rules

A handoff between Production Cells SHOULD include:

- output identifier;
- lifecycle state;
- provenance reference;
- validation status;
- unresolved ambiguity;
- failed or waived checks;
- next required stage; and
- responsible actor or system where known.

A receiving Production Cell SHOULD reject or quarantine inputs that lack required handoff information.

## Boundary Examples

### Extraction Cell

The Extraction Cell MAY identify Evidence in a Knowledge Source.

The Extraction Cell SHALL NOT decide final publication wording unless the Manufacturing Pipeline explicitly combines Extraction and Assembly.

### Assembly Cell

The Assembly Cell MAY combine validated Knowledge Objects into a draft Knowledge Product.

The Assembly Cell SHALL NOT invent unsupported source claims.

### Publishing Cell

The Publishing Cell MAY release a Package to a declared channel.

The Publishing Cell SHALL NOT publish a Product that has failed a required Quality Gate unless a Waiver has been explicitly recorded.

## Relationship to Permanent Agents

An implementation MAY assign a permanent agent, team, service, or role to operate a Production Cell.

KMRM does not prescribe the worker. It prescribes the cell contract, inputs, outputs, boundaries, and quality obligations.
