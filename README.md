# Trading data storage

Data files read by QuantConnect backtests in a personal trading research project.

| File | What it holds | Source |
|---|---|---|
| `insider/insider_buys_2010_2022.csv` | Corporate insiders' open-market purchases, one row per filing date and ticker, 2010-2022 | SEC Insider Transactions Data Sets (public) |

## insider_buys_2010_2022.csv

Filters: Form 4 open-market purchases (code P) of common stock by officers or directors, at least $25,000 per filing.

| Column | Meaning |
|---|---|
| `filing_date` | Date the filing was made public (use this, never the trade date) |
| `ticker` | Issuer's ticker as reported on the filing |
| `opportunistic` | True if the insider traded in each of the 3 prior years and not in this calendar month in all 3 (Cohen, Malloy & Pomorski 2012) |
| `cluster` | True if a different insider of the same company filed a buy within the prior 10 days |
