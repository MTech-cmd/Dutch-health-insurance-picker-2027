# Dutch-health-insurance-picker-2027

**An evidence-based Dutch health insurance research, comparison and decision-support application.**

[![Version](https://img.shields.io/badge/version-0.1-blue)]()
[![Status](https://img.shields.io/badge/status-foundation-orange)]()
[![Insurance year](https://img.shields.io/badge/insurance%20year-2027-green)]()

---

## What is this project?

Dutch Healing Insurance Picker 2027 is an independent project designed to help people understand, research and compare Dutch health insurance options for the 2027 insurance year.

Traditional health insurance comparisons often focus heavily on monthly premiums, deductibles and general coverage.

This project aims to provide a broader picture.

It investigates not only what an insurance policy promises, but also how accessible healthcare is in practice and how responsibly the organisations behind insurance products operate.

The application combines three dimensions:

1. **Healthcare suitability:** How well does an insurance option accommodate different healthcare needs?
2. **Consumer suitability:** What are the practical conditions, services and restrictions associated with the provider and policy?
3. **Corporate responsibility:** How does the insurance group perform in areas such as climate, human rights, labour practices and transparency?

The result should be an understandable, evidence-backed comparison system that supports independent decision-making.

**The application informs decisions. It does not make decisions on behalf of its users.**

---

## Why does this project exist?

Healthcare insurance is a complex combination of legislation, contractual conditions, commercial structures and practical healthcare accessibility.

A policy may technically cover a treatment while practical access remains limited by:

- Contracted healthcare providers.
- Regional availability.
- Referral requirements.
- Waiting times.
- Reimbursement restrictions.
- Financial conditions.

Similarly, two providers belonging to the same insurance group may offer different consumer experiences and insurance products.

A useful comparison therefore needs to distinguish between corporate ownership, customer-facing providers and individual insurance contracts.

The project also recognises that corporate responsibility matters independently of consumer suitability.

These dimensions should be visible without being confused with one another.

---

## Core architecture

The insurance database uses three primary entities.

### 1. Insurance groups

Represent the corporate organisations behind insurance providers.

Research areas include:

- Ownership and corporate structure.
- Climate and environmental responsibility.
- Investments.
- Human rights.
- LGBTQIA+ inclusion.
- Labour practices.
- Governance and transparency.

### 2. Insurance providers

Represent customer-facing insurance providers and brands.

Research areas include:

- Customer service.
- Healthcare accessibility.
- Regional provider availability.
- Contracted healthcare networks.
- Consumer experience.
- Financial accessibility.

### 3. Individual policies

Represent specific insurance contracts for a particular insurance year.

Research areas include:

- Monthly premium.
- Deductible.
- Healthcare coverage.
- Reimbursement conditions.
- Contracted and non-contracted care.
- Exclusions.
- Referral requirements.

The relationship is:

```text
Insurance Group
      |
      v
Insurance Provider
      |
      v
Individual Policy
```

One group can have multiple providers, and one provider can offer multiple policies.

Corporate assessments must not be duplicated across providers. Policy conditions must be researched individually.

---

## Evidence-based research

Assessments must be traceable to supporting information.

The evidence architecture introduces two additional data entities:

- **Claims:** Individual research findings about an insurance group, provider or policy.
- **Sources:** Documents, publications and other references supporting those claims.

Research should record:

- Source title and publisher.
- Direct URL.
- Publication date.
- Verification date.
- Applicable entity.
- Evidence summary.
- Limitations.
- Confidence.
- Conflicting information.

Unknown information must remain unknown.

An absent source is not evidence of poor performance, just as a corporate promise is not proof of successful implementation.

---

## Four-entity project governance

The project operates through four distinct entities.

| Entity | Responsibility |
|---|---|
| Operator | Project authority, decisions and approval |
| Research (Res) | Evidence, investigation and methodology |
| Development (Dev) | Architecture, software and testing |
| Maintainer | Coordination, continuity and project-state management |

### Operator

Defines what matters, sets priorities, approves requirements and makes final decisions.

The Operator is also expected to develop an increasingly independent understanding of insurance, research methodology and technical decisions.

### Research

Establishes what can be substantiated and communicates uncertainty.

### Development

Turns approved requirements and verified research structures into functioning software.

### Maintainer

Maintains an accurate picture of the entire project, including the status of every entity, outstanding work, dependencies and decisions.

Maintainer coordinates but does not override Operator.

---

## Project principles

1. Evidence before conclusions.
2. Transparency over unexplained scores.
3. Unknown values remain unknown.
4. Corporate, provider and policy assessments remain separate.
5. Consumer suitability and institutional responsibility remain independently visible.
6. Users retain control over their priorities.
7. Important decisions remain under Operator authority.
8. Every significant change is documented.
9. All entities improve through feedback and self-learning.
10. Automated assessments never replace human judgement.

---

## Initial research scope

The first research round covers five representative group/provider pairs.

| Insurance group | Representative provider |
|---|---|
| Achmea | Zilveren Kruis |
| VGZ | VGZ |
| CZ | CZ |
| Menzis | Menzis |
| DSW | DSW |

These are starting subjects, not an exhaustive list of the Dutch insurance market.

Ownership, legal insurer identities and provider relationships require verification.

The target insurance year is 2027.

---

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

---

## Project governance

The project is maintained through four canonical documents:

- `PROJECT.md` — Public project definition and shared source of truth.
- `DEVELOPMENT.md` — Development responsibilities and technical requirements.
- `RESEARCH.md` — Research responsibilities and evidence methodology.
- `MAINTAINER.md` — Project coordination and status management.

These documents must remain consistent.

---

## Relationship with Viewscape One

Dutch Healing Insurance Picker 2027 is an independent product.

Viewscape One is a separate, larger AI-web framework project.

The Picker may eventually use Viewscape One as an underlying technical framework, but this is a possible future integration, not a current dependency or part of the project's identity.

The Picker must maintain its own objectives, governance, data architecture and documentation.

---

## Current status

**Version:** 0.1  
**Status:** Initial foundation  
**Implementation:** Not yet established  
**Research verification:** Outstanding  
**Architecture:** Initial specification documented

Version 0.1 establishes the operating model, initial insurance data architecture, research direction and development requirements.

It does not claim that a functional application or verified insurance database already exists.

---

## Intended outcome

The long-term goal is to create an accessible, transparent and evidence-based tool through which people can understand Dutch health insurance options in greater depth.

It should make complex information easier to navigate while preserving the user's ability to inspect evidence, challenge assumptions and reach independent conclusions.

**Better information. Greater understanding. Independent decisions.**