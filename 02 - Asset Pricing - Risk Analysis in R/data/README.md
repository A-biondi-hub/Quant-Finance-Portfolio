# Data

The input files are **not included** in this repository. To reproduce the analysis, put them in this folder with the names below.

<!-- TODO: add the source of each file (course material / public dataset) and check that it can be shared before publishing it -->

| File | Used in | Columns used |
|:--|:--|:--|
| `obbligazioni_portafoglio.csv` | Part 1 | `bond_id`, `cashflow`, `time_years`, `market_price` (one row per cash flow) |
| `curva_tassi_storico.csv` | Part 4 | first column: date; then one column per maturity (1, 2, 3, 5, 7, 10, 20, 30 years), rates in % |
| `indici_azionari_storico.csv` | Part 5 | `Eq_A`, `Eq_B`, `Eq_C`, `Eq_D` (index levels) |
| `firms_merton.csv` | Part 6 | `firm_id`, `V0`, `F_debt`, `r`, `sigma_V`, `T_mat` |
| `prosper_loans_credit.csv` | Part 8 | `ListingKey`, `ProsperRating_Alpha`, `LoanOriginationDate`, `ClosedDate`, `LoanStatus`, `LP_GrossPrincipalLoss`, `LP_NetPrincipalLoss`, `LoanOriginalAmount`, `CreditScoreRangeLower`, `CreditScoreRangeUpper`, `DebtToIncomeRatio`, `StatedMonthlyIncome` |
