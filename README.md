# Dutch Health Insurance Picker 2027

An independent, evidence-based project to help people understand and compare Dutch health insurance options for the 2027 insurance year.

> The application informs decisions. It does not make decisions on behalf of its users.

## Purpose

Dutch health insurance comparisons often focus on premiums, deductibles and headline coverage. This project aims to provide a broader picture by examining:

1. **Healthcare suitability** — how well an insurance option accommodates different healthcare needs.
2. **Consumer suitability** — the practical conditions, services and restrictions associated with providers and policies.
3. **Corporate responsibility** — how the organisations behind insurance products perform in areas such as climate, human rights, labour practices and transparency.

These dimensions are presented separately so that users can inspect the evidence and apply their own priorities.

## Data model

The core insurance database distinguishes three levels:

- **Insurance groups** — the corporate organisations behind insurance providers.
- **Insurance providers** — customer-facing insurers and brands.
- **Individual policies** — specific insurance contracts for an insurance year.

The relationship is:

Insurance Group
       |
       v
Insurance Provider
       |
       v
Individual Policy

One group may have multiple providers, and one provider may offer multiple policies. Group-level assessments must not be duplicated as provider assessments, and policy conditions must be researched individually.

Two supporting entities make the evidence traceable:

- **Claims** — individual research findings associated with a group, provider or policy.
- **Sources** — documents, publications and references supporting claims.

Research records should include source details, publication and verification dates, evidence summaries, limitations, confidence and conflicting information. Unknown information remains unknown; missing evidence is not itself proof of poor performance.

## Initial research scope

The first research round covers five representative group/provider pairs:

| Insurance group | Representative provider |
|---|---|
| Achmea | Zilveren Kruis |
| VGZ | VGZ |
| CZ | CZ |
| Menzis | Menzis |
| DSW | DSW |

These are initial research subjects, not an exhaustive list of the Dutch insurance market. Ownership, legal insurer identities, provider relationships and 2027 policy details require verification.

## Project principles

1. Evidence before conclusions.
2. Transparency over unexplained scores.
3. Unknown values remain unknown.
4. Corporate, provider and policy assessments remain separate.
5. Consumer suitability and institutional responsibility remain independently visible.
6. Users retain control over their priorities.
7. Important decisions remain under Operator authority.
8. Significant changes are documented.
9. Research and implementation improve through feedback.
10. Automated assessments never replace human judgement.

## Governance

The project operates through four entities:

| Entity | Responsibility |
|---|---|
| Operator | Project authority, priorities, decisions and approval |
| Research (Res) | Investigation, evidence and methodology |
| Development (Dev) | Architecture, software and testing |
| Maintainer | Coordination, project-state tracking and continuity |

Maintainer coordinates but does not override Operator. Research establishes what can be substantiated. Development implements approved requirements. Operator retains final authority over project decisions and milestone progression.

## Canonical documentation

The project is governed through four canonical documents:

- `PROJECT.md` — public project definition and shared source of truth.
- `DEVELOPMENT.md` — development responsibilities and technical requirements.
- `RESEARCH.md` — research responsibilities and evidence methodology.
- `MAINTAINER.md` — project coordination and status management.

These documents should remain consistent. Significant decisions, changes, dependencies and handovers should be documented.

## Development roadmap

| Version | Objective |
|---|---|
| V0.1 | Project foundation and governance |
| V0.2 | Database management and validation |
| V0.3 | Research and evidence infrastructure |
| V0.4 | Assessment and scoring |
| V0.5 | User questionnaire |
| V0.6 | Recommendation engine |
| V0.7 | Comparison interface |
| V0.8 | Evidence-backed reports |
| V0.9 | Validation and refinement |
| V1.0 | Public-ready application |

The roadmap is provisional. Each milestone requires defined acceptance criteria and Operator approval.

## Current status

**Version:** 0.1  
**Status:** Initial foundation  
**Repository:** Created; canonical project documents present  
**Research:** Initialised; investigations and verification outstanding  
**Development:** Initialised; implementation not started  
**Architecture:** Initial specification documented; technical implementation and approval outstanding

Initialisation does not mean implementation is complete. No functional application or verified insurance database is claimed at this stage.

## Relationship with Viewscape One

Dutch Health Insurance Picker 2027 is an independent project. Viewscape One is a separate AI-web framework. A possible future integration may be considered as a separate technical decision; it is not a current dependency or part of this project's identity.

## Intended outcome

The long-term goal is an accessible, transparent and evidence-based tool that helps people understand Dutch health insurance options, inspect supporting evidence, challenge assumptions and make independent decisions.

**Better information. Greater understanding. Independent decisions.**