# Assignment - Leverage Procyclicality of Financial Institutions

## Setting

**Objective.** Study how financial institutions manage their balance sheets, and in particular whether leverage is procyclical, that is, whether institutions increase leverage when their assets grow and reduce it when they shrink.

**Data.** A spreadsheet with quarterly observations for each financial entity, for a financial system chosen between the United States and China. The entities belong to three types: Commercial Banks, Finance Services and Real Estate Finance Services. The variables are:

- total assets (US$ million);
- equity market value (US$ billion);
- price;
- leverage ratio;
- market-to-book value ratio.

## Tasks

1. **Basic statistics.**
   - Choose the financial system and read the data.
   - Create a panel dataset.
   - For total assets, leverage and equity market value, take the natural logarithm and compute the growth rate.
   - Inspect the variables of each financial entity and comment on any exceptional features.
   - Compute summary statistics for the variables, comment on how they vary across financial entities and on the implications of this variation, and provide some stylised facts.

2. **Panel analysis over the whole period.** How sensitive is the leverage ratio to size growth? For the entire panel:
   - regress $\text{leverage growth}_{i,t}$ on $\text{size growth}_{i,t}$, $\ln(\text{leverage}_{i,t-1})$ and time dummies;
   - regress $\text{leverage growth}_{i,t}$ on $\text{size growth}_{i,t}$, $\text{market-to-book}_{i,t-1}$, $\ln(\text{leverage}_{i,t-1})$ and time dummies;
   - repeat both regressions using equity market value instead of total assets as the measure of size;
   - interpret the regression coefficients and their t-ratios or p-values, and the $R^2$ of the regressions.

3. **Panel analysis by sub-period and financial entity.** Is leverage procyclicality different for each sub-period and for each type of financial entity?
   - Based on the literature on procyclicality, identify at least two sub-periods that characterise financial distress in the financial market.
   - Run a panel regression for each type of financial entity separately, with $\text{leverage growth}_{i,t}$ as the dependent variable and $\text{size growth}_{i,t}$, $\text{market-to-book}_{i,t-1}$ and $\ln(\text{leverage}_{i,t-1})$ as explanatory variables, controlling for time dummies.
   - Run a panel regression for each sub-period, for all financial entities together, with the same dependent and explanatory variables.
   - Run two panel regressions that capture the different procyclical behaviour of each type of financial entity.
   - Interpret the results.
