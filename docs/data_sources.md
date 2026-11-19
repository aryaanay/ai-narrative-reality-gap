# Data sources

These are the main datasets I plan to use. I will start with SEC filings, financial data, patents, and stock prices. The other sources can be added later if there is enough time.

| Source | How I will use it | Main issue |
|---|---|---|
| [SEC EDGAR](https://www.sec.gov/search-filings/edgar-application-programming-interfaces) | Find AI claims, risks, products, partnerships, and filing dates | Filing formats are not always consistent |
| [SEC Company Facts](https://www.sec.gov/Archives/edgar/daily-index/xbrl/companyfacts.zip) | Get revenue, R&D, capital spending, margins, and other financial data | Company specific tags may need to be cleaned |
| [SEC ticker mapping](https://www.sec.gov/files/company_tickers_exchange.json) | Connect CIKs, company names, tickers, and exchanges | Tickers can change, so CIK will be the main company ID |
| [USPTO PatentsView](https://www.uspto.gov/ip-policy/economic-research/patentsview) | Measure AI patent activity and patent citations | Patent owner names have to be matched to public companies |
| [Epoch AI](https://epoch.ai/data/ai-models) | Create a timeline of important model releases | The list of notable models is curated |
| [Alpha Vantage](https://www.alphavantage.co/documentation/) | Get stock prices for the first prototype | The free API has rate limits |
| CRSP through WRDS | Run a stronger version of the stock return analysis | Access may depend on UW subscriptions |
| [GDELT](https://www.gdeltproject.org/data.html) | Find possible AI news and company events | News data can be noisy and needs to be checked |

## Final analysis table

The goal is to create one row for each company and quarter. It may include:

- CIK, ticker, company name, and industry
- Filing date and accession number
- Number of AI claims
- Claim specificity
- Whether a claim includes a measurable target or deadline
- Named AI providers, models, or chips
- AI patent counts and citations
- Changes in R&D and capital spending
- Whether earlier claims were later supported
- AI Narrative Reality Gap score
- Future stock returns and volatility
- Future revenue and operating margin changes

## Data rules

Large filing archives, paid market data, and API keys will not be uploaded to GitHub. I will save source links, download dates, and transformation steps so the final analysis can be reproduced.
