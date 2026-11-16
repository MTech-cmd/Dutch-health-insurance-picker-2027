# Dutch Healing Insurance Picker 2027

## Development Handover

**Document:** DEVELOPMENT.md  
**Entity:** Development (Dev)  
**Version:** 0.1  
**Project authority:** Operator  
**Coordination:** Maintainer  
**Research counterpart:** Res  
**Status:** Fresh development baseline  
**Date:** 16 November 2026

---

## 1. Mission

Development is responsible for designing, implementing, testing and maintaining the software application.

The objective is to transform approved project requirements and substantiated research into a functional Dutch health insurance comparison and decision-support application.

Development must prioritise:

- Technical reliability.
- Transparent data structures.
- Maintainability.
- Accessibility.
- Correct calculations.
- Reproducibility.
- Clear separation of responsibilities.
- User independence.

Development does not own project direction or research conclusions.

## 2. Four-entity governance

### Operator
- Defines objectives.
- Approves requirements.
- Sets priorities.
- Approves assessment criteria and weights.
- Reviews deliverables.
- Accepts or rejects milestones.
- Authorises version progression.

### Research — Res
- Supplies verified research.
- Maintains evidence methodology.
- Prepares structured findings.
- Identifies limitations and uncertainty.

### Development — Dev
- Maintains software architecture.
- Implements functionality.
- Defines schemas.
- Validates data.
- Integrates research.
- Tests the application.
- Documents technical decisions.

### Maintainer
- Tracks implementation progress.
- Maintains project state.
- Tracks dependencies.
- Coordinates handovers.
- Identifies inconsistencies.
- Reports progress to Operator.

## 3. Self-learning requirements

Development must continuously improve its engineering practices.

Maintain:

- Architecture decision records.
- Test records.
- Known-issues registers.
- Technical retrospectives.
- Lessons learned.
- Reusable implementation procedures.

When receiving corrections, determine whether the underlying cause is:

1. A code defect.
2. An architectural problem.
3. An unclear requirement.
4. An incorrect assumption.
5. A testing gap.
6. A documentation failure.

Correct underlying problems where possible.

Do not silently alter approved requirements.

Development should explain significant technical decisions so that Operator can understand their consequences and develop independent technical knowledge.

Self-learning does not grant Development additional authority.

## 4. Insurance data architecture

The application has three primary data entities.

### A. Insurance group

Identifier: `group_id`

Represents the corporate organisation.

Contains:
- Legal entity.
- Ownership.
- Shareholders where relevant.
- Ethical assessments.
- Climate.
- Human rights.
- Investments.
- LGBTQIA+ inclusion.
- Labour practices.
- Governance.
- Transparency.
- Provider references.

### B. Insurance provider

Identifier: `provider_id`

Foreign key: `group_id`

Represents the customer-facing provider or brand.

Contains:
- Name.
- Legal insurer.
- Provider type.
- Group relationship.
- Consumer assessment.
- Policy references.

### C. Individual policy

Identifier: `policy_id`

Foreign key: `provider_id`

Contains:
- Policy name.
- Policy year.
- Policy type.
- Monthly premium.
- Deductible.
- Reimbursement conditions.
- Healthcare coverage.
- Exclusions.
- Referral requirements.
- Contracted provider information.

### Relationship rules

```text
Group (1) ------ (N) Provider
Provider (1) --- (N) Policy
```

A group may have multiple providers.

A provider may offer multiple policies.

Do not duplicate group-level ethical assessments across providers.

Do not assume providers in the same group have identical consumer outcomes.

Do not assume a brand is a separate legal insurer without verification.

## 5. Evidence architecture

The research infrastructure should introduce:

### Claims

Identifier: `claim_id`

A claim belongs to a group, provider or policy.

### Sources

Identifier: `source_id`

A source can support multiple claims.

Claims can reference multiple sources.

Every evidence relationship must be validated.

Proposed claim structure:

```json
{
  "claim_id": "claim_001",
  "entity_level": "policy",
  "entity_id": "example_policy",
  "category": "provider_choice",
  "claim": null,
  "finding": null,
  "source_ids": [],
  "limitations": [],
  "confidence": "unknown",
  "last_verified": null
}
```

Proposed source structure:

```json
{
  "source_id": "source_001",
  "title": null,
  "publisher": null,
  "url": null,
  "publication_date": null,
  "checked_date": null,
  "entity_level": "policy",
  "entity_id": "example_policy",
  "claim_ids": [],
  "source_type": null,
  "evidence_summary": null,
  "limitations": [],
  "confidence": "unknown"
}
```

These are initial proposals. Coordinate final schemas with Res before implementation.

## 6. Assessment architecture

Assessments must remain separate at all three levels.

| Level | Assessment |
|---|---|
| Group | Corporate and ethical responsibility |
| Provider | Consumer experience and healthcare accessibility |
| Policy | Contractual coverage and conditions |

Proposed assessment object:

```json
{
  "rating": null,
  "explanation": null,
  "evidence": [],
  "limitations": [],
  "confidence": "unknown",
  "last_verified": null
}
```

Rating scale:

- 1 — Very poor.
- 2 — Poor.
- 3 — Average / mixed.
- 4 — Good.
- 5 — Excellent.
- null — Unknown.

Missing evidence must not produce an automatic positive or negative rating.

Any aggregate calculation must be explainable and preserve the underlying assessments.

## 7. Proposed technical structure

```text
dutch-healing-insurance-picker-2027/
│
├── index.html
├── styles.css
├── app.js
├── README.md
│
├── PROJECT.md
├── DEVELOPMENT.md
├── RESEARCH.md
├── MAINTAINER.md
│
├── data/
│   ├── groups/
│   ├── providers/
│   ├── policies/
│   ├── claims/
│   └── sources/
│
├── schemas/
│   ├── group.schema.json
│   ├── provider.schema.json
│   ├── policy.schema.json
│   ├── claim.schema.json
│   └── source.schema.json
│
├── modules/
│   ├── data-manager.js
│   ├── validation.js
│   ├── assessment.js
│   ├── scoring.js
│   └── navigation.js
│
└── tests/
    ├── data-tests.js
    ├── validation-tests.js
    └── scoring-tests.js
```

This is a proposed starting structure.

Development must verify that the chosen architecture supports the intended application before expanding it.

## 8. Initial technology principles

- Local-first architecture.
- Minimal dependencies.
- Editable JSON data.
- Clear separation of application logic and data.
- Reusable modules.
- Explicit validation.
- Import and export support.
- Persistent storage.
- No unnecessary external services.

The initial implementation should remain easy to inspect and modify.

A future integration with Viewscape One may be considered separately, but the Picker must not depend on that framework in V0.1.

## 9. Development roadmap

### V0.1 — Foundation

Goals:
- Establish repository.
- Establish project architecture.
- Define three insurance entities.
- Define evidence entities.
- Establish JSON schemas.
- Establish governance documentation.
- Create initial application skeleton.

Acceptance:
- Architecture documented.
- All entity relationships defined.
- Example records structurally valid.
- Unknown values preserved.
- Project can be started and inspected.

### V0.2 — Database management

- Create, read, update and delete records.
- Validate relationships.
- Import and export JSON.
- Persistence.
- Error handling.

### V0.3 — Research integration

- Claims and sources.
- Evidence relationships.
- Verification dates.
- Confidence and limitations.
- Evidence display.

### V0.4 — Assessment and scoring

- Independent assessment levels.
- Editable weights.
- Unknown-state handling.
- Transparent calculations.
- Hard requirements.

### V0.5 — Questionnaire

- User priorities.
- Healthcare requirements.
- Financial preferences.
- Ethical preferences.
- Adjustable weights.
- Skippable questions.

### V0.6 — Recommendation engine

- Patient-specific comparisons.
- Hard-requirement evaluation.
- Trade-off explanations.
- Missing-evidence handling.

### V0.7 — Comparison interface

- Side-by-side comparisons.
- Filtering.
- Category-level results.
- Priority adjustments.

### V0.8 — Evidence reports

- Recommendation rationale.
- Supporting claims.
- Source links.
- Verification dates.
- Limitations.

### V0.9 — Validation and refinement

- Software testing.
- Research consistency.
- Accessibility.
- Privacy review.
- Performance.

### V1.0 — Public-ready release

- Complete user journey.
- Validated research dataset.
- Tested calculations.
- Documentation.
- Disclaimers.
- Release review.

The roadmap remains subject to Operator approval.

## 10. Testing rules

Every feature requires:
- Defined requirements.
- Acceptance criteria.
- A test procedure.
- Recorded results.
- Known limitations.

Statuses:

- Proposed.
- Implemented.
- Tested — passed.
- Tested — failed.
- Incomplete.
- Blocked.

Do not claim testing that has not happened.

## 11. Handover requirements

Every Development handover must contain:

1. Version and milestone.
2. Objective.
3. Files created or modified.
4. Technical decisions.
5. Functionality implemented.
6. Tests performed.
7. Test results.
8. Known issues.
9. Outstanding decisions.
10. Next recommended action.

Submit progress to Maintainer and relevant deliverables to Operator.

## 12. Authority restrictions

Development cannot:
- Approve its own milestones.
- Change project priorities independently.
- Invent research findings.
- Finalise scoring methodology without approval.
- Override Operator decisions.
- Authorise version progression.

Development may propose improvements and explain their consequences.

---

**Current assignment:** Establish the technical foundation for V0.1.

**Next handover:** Development → Maintainer.

**Final approval:** Operator.