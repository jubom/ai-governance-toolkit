# AI Data Quality Vendor Scorecard

A way to evaluate AI-assisted data quality and governance platforms against **your** operating model, not the vendor's demo.

## The core risk

Vendor-led proofs of concept are designed to show a product's strengths. Without your own success criteria, it's easy to "successfully" demonstrate selected features while never testing the platform against how your business will actually run it.

## How to use the scorecard

1. **Write your success criteria before the vendor's plan arrives.** Use the capabilities in [`ai_dq_vendor_scorecard.csv`](ai_dq_vendor_scorecard.csv) as a starting list.
2. **Map the vendor's proposed plan against it.** Mark each capability Covered, Partial, or Gap.
3. **Close the gaps before kickoff.** Agree one plan that defines Data → Rules → Capabilities → Success criteria.
4. **Test with real rules and known answers.** Seeded errors are useful, but also run rules whose correct results you already know, and compare.
5. **Score with weights** that reflect your priorities, then decide.

## Questions vendors should answer in writing

- Are there limits on rows evaluated, failures captured, or results displayed?
- Is the full eligible population evaluated, or is it sampled?
- Can results be queried directly for dashboards and quality scores?
- How are execution failures distinguished from data quality failures?
- How are accepted exceptions handled without suppressing real failures?
- How are rule changes reviewed, approved, and versioned?
