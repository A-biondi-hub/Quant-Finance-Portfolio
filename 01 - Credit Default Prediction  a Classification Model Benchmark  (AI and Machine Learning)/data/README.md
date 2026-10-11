# Data

The input file is **not included** in this repository. To reproduce the analysis, put `credit.csv` in this folder.

<!-- TODO: add the source and the download link of the dataset (check the licence before publishing the file) -->

`credit.csv` contains 6,000 credit requests with a binary target and ten predictors. The columns, in this order, are renamed in the report as:

| Column | Description |
|:--|:--|
| `Default` | Target: 1 = the applicant defaulted, 0 = no default |
| `RevUtil` | Revolving utilisation: balance on credit lines / credit limit |
| `Age` | Age of the applicant |
| `Late30_59D` | Number of times 30-59 days past due |
| `DebtRatio` | Monthly debt payments / monthly income |
| `Income` | Monthly income |
| `Openlines` | Number of open credit lines and loans |
| `Late90D` | Number of times 90 days or more past due |
| `RealEstate` | Number of real estate loans or lines |
| `Late60_89D` | Number of times 60-89 days past due |
| `Dependents` | Number of dependents |
