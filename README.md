# AI Narrative–Reality Gap

An evidence-grounded AI and finance project investigating whether companies that make strong AI claims without observable implementation subsequently experience weaker financial performance or stock-price reversals.

## Research question

**Can an evidence-grounded AI system identify corporate AI-washing, and does the gap between a company's AI claims and observable AI investment predict subsequent stock-price reversals or financial performance?**

## Initial scope

- **Universe:** S&P 100 companies
- **Period:** 2022 onward
- **Unit of analysis:** company-quarter
- **Primary outcome:** 3–12 month abnormal stock return after AI-related claims
- **Secondary outcomes:** realized volatility, revenue growth, and operating-margin change

## Method

1. Collect 10-K, 10-Q, and 8-K filings from SEC EDGAR.
2. Extract AI-related claims with exact supporting passages.
3. Score claim specificity, measurability, deadlines, and named technologies.
4. Measure observable commitment using patents, R&D, capex, partnerships, and later disclosures.
5. Construct an interpretable **AI Narrative–Reality Gap**.
6. Compare it with simple AI keyword-count baselines.
7. Test its relationship with future returns and operating performance.
8. Present company scores and evidence in an interactive dashboard.

The language model will extract structured evidence; it will not assign an unexplained final score. The final index will use a documented formula or calibrated statistical model.

## Core data sources

- [SEC EDGAR APIs](https://www.sec.gov/search-filings/edgar-application-programming-interfaces)
- [SEC Company Facts bulk data](https://www.sec.gov/Archives/edgar/daily-index/xbrl/companyfacts.zip)
- [SEC ticker/exchange mapping](https://www.sec.gov/files/company_tickers_exchange.json)
- [USPTO PatentsView](https://www.uspto.gov/ip-policy/economic-research/patentsview)
- [Epoch AI model data](https://epoch.ai/data/ai-models)
- [Alpha Vantage](https://www.alphavantage.co/documentation/) or institutional CRSP data
- [GDELT](https://www.gdeltproject.org/data.html) as an optional event source

See [docs/data_sources.md](docs/data_sources.md) for roles and limitations.

## Repository layout

```text
config/      Project configuration
data/        Local data directories (large/raw files are ignored)
docs/        Methodology and source documentation
notebooks/   Exploration and analysis notebooks
src/         Reusable collection, extraction, scoring, and analysis code
tests/       Automated tests
app/         Dashboard code
```

## Setup

```bash
python -m venv .venv
# Windows: .venv\Scripts\activate
# macOS/Linux: source .venv/bin/activate
pip install -r requirements.txt
```

Copy `config/example.yaml` to `config/local.yaml` and customize it. Never commit API keys.

## Planned milestones

- [ ] Freeze universe and company identifier table
- [ ] Download SEC filings and XBRL facts
- [ ] Define AI-claim annotation guide
- [ ] Label the first 100 claims
- [ ] Build keyword-count baseline
- [ ] Build evidence-grounded claim extractor
- [ ] Construct commitment variables and gap score
- [ ] Run event study and panel regressions
- [ ] Build dashboard
- [ ] Publish results, limitations, and reproducibility notes

## Status

Project initialization and research design.

## License

Code is available under the MIT License. Source datasets retain their original terms and licenses.
