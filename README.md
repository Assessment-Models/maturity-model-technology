# Technology Maturity Model

**Assessing the fitness, sustainability and organizational readiness of the technology estate.**

The Technology Maturity Model provides a structured view of how an organization selects, governs, maintains and evolves the technologies on which its products, services and operations depend.

Technology maturity is broader than the operation of infrastructure or the adoption of new tools. It concerns whether the technology estate remains fit for current and future needs, whether technical debt and lifecycle exposure are understood, whether critical skills are available, and whether platforms and tooling enable teams to use technology consistently and effectively.

The repository currently provides a stable five-level maturity scale and an initial **draft** criteria register. The register is a seed for the complete assessment instrument; it should not yet be treated as a fully specified, weighted assessment.

---

## Find your starting point

| If you are a... | Start with |
|---|---|
| CTO, CIO or technology executive | [What the model assesses](#what-the-model-assesses) and [Maturity progression](#maturity-progression) |
| Enterprise or technology architect | [The five assessment dimensions](#the-five-assessment-dimensions) |
| Platform, infrastructure or engineering leader | [Platform and tooling capability](#the-five-assessment-dimensions) |
| Technology portfolio or risk leader | [Technical debt and lifecycle management](#the-five-assessment-dimensions) |
| Engineering manager or capability leader | [Skill coverage](#the-five-assessment-dimensions) |
| Assessor or model contributor | [Current assessment assets](#current-assessment-assets) and [Governance](#governance-and-contribution) |

## What the model assesses

The model is concerned with the fitness and sustainability of the technology estate as an organizational asset. It is intended to help answer questions such as:

- Are technology choices appropriate for current workloads and anticipated future needs?
- Are selection standards and technology patterns visible and consistently applied?
- Is technical debt identified, risk-ranked and addressed through funded remediation?
- Are technology versions supported, and are end-of-life risks managed ahead of vendor deadlines?
- Does the organization have sufficient skills and enablement to operate and evolve its technology estate?
- Are platform capabilities and engineering tools available to support reliable, repeatable technology delivery?

The model complements broader enterprise assessments. It focuses on technology capability and the health of the technology estate, not the overall maturity of enterprise operations, service delivery or digital transformation.

## The five assessment dimensions

The current seed criteria register organizes technology maturity into five dimensions and ten subdimensions. It currently contains 11 criterion statements.

| ID | Dimension | Scope |
|---|---|---|
| **D1** | Stack Fitness | Technology fitness against current and future workload needs; selection standards and golden paths |
| **D2** | Technical Debt | Visibility, risk ranking, funding and remediation of accumulated technical debt |
| **D3** | Lifecycle Management | Supported-version currency, end-of-life planning, patching and upgrade cadence |
| **D4** | Skill Coverage | Technology skills, skill gaps, team enablement and adoption support |
| **D5** | Platform & Tooling Capability | Shared observability, CI/CD and provisioning automation capabilities |

These dimensions provide the initial coverage structure. The current register is deliberately marked draft: its criteria are seed propositions and do not yet provide the complete definitions, assessment questions, level-specific anchors, evidence requirements, applicability rules and weighting needed for a fully operational instrument.

## Maturity progression

The model uses five capability maturity levels, with a separate L-0 Not Assessed state. L-0 is not a capability level and must not be interpreted as a finding that technology capability is absent.

| Level | Name | Canonical score range | Interpretation |
|---|---|---:|---|
| L-0 | Not Assessed | Not a maturity band | No criterion evidence has been assessed |
| L-1 | Emergent | 0–20 | Technology choices are largely decentralized, informal and person-dependent |
| L-2 | Structured | 21–45 | Inventories, standards and basic lifecycle practices exist but are inconsistently applied |
| L-3 | Systematic | 46–70 | Technology is actively governed, maintained and managed through defined practices |
| L-4 | Adaptive | 71–88 | Technology decisions respond to measured performance, risk, value and changing needs |
| L-5 | Self-Optimising | 89–100 | Technology is continuously evolved as a strategic asset, with sustained improvement |

The canonical band definitions and effort multipliers are maintained in [maturity/scale.yaml](maturity/scale.yaml). The five maturity bands are:

| Band | Score range | Effort multiplier |
|---|---:|---:|
| Emergent | 0–20 | 1.0× |
| Structured | 21–45 | 1.5× |
| Systematic | 46–70 | 2.5× |
| Adaptive | 71–88 | 4.0× |
| Self-Optimising | 89–100 | 6.0× |

The scale defines the progression semantics. The current seed criteria register does not yet define a complete criterion-level scoring and aggregation method; the canonical band ranges should not be mistaken for a complete assessment calculation specification.

## Current assessment assets

The repository's current maturity assets have different levels of completion:

| Asset | Current state | Use |
|---|---|---|
| [Maturity scale](maturity/scale.yaml) | Stable | Defines L-0 Not Assessed and the five capability levels, characteristics and evidence expectations |
| [Technology model register](maturity/model/technology.yaml) | Stable | Defines model identity, scale relationship and provenance |
| [Seed criteria register](maturity/model/technology-register-draft.yaml) | Draft | Provides initial five-dimension, ten-subdimension criterion coverage |
| [Worked example](examples/technology-2026.yaml) | Illustrative | Demonstrates a sample 0–100 score, canonical band resolution and effort-adjusted value; it is not a complete criterion-level assessment record |
| [Model manifest](model.yaml) | Current repository identity | Declares model identity, version, dependencies and contract relationship |

A full questionnaire, criterion-level evidence schema and normative evaluation profile are not yet present. The next substantive model-development work is to complete and validate the criteria, define the assessment questions and evidence expectations, establish the scoring and aggregation method, and provide worked assessment records that exercise those rules.

## Relationship to other assessment models

Technology maturity is one part of the broader enterprise capability landscape. The model should be used alongside specialist assessments without duplicating their ownership.

| Assessment concern | Relevant model | Boundary |
|---|---|---|
| Enterprise operations and the effective use of technology in day-to-day operations | [Operations Maturity Model](https://github.com/Assessment-Models/maturity-model-operations) | Technology assesses the capability and fitness of the technology estate; Operations assesses how technology is used to operate the enterprise |
| Closed-loop autonomous operations and agent governance | [Autonomous Operations Maturity Model](https://github.com/Assessment-Models/maturity-model-autonomous-operations) | Technology provides evidence about platform and tooling capabilities; Autonomous Operations assesses governed autonomous execution |
| Customer-facing delivery flow and outcomes | [Services Delivery Maturity Model](https://github.com/Assessment-Models/maturity-model-services-delivery) | Technology assesses enabling technology capability; Services Delivery assesses delivery performance and customer outcomes |
| Enterprise-wide digital transformation | [Digital Transformation Maturity Model](https://github.com/Assessment-Models/maturity-model-digital-transformation) | Technology assesses the technology estate; Digital Transformation assesses the broader transformation of the business and operating model |
| Architecture modernization need and practice | [Architecture Modernization Assessment](https://github.com/Assessment-Models/maturity-model-modernization) | Technology maturity can inform modernization decisions; AMAF assesses the modernization need of architecture subjects |

The model also declares a touchpoint with Operations for shared platform and tooling evidence. The intended principle is single ownership of each criterion, with relevant evidence reused by a peer model rather than assessed twice. See [touchpoints.yaml](touchpoints.yaml).

## Worked example

The [technology-2026 example](examples/technology-2026.yaml) is an illustrative score record. It demonstrates the canonical v2 band lookup and effort-adjusted value calculation for a sample aggregate score. It does not replace a completed criterion-level assessment or establish benchmark performance.

## How to use the model today

For exploratory use:

1. Review the [maturity scale](maturity/scale.yaml) to understand the five capability levels.
2. Use the five dimensions as an initial discovery structure for technology estate discussions.
3. Review the [seed criteria register](maturity/model/technology-register-draft.yaml) as a starting point for identifying relevant evidence and assessment propositions.
4. Treat any aggregate score derived from the illustrative example as a demonstration of band arithmetic only, not as an organizational maturity result.
5. Record gaps and proposed refinements for the model's criteria, questionnaire, evidence and evaluation design.

Do not use the seed register as a formally calibrated benchmark or compare its results with other organizations until the assessment instrument and evaluation rules have been completed and governed.

## Repository contents

| Resource | Purpose |
|---|---|
| [model.yaml](model.yaml) | Model identity, dependencies and contract declaration |
| [maturity/scale.yaml](maturity/scale.yaml) | Stable maturity scale and capability-level definitions |
| [maturity/model/technology.yaml](maturity/model/technology.yaml) | Stable model register |
| [maturity/model/technology-register-draft.yaml](maturity/model/technology-register-draft.yaml) | Draft criterion register |
| [examples/technology-2026.yaml](examples/technology-2026.yaml) | Illustrative scoring example |
| [touchpoints.yaml](touchpoints.yaml) | Declared relationship with Operations |
| [CHANGELOG.md](CHANGELOG.md) | Versioned model changes |
| [CONTRIBUTING.md](CONTRIBUTING.md) | Change-control and contribution rules |
| [scripts/local_validate.py](scripts/local_validate.py) | Local model validation |

## Governance and contribution

The Technology Maturity Model is maintained by the [Assessment-Models organisation](https://github.com/Assessment-Models). Changes to model identity, maturity definitions, dimensions, criteria, scoring or evidence semantics must follow the repository's change-control process.

Contributors should preserve the distinction between the stable maturity scale and the draft criteria register. Criterion refinements should be accompanied by definitions, assessment questions, applicability rules, evidence expectations and observable level anchors. Scoring, aggregation and weighting should be specified and validated before the register is promoted to a stable assessment instrument.

See [CONTRIBUTING.md](CONTRIBUTING.md) and [CHANGELOG.md](CHANGELOG.md).

## Status

**Repository maturity-model release: 2.0.0** · **Criteria register:** draft · **Maturity scale:** stable

The repository has adopted the L-0 Not Assessed plus L-1…L-5 numbering convention. The seed criteria register remains a draft model extension and is not yet a complete assessment instrument.

## Licence

MIT. See [LICENSE](LICENSE).
