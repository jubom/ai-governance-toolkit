# AI Governance Toolkit

Practical, reusable templates for data and AI governance, maintained by **Janet Ubom** ([janetu.com](https://janetu.com)).

Most AI programs don't fail at the model. They fail at the data underneath it: unclear ownership, ambiguous definitions, unprotected personal data, and no agreed bar for what AI is allowed to consume. These templates turn that problem into concrete, adoptable controls.

## What's inside

| Folder | What it gives you | Format |
|---|---|---|
| [`pii-tagging/`](pii-tagging/) | A sensitive-data tag taxonomy, risk tiers, and a phased path from discovery to masking | YAML, Markdown |
| [`ai-readiness-certification/`](ai-readiness-certification/) | A 6-stage certification lifecycle and the criteria an asset must meet before AI may use it | Markdown, CSV |
| [`vendor-evaluation/`](vendor-evaluation/) | A weighted scorecard for evaluating AI-assisted data quality and governance tools | CSV, Markdown |
| [`dq-rule-library/`](dq-rule-library/) | Generic data quality rules organized by dimension, written in business language | CSV, Markdown |
| [`traceability/`](traceability/) | A model that links strategic priorities to the work that delivers them | Markdown |

## Principles behind the toolkit

1. **AI readiness is a certification, not a feeling.** If no one can name the owner, definition, quality threshold, and known limits, the data isn't ready for AI.
2. **Built is not the same as certified.** Implementation teams build; governance decides what the business may rely on.
3. **Find it before you protect it.** Masking, access control, and AI guardrails all depend on knowing where sensitive data lives.
4. **Measure trust and adoption, not artifacts.** Track how much of the business runs on certified data, not how many policies exist.

## How to use it

Each folder stands alone. Copy what you need, replace the example values with your own domains, owners, and thresholds, and adapt the wording to your organization. All examples use fictional table and column names.

## Alignment

The templates are designed to support programs aligned with NIST AI RMF, ISO/IEC 42001, the EU AI Act, GDPR and CCPA, and DAMA-DMBOK. They are practical starting points, not legal or compliance advice.
