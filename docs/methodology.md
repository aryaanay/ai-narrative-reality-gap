# Methodology

## Main idea

I expect companies with specific AI claims and visible follow through to have more reliable results than companies that use a lot of vague AI language. A large gap between the story and the evidence may be followed by weaker returns or higher volatility.

This is a hypothesis, not an assumption. The analysis may find little or no relationship, which would still be a useful result.

## What counts as an AI claim?

An AI claim is a statement about an AI product, investment, partnership, expected source of revenue, cost saving, workforce change, or internal use.

For each claim, I plan to record:

- The exact passage
- The filing and date
- The type of claim
- Any named product, model, chip, or partner
- Whether the company gives a number or deadline
- How specific the statement is
- Whether later filings provide evidence that it happened

## Models to compare

1. A financial model with no AI variables
2. A simple count of AI related keywords
3. A model using structured claim features
4. A model using the full Narrative Reality Gap score

This comparison will show whether the more detailed approach adds anything beyond simply counting how often a company says AI.

## Possible score

```text
Narrative Reality Gap =
  claim intensity
+ vague language
+ earlier claims without follow through
- patent activity
- financial commitment
- verified products and partnerships
```

Each part will be standardized before it is combined. I will start with equal weights because they are easy to explain, then test whether other reasonable weights change the results.

## Validation

- Manually review at least 300 filing passages
- Measure precision and recall for the claim extraction process
- Split training and testing by time
- Only use information that was public on the prediction date
- Control for company size, industry, valuation, prior returns, and market returns
- Report effect sizes and uncertainty
- Run sensitivity checks using different score definitions and time horizons

## Final product

The dashboard will let someone search for a company and see:

- Its current score
- How the score has changed
- The filing passages behind the score
- Evidence of real AI investment or follow through
- Stock and financial outcomes after earlier claims
- A clear explanation of how the score was calculated
