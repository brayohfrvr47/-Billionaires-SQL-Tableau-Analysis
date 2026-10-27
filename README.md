# Forbes Billionaires Analysis (SQL + Tableau)

## Goal
I analyzed a billionaires dataset in MySQL to answer business questions about
wealth, industry, age, gender and country, then visualized the results in
Tableau Public.

## Tools
MySQL (Workbench), Excel, Tableau Public

## Dataset
- Source: [billionaires dataset](https://www.kaggle.com/datasets/ahmedmohamedibrahim1/billionaires-dataset)
- Original file: `billionaires_dataset.csv`
- Working table in MySQL: `billionaires_portfolio`
- 475 rows, 19 columns, no duplicate rows or blank values

## Data notes
- `finalWorth` is in millions of USD, so I converted to billions where needed
  to make results easier to read.
- `category` and `industries` contain identical values, so I used `industries`.
- `selfMade` is stored as TRUE/FALSE (FALSE = inherited).
- About 80 entries are family fortunes (e.g. "X & family"), so counts mean
  entries on the list, not strictly individuals.
- Country-level columns (population, GDP, tax rate, etc.) repeat on every row,
  so I grouped by country first to avoid counting them multiple times.
- The source CSV is Latin-1 encoded; I checked that accented names (e.g. François,
  Saadé) imported correctly.
- Minor spelling inconsistency in source like "Francoise" vs "François" (I haven't corrected it,
  doesn't affect the analysis).
