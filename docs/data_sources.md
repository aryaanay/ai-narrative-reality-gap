# Data sources

| Source | Role | Key limitation |
|---|---|---|
| [SEC EDGAR](https://www.sec.gov/search-filings/edgar-application-programming-interfaces) | AI claims, risks, partnerships, products, and filing dates | Filing structure varies; follow SEC access policies |
| [SEC Company Facts](https://www.sec.gov/Archives/edgar/daily-index/xbrl/companyfacts.zip) | Point-in-time fundamentals | Company-specific tags require normalization |
| [SEC ticker mapping](https://www.sec.gov/files/company_tickers_exchange.json) | CIK, ticker, and exchange linkage | Tickers can change; use CIK as the primary issuer key |
| [USPTO PatentsView](https://www.uspto.gov/ip-policy/economic-research/patentsview) | AI patents, citations, and assignees | Assignee-to-public-company resolution is nontrivial |
| [Epoch AI](https://epoch.ai/data/ai-models) | Major model releases and AI event dates | Model notability is curated |
| [Alpha Vantage](https://www.alphavantage.co/documentation/) | Prototype price data | Rate limits and historical coverage |
| CRSP via WRDS | Research-quality returns and delistings | Requires institutional access |
| [GDELT](https://www.gdeltproject.org/data.html) | Optional AI news and event candidates | Noisy entity matching; verify events independently |

## Proposed analytical table

One row per company-quarter:

- `cik`, ticker, company name, sector
- filing date and accession number
- AI claim count and claim specificity
- measurable-target and deadline indicators
- named provider/model/chip relationships
- AI patent count and citation-weighted patent measure
- R&D and capital-expenditure changes
- previous-claim fulfillment rate
- Narrative–Reality Gap score
- future abnormal return and volatility
- future revenue and operating-margin changes

## Data governance

Do not commit raw bulk filings, licensed price data, API keys, or credentials. Store source URLs, retrieval timestamps, checksums, and transformations so the analytical dataset can be reproduced.
