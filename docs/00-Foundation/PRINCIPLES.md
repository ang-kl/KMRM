# Principles

KMRM is governed by the following principles. These principles guide all future reference model documents, examples, and implementations.

## 1. Specification First

KMRM SHALL define the reference model before defining any implementation.

The model SHALL describe what a conforming knowledge manufacturing system must preserve, represent, validate, and produce. It SHALL NOT depend on one runtime, AI model, product repository, or vendor platform.

## 2. Implementation Independence

KMRM SHALL remain independent of programming languages, databases, AI models, orchestration frameworks, hosting platforms, and user interfaces.

An implementation MAY use AI systems, graph databases, file systems, relational databases, or other technologies, provided the implementation preserves the required semantics.

## 3. Source Grounding

A Knowledge Product SHOULD be grounded in identifiable Knowledge Sources and Evidence.

A conforming implementation SHALL distinguish between source-grounded content, inferred content, generated phrasing, and unresolved ambiguity.

## 4. Provenance Preservation

A Manufacturing Pipeline SHALL preserve provenance from source intake through publication.

A pipeline SHALL NOT discard provenance merely because knowledge has been transformed, summarised, assembled, or repackaged.

## 5. Object First

KMRM treats the Knowledge Object as the primary unit of structured knowledge.

Knowledge Graphs, Products, Recipes, Pipelines, and Publications are built from, operate on, or refer back to Knowledge Objects.

## 6. Relationships Are Explicit

A Relationship between Knowledge Objects SHALL be represented explicitly.

A conforming implementation SHOULD avoid hidden, implicit, or unverifiable relationships when those relationships are used for manufacturing or validation.

## 7. Recipes Over Prompts

A Production Recipe SHALL define the required ingredients, transformation steps, Quality Gates, and output expectations for a Knowledge Product.

Prompts MAY be used by an implementation, but prompts SHALL NOT replace the recipe definition.

## 8. Quality Gates Before Publication

A Knowledge Product SHALL pass its required Quality Gates before it is treated as publishable.

Quality Gates SHOULD test source grounding, traceability, completeness, consistency, terminology, and format requirements.

## 9. Adapters Are Not the Model

Adapters MAY connect a conforming implementation to source systems such as GitHub repositories, document stores, wikis, or media libraries.

Adapter-specific behaviour SHALL NOT be treated as universal model behaviour.

## 10. Minimal Core, Extensible Specialisation

KMRM SHOULD maintain a small core of universal primitives.

Domain-specific concepts such as Feature, Screen, API, Lesson, Policy, or Sermon Note SHOULD be modelled as specialisations or profiles, not as required primitives.

## 11. Audience Is a Publishing Concern

KMRM MAY support audience-specific outputs, but audience segmentation SHALL NOT be the organising centre of the reference model.

Audience needs MAY influence Product Profiles, Packaging, and Publication. They SHALL NOT replace source grounding, object modelling, or manufacturing discipline.

## 12. Human Accountability

A conforming implementation MAY automate extraction, transformation, validation, and publishing. It SHOULD still support human review, override, and accountability where outputs affect users, operations, compliance, training, or decision-making.
