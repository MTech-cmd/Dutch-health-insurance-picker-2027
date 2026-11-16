# Dutch Healing Insurance Picker 2027

## Research Handover

**Document:** RESEARCH.md  
**Entity:** Research (Res)  
**Version:** 0.1  
**Project authority:** Operator  
**Coordination:** Maintainer  
**Development counterpart:** Dev  
**Status:** Initial research specification  
**Date:** 16 November 2026

---

## 1. Mission

Research establishes a reliable understanding of Dutch health insurance options for the 2027 insurance year.

Its objective is to investigate:

- Insurance groups.
- Insurance providers.
- Individual policies.
- Healthcare coverage.
- Practical healthcare accessibility.
- Consumer experience.
- Financial accessibility.
- Corporate responsibility.

Research must provide evidence, identify uncertainty and explain conflicting information.

It must help users understand their options rather than decide what they should choose.

## 2. Four-entity governance

### Operator
- Defines research priorities.
- Approves assessment criteria.
- Approves weights.
- Reviews findings.
- Makes final decisions.

### Research — Res
- Investigates.
- Collects evidence.
- Verifies claims.
- Maintains methodology.
- Documents uncertainty.
- Proposes assessments.
- Improves research procedures.

### Development — Dev
- Implements research structures.
- Maintains data schemas.
- Integrates evidence.
- Displays findings.

### Maintainer
- Tracks research progress.
- Coordinates handovers.
- Maintains project state.
- Tracks outstanding questions.
- Identifies inconsistencies.

Research does not have final decision-making authority.

## 3. Self-learning methodology

Research must continuously improve its own methodology.

Maintain:
- Research procedures.
- Source-quality criteria.
- Verification standards.
- Claim registers.
- Source registers.
- Research completeness reports.
- Historical corrections.
- Lessons learned.

When a claim is contradicted or outdated, revisit it and document the change.

Distinguish:

- Evidence from interpretation.
- Official policy from marketing.
- Legal entitlement from contractual entitlement.
- Contractual entitlement from practical accessibility.
- Corporate statements from independently verified performance.
- Allegations from documented findings.
- Unknown information from negative findings.

Self-learning must improve consistency and reliability without changing Operator authority.

## 4. Three research levels

### Level 1 — Insurance group

Research corporate and ethical responsibility.

Categories:
- Climate and environment.
- Investments.
- Human rights.
- LGBTQIA+ inclusion.
- Labour practices.
- Governance.
- Transparency.
- Political influence and lobbying.

Group-level assessments should be researched once and referenced by associated providers.

### Level 2 — Insurance provider

Research the customer-facing insurance provider or brand.

Categories:
- Customer service.
- Healthcare accessibility.
- Regional availability.
- Contracted provider network.
- Freedom of provider choice.
- Consumer experience.
- Financial accessibility.

Verify legal insurer identities, risk-bearing entities and commercial relationships.

Do not assume that every commercial brand is a separate legal insurer.

### Level 3 — Individual policy

Research the actual insurance contract for the relevant insurance year.

Categories:
- Premium.
- Deductible.
- Coverage.
- Reimbursements.
- Contracted healthcare.
- Non-contracted reimbursements.
- Exclusions.
- Referral requirements.
- Medication coverage.
- Policy conditions.

Every policy must be independently verified.

## 5. Initial research subjects

The first research assignment covers five representative group/provider pairs.

| Group | Provider | Group ID | Provider ID |
|---|---|---|---|
| Achmea | Zilveren Kruis | achmea | zilveren_kruis |
| VGZ | VGZ | vgz | vgz |
| CZ | CZ | cz | cz |
| Menzis | Menzis | menzis | menzis |
| DSW | DSW | dsw | dsw |

These are starting points, not an exhaustive representation of the Dutch market.

Verify:
- Legal entities.
- Ownership.
- Risk-bearing insurers.
- Brand relationships.
- Provider relationships.
- Available 2027 policies.

Do not treat the proposed relationships as verified until evidence supports them.

## 6. Healthcare research priorities

The primary research perspective is healthcare suitability.

Investigate:

1. Gender-affirming healthcare.
2. Hormone-related healthcare.
3. Mental healthcare and psychiatry.
4. Women's healthcare.
5. Disability-related healthcare.
6. Chronic illness and recurring treatment.
7. Freedom of provider choice.
8. Regional healthcare access.
9. Waiting times where reliable data exists.
10. Referral requirements.
11. Medication accessibility.
12. Financial accessibility.

### Three mandatory distinctions

**Legal entitlement**

What healthcare is covered under applicable Dutch law and regulation?

**Contractual entitlement**

What does the individual insurance policy actually promise?

**Practical accessibility**

Can the insured realistically obtain the care, considering provider availability, contracts, waiting times, referral requirements and other restrictions?

Coverage on paper does not automatically establish practical access.

## 7. Corporate responsibility research

The Institution View investigates:

- Climate commitments and actual progress.
- Investments.
- Human rights.
- LGBTQIA+ inclusion.
- Labour practices.
- Governance.
- Transparency.
- Political influence and lobbying.

Distinguish official corporate statements, independently verified performance, documented incidents, allegations and third-party assessments.

Do not present allegations as established facts.

## 8. Evidence methodology

Every meaningful assessment must be traceable.

### Claim records

Each claim should include:

- Claim ID.
- Entity level.
- Entity ID.
- Category.
- Claim description.
- Finding.
- Source IDs.
- Limitations.
- Confidence.
- Verification date.

### Source records

Each source should include:

- Source ID.
- Title.
- Publisher.
- Direct URL.
- Publication date.
- Date checked.
- Applicable entity.
- Source type.
- Evidence summary.
- Limitations.
- Confidence.

### Evidence status

| Status | Meaning |
|---|---|
| Supported | Evidence supports the finding |
| Partly supported | Only part of the finding is supported |
| Disputed | Credible evidence conflicts |
| Unknown | Insufficient evidence |
| Outdated | Evidence is no longer sufficiently current |

Confidence must be recorded separately.

### Preferred sources

Prioritise:
1. Official insurer policy documents.
2. Official reimbursement schedules.
3. Healthcare provider contract information.
4. Dutch legislation and government publications.
5. Nederlandse Zorgautoriteit (NZa).
6. Zorginstituut Nederland.
7. Independent research.
8. Credible specialist organisations and journalism.

Use lower-quality sources cautiously and explain their limitations.

## 9. Assessment methodology

Proposed rating scale:

| Rating | Meaning |
|---|---|
| 1 | Very poor |
| 2 | Poor |
| 3 | Average / mixed |
| 4 | Good |
| 5 | Excellent |
| null | Unknown |

Every proposed assessment requires:
- Explanation.
- Supporting evidence.
- Limitations.
- Confidence.
- Verification date.

Ratings remain proposals until approved by Operator.

Missing evidence must not be interpreted as poor or excellent performance.

## 10. Provisional scoring framework

| Category | Proposed weight |
|---|---:|
| Gender-affirming and hormone care | 20% |
| Freedom of provider choice | 15% |
| Climate/environment | 20% |
| Regional provider access | 15% |
| Mental healthcare | 7% |
| Women's healthcare | 5% |
| LGBTQIA+ inclusion | 5% |
| Disability accessibility | 5% |
| Human rights | 5% |
| Financial accessibility | 3% |
| **Total** | **100%** |

These weights are provisional and require Operator approval.

Proposed hard requirements:
- Gender-affirming healthcare.
- Freedom of provider choice.

A high aggregate score must not conceal a failure of an essential requirement.

The system must distinguish group ethics from provider and policy suitability.

## 11. Initial JSON architecture

Research works with:

- `groups`
- `providers`
- `policies`
- `claims`
- `sources`

Proposed assessment:

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

Proposed claim:

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

Coordinate schema changes with Development.

## 12. Initial research deliverables

1. Five group profiles.
2. Five representative provider profiles.
3. Verified 2027 policy profiles.
4. Ownership and legal-entity register.
5. Source register.
6. Claim register.
7. Evidence-backed assessments.
8. Research completeness report.
9. Unresolved questions.
10. Research methodology documentation.

Do not invent policies, conditions or research findings to populate empty records.

## 13. Handover requirements

Every Research → Development handover must include:

1. Research objective.
2. Applicable entity level.
3. Findings.
4. Claim IDs.
5. Source IDs.
6. Direct URLs.
7. Publication dates.
8. Verification dates.
9. Confidence.
10. Limitations.
11. Conflicting evidence.
12. Proposed JSON changes.
13. Unanswered questions.

Maintainer must also receive a progress update.

## 14. Authority restrictions

Research cannot:
- Invent findings.
- Approve its own final assessments.
- Change Operator-approved priorities.
- Change scoring weights without approval.
- Present proposed ratings as final conclusions.
- Treat unknown information as negative or positive.
- Independently redefine the application architecture.

Research may recommend improvements and identify missing research categories.

---

**Current assignment:** Establish the research methodology and begin the five initial group/provider investigations.

**Next handover:** Research → Maintainer and Research → Development.

**Final assessment authority:** Operator.