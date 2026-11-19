# AI Narrative Reality Gap

Companies talk about AI all the time, but it is not always clear whether those claims are backed by real work. This project looks at the gap between what public companies say about AI and what they actually appear to be doing.

## Main question

**Can we use AI to identify possible corporate AI washing, and does a large gap between AI claims and real investment help predict future stock performance or business results?**

## Why this matters

Some companies can point to real AI products, patents, partnerships, research spending, or measurable results. Others may use vague AI language without showing much evidence. Investors may initially respond to the story, then change their view once more information becomes available.

The goal is not to label a company as dishonest. The goal is to build a transparent score based on public evidence and test whether that score contains useful financial information.

## Starting scope

- S&P 100 companies
- Filings from 2022 onward
- One observation per company and quarter
- Main outcome: stock performance 3, 6, and 12 months after an AI claim
- Other outcomes: volatility, revenue growth, and operating margin changes

## Plan

1. Download 10-K, 10-Q, and 8-K filings from SEC EDGAR.
2. Find passages where companies discuss AI.
3. Use an LLM to turn each passage into structured data.
4. Record how specific each claim is and whether it includes a target, deadline, product, or named partner.
5. Look for supporting evidence such as patents, R&D spending, capital spending, partnerships, and later updates.
6. Build an AI Narrative Reality Gap score.
7. Compare the score with a simple baseline that only counts AI keywords.
8. Test whether either method helps explain future returns or business performance.
9. Build a dashboard that shows each score and the evidence behind it.

The LLM will help extract information from documents, but it will not make up the final score. The score will come from a clear formula or statistical model that can be inspected and tested.

## Data

- [SEC EDGAR APIs](https://www.sec.gov/search-filings/edgar-application-programming-interfaces)
- [SEC Company Facts](https://www.sec.gov/Archives/edgar/daily-index/xbrl/companyfacts.zip)
- [SEC company and ticker mapping](https://www.sec.gov/files/company_tickers_exchange.json)
- [USPTO PatentsView](https://www.uspto.gov/ip-policy/economic-research/patentsview)
- [Epoch AI model data](https://epoch.ai/data/ai-models)
- [Alpha Vantage](https://www.alphavantage.co/documentation/) or CRSP through UW
- [GDELT](https://www.gdeltproject.org/data.html) as an optional news source

More details are in [docs/data_sources.md](docs/data_sources.md).

## Project structure

```text
config/      Project settings
data/        Local data files
docs/        Notes about the data and methods
notebooks/   Exploration and analysis
src/         Reusable Python code
tests/       Tests
app/         Dashboard
```

## Setup

```bash
python -m venv .venv
# Windows
.venv\Scripts\activate

pip install -r requirements.txt
```

Copy `config/example.yaml` to `config/local.yaml` before changing the settings. API keys should go in a local `.env` file and should never be committed.

## Next steps

- [ ] Finalize the company list
- [ ] Build a table that connects CIKs, tickers, and company names
- [ ] Download the first set of SEC filings
- [ ] Write clear labeling rules for AI claims
- [ ] Manually label the first 100 examples
- [ ] Build a keyword baseline
- [ ] Build the claim extraction pipeline
- [ ] Create the first version of the score
- [ ] Run the financial analysis
- [ ] Build the dashboard

## Current status

The topic, research question, data sources, and initial project structure are set up. Data collection is next.

## License

The code is licensed under the MIT License. Each dataset keeps its own original license and terms.
