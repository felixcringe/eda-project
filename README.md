# EDA-Project: King County House Sales

Time-boxed exploratory data analysis of **21,420 home sales** in King County, Washington (May 2014 – May 2015), conducted as a neuefische bootcamp project. The analysis tests three general hypotheses about the housing market and translates them into concrete recommendations for a specific buyer-side client.

## Client

**Thomas Hansen** — buyer · five kids · low budget · looking for a nice (social) family neighborhood.

## Hypotheses

1. Price differs substantially across zip codes — there is high price variance between regions.
2. Lower-price regions don't necessarily have worse-condition or lower-grade houses.
3. Renovated houses sell above comparable un-renovated ones.

## Data

- **Source:** King County house sales dataset, pulled from the bootcamp's `eda` schema into `data/eda.csv`. For data retrieval the File `1_Fetching_the_data_eda` was used.
- **Scope:** 21,420 sales · May 2014 – May 2015 · 70 zip codes.
- **Column descriptions:** see `column_names.md`.
- **Note:** the `data/` directory is gitignored.

## Repository structure

```
.
├── EDA.ipynb            # main analysis notebook (load → clean → hypotheses → insights → client → recommendations)
├── data/                # raw CSV (gitignored)
├── column_names.md      # column descriptions
├── workflow.md          # bootcamp EDA workflow reference
├── presentation.pdf     # 10-min non-technical slide deck for the client
├── requirements.txt     # pinned dependencies
└── README.md
```

## Setup

```bash
# Python 3.10+ recommended
python -m venv .venv
source .venv/bin/activate          # macOS / Linux
# .venv\Scripts\activate           # Windows

pip install -r requirements.txt
jupyter notebook EDA.ipynb
```

Place the data file at `data/eda.csv` before running.

## Key insights

1. **Location is the dominant price driver.** Median price-per-sqft varies up to **~3.8×** across zip codes and falls with distance from downtown Seattle.
2. **Affordable neighborhoods are not run-down.**
3. Renovated homes sell at higher \$ per sqft