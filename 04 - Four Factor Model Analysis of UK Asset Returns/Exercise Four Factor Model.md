# Assignment - Four-Factor Model for UK Asset Returns

## Setting

**Objective.** Understand the sources of risk that lead to different expected returns across securities. The assignment builds on US research and tests a four-factor model for UK asset returns, based on the work of Fama, French and Carhart.

**Data.** A spreadsheet with monthly observations of:

- **SMB:** return on a size factor portfolio, long small-cap stocks and short large-cap stocks;
- **HML:** return on a value portfolio, long stocks with a high book-to-market ratio and short stocks with a low one;
- **UMD:** return on a momentum portfolio, long recent winners and short recent losers (in cumulative return terms), as in Carhart (1997);
- **RM:** return on the UK stock market;
- **RF:** UK risk-free return;
- **RMRF:** difference between the UK market return and the UK risk-free return;
- **S1-S10:** returns on 10 portfolios of UK stocks sorted by market capitalisation, from the smallest stocks (S1) to the largest (S10).

RMRF, SMB, HML and UMD are the risk factors; the ten size portfolios S1-S10 are the assets whose pricing the model has to explain.

## Tasks

1. **Basic statistics.**
   - Read the data.
   - From S1-S10 and the risk-free rate, create the excess returns of the ten portfolios (XS1-XS10).
   - Inspect the returns of each portfolio and comment on any exceptional features.
   - Compute summary statistics for the ten excess return series, and comment on how they vary across portfolios and on the implications of this variation.

2. **Time-series regressions.** For each excess return XS1-XS10:
   - regress the excess return on a constant, RMRF, SMB, HML and UMD;
   - interpret the regression coefficients and their t-ratios or p-values;
   - store the slope coefficients in an Excel file;
   - comment on the variation of risk exposures across factors and on how it can be interpreted;
   - interpret the $R^2$ of the regressions.

3. **Cross-sectional regressions.** Do risk exposures explain how mean returns vary across portfolios?
   - Run cross-sectional regressions with the ten mean returns of the size portfolios as the dependent variable, and as explanatory variables a constant and two sets of risk exposures taken from the time-series regressions: the exposure to RMRF and, in turn, the exposure to SMB, HML or UMD. Each regression has 10 observations, two explanatory variables and a constant.
   - Interpret the results.
