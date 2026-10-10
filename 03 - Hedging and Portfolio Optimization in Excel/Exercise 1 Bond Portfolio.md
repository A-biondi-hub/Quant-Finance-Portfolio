# Assignment 1 - Bond Portfolio, Mean-CVaR Optimisation and Single Index Model

## Setting

- **Valuation date:** 15/05/2025.
- **Data:** a spreadsheet with two sheets. The first contains daily observations of spread (with respect to the term structure), duration, price and IRR for a set of US Treasury bonds; the second contains the historical prices of a set of stocks.
- **Choices to make:** a selection of stocks, a selection of Treasury bonds and an investor utility function.
- **Universe size:** at least 4 assets per group member in each market (fixed income and equity).

## Tasks

1. **Optimal bond portfolio (immunisation).** Determine the portfolio of bonds that maximises future wealth according to immunisation theory, subject to:
   - no more than 40% invested in each bond whose duration is less than or equal to the empirical mean duration of the bonds considered;
   - a spread to maturity not higher than the average spread of the bonds considered.

2. **Optimal portfolio on the mean-CVaR (3%) frontier.** Determine the investor's optimal portfolio, given the chosen utility function, on the mean-CVaR 3% efficient frontier with no short sales. The IRR of the optimal bond portfolio from Task 1 is the riskless rate of the market.

3. **Single Index Model and Markowitz portfolio.** Taking the market portfolio of Task 2 as the index, estimate alpha and beta of the Single Index Model and compute the variance-covariance matrix of the assets under the model's assumptions. Then determine the optimal Markowitz portfolio with a target mean equal to the IRR of the bond portfolio, with no short sales.

Repeat the procedure every month for three months and plot the ex-post wealth of the portfolios from Tasks 2 and 3, assuming an initial wealth of EUR 100,000.

Finally, compute the certainty equivalent and the risk premium, and discuss the investor's risk aversion or tolerance.
