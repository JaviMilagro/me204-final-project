# ME204 Final Project: DO SOFT DRINKS SOLD IN THE UK AND FRANCE CONTAIN LESS SUGAR THAN THOSE SOLD IN GERMANY AND ITALY?


| GitHub username                           | LSE ID            |
| ----------------------------------------- | ----------------- |
| JaviMilagro                               | 250100007         |


## Overview

Sugar taxes are meant to give manufacturers a financial reason to reformulate
their drinks, so a market where sugary drinks are taxed should end up with less
sugar on the shelves. This project tests that by comparing the sugar content of
sodas sold in two taxed markets (United Kingdom, France) against two untaxed ones
(Germany, Italy).

Italy is a borderline case handled deliberately: Italian law contains a sugar tax
enacted in 2019, but it has been postponed repeatedly and has never come into
force, so Italy counts as untaxed here. NB01 sets out the policy sources for all
four countries.

## Data sources

[Open Food Facts](https://world.openfoodfacts.org), a free and open database of
food products built by volunteers, available under the Open Database License.
Data is collected through the Search-a-licious search API at
`https://search.openfoodfacts.org/search`.

The project collects **every soda the database holds** for the four countries:
6,557 products in total (512 UK, 3,765 France, 1,943 Germany, 337 Italy).

## How to reproduce

**Python packages:** `pandas`, `plotly`, `requests`. Everything else used
(`json`, `pathlib`) is in the standard library.

**Credentials: none required.** Open Food Facts does not need an API key or an
account for reading data.

**One thing you must change, though.** The API's terms ask every user to identify
themselves with a custom `User-Agent` header containing an app name and a contact
email. Mine is hardcoded in NB01:

```python
HEADERS = {"User-Agent": "ME204-LSE-project/1.0 j.milagro-caro@lse.ac.uk"}
```

Replace the email with your own before running NB01, so the traffic is attributed
to you rather than to me.

## Run order

Run the three notebooks in order. Each depends on the output of the one before.

| # | Notebook | Reads | Does | Writes |
|---|---|---|---|---|
| 1 | `NB01-Data-Collection.ipynb` | Open Food Facts API | Paginates through every soda for each of the four countries, 100 products per request | `data/raw/united-kingdom.json`, `france.json`, `germany.json`, `italy.json` |
| 2 | `NB02-Data-Transformation.ipynb` | `data/raw/*.json` | Flattens the nested JSON into one row per product per country, counts missing sugar values, checks for products shared between countries, drops rows with no sugar value | `data/processed/sodas_clean.csv` (6,086 rows) |
| 3 | `NB03-Data-Analysis.ipynb` | `data/processed/sodas_clean.csv` | Classifies countries by tax status, separates zero-sugar from full-sugar drinks, compares sugar content across countries, produces two charts | `docs/` [confirm — see note below] |

![Sugar content by country](docs/sugar_by_country.png)

