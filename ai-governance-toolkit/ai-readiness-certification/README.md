# AI-Readiness Certification Framework

A lifecycle and set of criteria for deciding when a dataset or business metric is trustworthy enough for people and AI systems to treat as authoritative.

**The certification question:** *Can we confidently allow people and AI systems to use this asset as an authoritative representation of the business?*

## The lifecycle

| Stage | What it means | Who signs off |
|---|---|---|
| 1. Draft | Definition proposed | Data Governance |
| 2. Validated | Definition, owner, and logic agreed | Data Governance + Domain Owner |
| 3. Implemented | Built in the platform or semantic layer | Implementation team |
| 4. Certified | Meets all certification criteria | Data Governance |
| 5. AI-Ready | Approved for consumption by AI systems | Data Governance |
| 6. Monitored | Quality, usage, and drift tracked; recertified on change | Data Governance + Implementation team |

**Implemented is not Certified.** Keeping those stages separate stops technical completion from being mistaken for business approval.

## What must be true before certification

| Area | Criteria |
|---|---|
| Business | Definition approved; owner assigned; intended use documented; calculation understood |
| Data | Authoritative source identified; lineage available; quality requirements met; known limitations documented |
| Semantic | Mappings and relationships validated; terminology standardized; conflicting definitions resolved |
| Governance | Required metadata complete; certification status recorded; change process in place |
| AI readiness | Meaning explicit and unambiguous; quality threshold met; limitations documented; consistent with access controls and sensitive-data rules |

The full checklist is in [`certification_checklist.csv`](certification_checklist.csv).

## Standard fields for a certified metric

| Field | Description |
|---|---|
| Metric name | Standard business name |
| Business definition | What the metric means, in plain language |
| Business owner | Accountable domain owner |
| Technical owner | Team that implements and maintains it |
| Source assets | Authoritative governed data it draws from |
| Calculation logic | Approved calculation |
| Population and exclusions | Records included and excluded |
| Approved dimensions | How it may be sliced |
| Quality requirements | Minimum quality expectations |
| Certification status | Draft, Validated, Implemented, Certified, AI-Ready, Monitored |
| AI readiness | Whether it is approved for AI consumption |
| Last review | Date of the most recent certification review |

## Measuring success

Measure trust and adoption, not the number of objects built:

- % of business-critical metrics certified
- Time to certify a new metric
- Usage of certified versus uncertified definitions
- AI use cases running on certified data
- Incidents of AI or reports misinterpreting a metric
