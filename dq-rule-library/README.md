# Data Quality Rule Library

Generic, reusable data quality rules organized by quality dimension. Each rule is written in business language first, so it can be reviewed by business owners and translated into SQL, a data quality tool, or an AI assistant prompt.

## How to use it

1. Pick the rules that match your domains and adjust the business rule to your definitions.
2. Assign an owner and a severity to each.
3. Implement the rule in your platform and record the expected eligible population.
4. Track evaluated count, failed count, and failure rate over time.

All rules are in [`dq_rule_library.csv`](dq_rule_library.csv). Entity and field names are generic examples.

## Writing a good rule

A good rule states:

- **The business rule**: what must be true, in plain language.
- **The business impact**: why a failure matters.
- **The required data elements**: what the rule needs to run.
- **The eligible population**: which records the rule applies to.

The business-language description doubles as a prompt for AI-assisted rule creation. If an AI tool can't produce the right rule from it, the description probably isn't precise enough for people either.
