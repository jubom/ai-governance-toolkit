# PII Risk-to-Remediation Playbook

A phased approach for getting sensitive data under control in a data catalog (for example, Databricks Unity Catalog), so masking, access control, and AI guardrails have something reliable to act on.

## Why tagging comes first

Column masking, row-level security, access reviews, and AI data-use rules all depend on one question: *where does sensitive data live?* If the answer lives in engineers' heads rather than the catalog, every later control is guesswork. Tagging is the foundation.

## The four phases

| Phase | Goal | Typical duration | Exit criteria |
|---|---|---|---|
| 0. Define the taxonomy | Agree the standard with Security, Privacy, and Legal | 1 week | Taxonomy approved and published |
| 1. Pilot | Tag the highest-exposure, consumer-facing tables first | 2 weeks | Pilot tables fully tagged and reviewed by stewards |
| 2. Scale | Generate and apply tags programmatically across all high-risk columns | 3–4 weeks | 100% of high-risk columns tagged |
| 3. Validate and operationalize | Reconcile coverage, get sign-off, and make tagging part of onboarding | Ongoing | Tag coverage reported as a recurring governance metric |

Masking and row-level security are **separate, follow-on phases**. Make that explicit: stakeholders often assume tagging alone solves the exposure. It doesn't; it makes the fix possible.

## Prioritizing what to tag first

Rank tables by exposure, not by size:

1. **Consumer-facing gold or reporting tables** that many people and tools can query.
2. **Tables feeding AI** (retrieval, agents, natural-language analytics, model training).
3. **High-risk categories**: government IDs, financial identifiers, contact details, dates of birth.
4. Everything else in the inventory.

## Applying tags at scale

Generate tagging statements from your scan inventory rather than tagging by hand. Example pattern for Unity Catalog (fictional names):

```sql
ALTER TABLE sales.gold.dim_customer
  ALTER COLUMN email_address
  SET TAGS ('pii' = 'email', 'pii_risk' = 'high');
```

## Metrics to report

- High-risk tag coverage (% of identified high-risk columns tagged)
- Unreviewed classifications awaiting steward confirmation
- New sensitive columns found since the last scan
- Consumer-facing tables with sensitive data and no mask

## Common risks

| Risk | Mitigation |
|---|---|
| Columns misclassified without business context | Steward review built into the pilot and scale phases |
| Manual tagging drifts out of date | Programmatic tagging plus a scheduled re-scan |
| Tagging mistaken for protection | Scope masking and access control as named next phases |
| Cross-team coordination stalls | A named owner per phase and a weekly check-in |

See [`pii_tag_taxonomy.yaml`](pii_tag_taxonomy.yaml) for the tag standard.
