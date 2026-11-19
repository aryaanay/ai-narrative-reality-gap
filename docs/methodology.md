# Methodology plan

## Hypothesis

Companies with highly specific and verifiable AI claims supported by observable commitment will have more persistent operating outcomes than firms with intense but vague AI narratives. A large narrative–reality gap may be followed by stock-price reversal or higher volatility.

## Baselines

1. No AI variables
2. Raw count of the terms AI, artificial intelligence, generative AI, and machine learning
3. Evidence-grounded claim features
4. Full Narrative–Reality Gap score

## Validation

- Manually annotate at least 300 filing passages.
- Measure extraction precision, recall, and agreement with human labels.
- Use chronological train/test splits.
- Preserve filing availability dates to avoid look-ahead bias.
- Include size, industry, valuation, prior returns, and market returns as controls.
- Report effect sizes and uncertainty, not only statistical significance.

## Candidate score

```text
Narrative–Reality Gap =
  standardized claim intensity
+ standardized vagueness
+ standardized unfulfilled prior promises
- standardized patent activity
- standardized financial commitment
- standardized verified product/partnership evidence
```

Weights will be documented and tested through sensitivity analysis. A learned score will be compared with an equal-weight version.

## Deliverable

A dashboard showing a company's score, time series, cited filing evidence, observable commitment signals, and subsequent financial outcomes.
