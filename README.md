# Quantitative Finance Portfolio

Selected projects in quantitative finance, risk management and financial econometrics, developed during my MSc in Quantitative Finance and Insurance at the University of Bergamo.

Each folder is self-contained. The two R projects come with an R Markdown report (code, output, plots and commentary); the other folders contain the task statements together with the final deliverables: Excel models, group reports, slide decks and Python notebooks.

## Projects at a glance

| # | Project | Main topics | Tools | Format |
|:-:|:--|:--|:--|:--|
| 01 | [Credit Default Prediction: a Classification Model Benchmark](01%20-%20Credit%20Default%20Prediction%20-%20Classification%20Model%20Benchmark) | Credit scoring, supervised learning, class imbalance | R, caret, rpart, randomForest, gbm, Keras/TensorFlow | R Markdown report + code |
| 02 | [Asset Pricing and Risk Analysis in R](02%20-%20Asset%20Pricing%20-%20Risk%20Analysis%20in%20R) | Yield curve, option pricing, Greeks, PCA, VaR/ES, Merton, copulas, Basel IRB | R, mvtnorm, tidyverse | R Markdown report + code |
| 03 | [Hedging and Portfolio Optimisation in Excel](03%20-%20Hedging%20and%20Portfolio%20Optimization%20in%20Excel) | Spread options, STARR ratio, Mean-CVaR, Single Index Model | Excel (Monte Carlo, Solver) | Group assignment, 2 workbooks |
| 04 | [Four-Factor Analysis of UK Asset Returns](04%20-%20Four%20Factor%20Model%20Analysis%20of%20UK%20Asset%20Returns) | Fama-French and Carhart models, cross-sectional regressions | Econometrics, factor models | Group report |
| 05 | [Leverage Procyclicality in Chinese Financial Institutions](05%20-%20Leverage%20Procyclicality%20Analysis%20in%20Chinese%20Financial%20Institutions) | Panel regressions, accounting vs market leverage, systemic risk | Panel econometrics | Group report |
| 06 | [Macro-Finance Paper Presentations](06%20-%20Macro-Finance%20Papers%20Presentations) | Central bank digital currency, monetary policy and redistribution | Academic presentations | 2 slide decks (PDF) |
| 07 | [Python Notebooks: Stock Ranking and Risk Metrics](07%20-%20Python%20-%20Stock%20Ranking%20and%20Risk%20Metrics) | TOPSIS and VIKOR, composite Sharpe-style ranking, Sortino, Treynor, alpha, stochastic dominance | Python, NumPy, pandas | 3 Jupyter notebooks |

---

## 01 - Credit Default Prediction: a Classification Model Benchmark

Course project for AI and Machine Learning for Finance. Benchmark of 14 classification models (including variants) for predicting whether a credit applicant will default, on a dataset of 6,000 credit requests with a 6.7% default rate. All models share the same cleaning, the same stratified 70/30 train/test split and the same metrics (Accuracy, Precision, Recall, F1, AUC), so the results are directly comparable.

- **Methods**: logistic regression, LDA, QDA, Naive Bayes, KNN with cross-validated K, classification and regression trees with pruning, bagging, random forest, boosting, three neural networks.
- **Main findings**: LDA has the best ranking performance (AUC 0.843); boosting is the best ensemble (AUC 0.832); a pruned tree with 3 splits has the highest recall (0.727) but low precision, so the best model depends on the relative cost of a missed default versus a false alarm.
- **Files**: [`README.md`](01%20-%20Credit%20Default%20Prediction%20-%20Classification%20Model%20Benchmark/README.md) (summary and results table), [`credit_default_benchmark.md`](01%20-%20Credit%20Default%20Prediction%20-%20Classification%20Model%20Benchmark/credit_default_benchmark.md) (full report), [`credit_default_benchmark.Rmd`](01%20-%20Credit%20Default%20Prediction%20-%20Classification%20Model%20Benchmark/credit_default_benchmark.Rmd) (source).

## 02 - Asset Pricing and Risk Analysis in R

Implementation from scratch of the main building blocks of quantitative asset pricing and financial risk management, in eight parts: Svensson yield curve and bond pricing; option pricing (Monte Carlo, binomial tree, Black-Scholes-Merton); Greeks and delta-hedging; PCA on interest rates; VaR and Expected Shortfall; Merton structural model; Gaussian and Student's t copulas; Basel IRB capital for a retail loan portfolio.

- **Main findings**: the first two principal components explain 98.9% of the variance of rate changes; with the same marginals and correlation, the t copula gives a joint default probability about 2.1 times higher than the Gaussian one; ignoring correlation makes the unexpected loss of a retail portfolio tens of times smaller than the Vasicek/Basel capital.
- **Files**: [`README.md`](02%20-%20Asset%20Pricing%20-%20Risk%20Analysis%20in%20R/README.md), [`asset_pricing_risk_analysis.md`](02%20-%20Asset%20Pricing%20-%20Risk%20Analysis%20in%20R/asset_pricing_risk_analysis.md) (full report), [`asset_pricing_risk_analysis.Rmd`](02%20-%20Asset%20Pricing%20-%20Risk%20Analysis%20in%20R/asset_pricing_risk_analysis.Rmd) (source).

## 03 - Hedging and Portfolio Optimisation in Excel 

Two fully formula-driven Excel workbooks (Monte Carlo simulation and Solver optimisation), each with the task statement it solves.

- [`Bond Portfolio.xlsx`](03%20-%20Hedging%20and%20Portfolio%20Optimization%20in%20Excel/Bond%20Portfolio.xlsx) (task: [`Exercise 1 Bond Portfolio.md`](03%20-%20Hedging%20and%20Portfolio%20Optimization%20in%20Excel/Exercise%201%20Bond%20Portfolio.md))
  - Immunised bond portfolio.
  - Mean-CVaR (3%) efficient frontier without short selling and optimal portfolio at three rebalancing dates.
  - Single Index Model and Markowitz portfolio at each date.
  - Ex-post wealth over three months and summary of certainty equivalent, risk premium and performance.
- [`Spread Options STARR PCA.xlsx`](03%20-%20Hedging%20and%20Portfolio%20Optimization%20in%20Excel/Spread%20Options%20STARR%20PCA.xlsx) (task: [`Exercise 2 Spread Options.md`](03%20-%20Hedging%20and%20Portfolio%20Optimization%20in%20Excel/Exercise%202%20Spread%20Options.md))
  - Monte Carlo pricing (5,000 scenarios per asset, risk-neutral measure) of 6 at-the-money call spreads and 6 put spreads with 3-month maturity.
  - Hedged portfolio that maximises the STARR ratio with 3% CVaR, checked after 5 trading days and at maturity.
  - Portfolio choice on a universe of 36 assets (about 2,500 daily observations): PCA on the correlation matrix, approximation via conditional expectations on 16 cells, regression on the first two principal components, and ex-post wealth to maturity.

## 04 - Four-Factor Analysis of UK Asset Returns 

Empirical study of ten UK equity portfolios sorted by market capitalisation (monthly data, 1980-2010) with the Fama-French three-factor model and Carhart's four-factor model (momentum). It covers time-series regressions of excess returns, the impact of outliers through winsorising, cross-sectional regressions of average returns on estimated betas, and statistical diagnostic tests.

- **Data**: [`First_Assignment_dataset.xlsx`](04%20-%20Four%20Factor%20Model%20Analysis%20of%20UK%20Asset%20Returns/First_Assignment_dataset.xlsx), a monthly dataset with the factors (market excess return RMRF, SMB, HML, UMD) and the risk-free rate, plus the returns of the ten portfolios S1-S10.
- **Files**: [`Four Factor Analysis UK Asset Returns.pdf`](04%20-%20Four%20Factor%20Model%20Analysis%20of%20UK%20Asset%20Returns/Four%20Factor%20Analysis%20UK%20Asset%20Returns.pdf) (report, 14 pages), [`Exercise Four Factor Model.md`](04%20-%20Four%20Factor%20Model%20Analysis%20of%20UK%20Asset%20Returns/Exercise%20Four%20Factor%20Model.md) (task statement).

## 05 - Leverage Procyclicality in Chinese Financial Institutions

Analysis of leverage procyclicality for 158 listed Chinese financial institutions (banks, financial services, real estate finance) from Q4 2005 to Q4 2024, 12,166 firm-quarter observations, following the approach of Cincinelli et al. (2021). The report has three parts: data processing and descriptive statistics; panel regression on leverage procyclicality, mean reversion and market valuation effects; marginal effects by entity type and by sub-period, with interaction terms for crisis periods.

- **Main findings**: significant evidence of procyclical leverage, and commercial banks emerge as the main drivers of procyclicality.
- **Data**: [`Data set China.xlsx`](05%20-%20Leverage%20Procyclicality%20Analysis%20in%20Chinese%20Financial%20Institutions/Data%20set%20China.xlsx), a quarterly dataset with three sheets (banks, finance services, real estate finance services) and, for each firm, price, total assets, market value and market-to-book value.
- **Files**: [`Leverage Procyclicality China.pdf`](05%20-%20Leverage%20Procyclicality%20Analysis%20in%20Chinese%20Financial%20Institutions/Leverage%20Procyclicality%20China.pdf) (report, 9 pages), [`Exercise Leverage Procyclicality.md`](05%20-%20Leverage%20Procyclicality%20Analysis%20in%20Chinese%20Financial%20Institutions/Exercise%20Leverage%20Procyclicality.md) (task statement).

## 06 - Macro-Finance Paper Presentations

Two academic presentations, each based on a research paper.

- [`Central Banking For All.pdf`](06%20-%20Macro-Finance%20Papers%20Presentations/Central%20Banking%20For%20All.pdf) (20 slides): *Central Bank Digital Currency: Central Banking For All?* (Fernandez-Villaverde, Sanches, Schilling, Uhlig). It uses a Diamond-Dybvig banking model to study whether a central bank offering a CBDC to the public can replicate the optimal allocation, and what this implies for bank runs and the role of commercial banks.
- [`Monetary Policy and the Redistribution Channel.pdf`](06%20-%20Macro-Finance%20Papers%20Presentations/Monetary%20Policy%20and%20the%20Redistribution%20Channel.pdf) (18 slides): *Monetary Policy and the Redistribution Channel* (Auclert, American Economic Review, 2019), on redistribution as a transmission channel of monetary policy in a heterogeneous-agent setting.

## 07 - Python Notebooks: Stock Ranking and Risk Metrics

Three Python notebooks (NumPy, pandas) from the Coding for Finance course. Requirements: `numpy`, `pandas`, `matplotlib` and, for the first notebook, `yfinance`.

The data in these notebooks are used for illustration only (market data downloaded from Yahoo Finance in the first, public company figures in the second, simulated returns in the third): the notebooks show how the methods work and their results are not investment advice.

- [`topsis_vikor_ranking.ipynb`](07%20-%20Python%20-%20Stock%20Ranking%20and%20Risk%20Metrics/topsis_vikor_ranking.ipynb): classification of 20 US-listed stocks (Excellent, Good, Risky, Moderate, Avoid) from annualised return, volatility, Sharpe ratio and maximum drawdown, computed on 36 monthly returns downloaded from Yahoo Finance (September 2023 - September 2026), followed by TOPSIS and VIKOR multi-criteria rankings with a rank-correlation check and a sensitivity analysis on the criteria weights.
- [`composite_sharpe_ranking.ipynb`](07%20-%20Python%20-%20Stock%20Ranking%20and%20Risk%20Metrics/composite_sharpe_ranking.ipynb): ranking of five technology companies (NVIDIA, Meta, Netflix, Adobe, Intel) on FY2021-FY2025 fundamentals (revenue growth, operating margin, ROA, EPS, debt-to-equity), with min-max normalisation and a composite Sharpe-style score whose dispersion term uses only the criteria with a complete yearly series. It includes robustness checks on the weights and on the debt-to-equity criterion, and documents the data limitations.
- [`risk_metrics_stochastic_dominance.ipynb`](07%20-%20Python%20-%20Stock%20Ranking%20and%20Risk%20Metrics/risk_metrics_stochastic_dominance.ipynb): screening tool that extends classical return/risk measures with Sortino ratio, CAPM alpha and Treynor ratio, tests first- and second-order stochastic dominance against the market, and combines everything into a 7-class classification of 20 stocks. Betas and trailing 1-year returns are real; the 36 monthly return series are simulated from a single-factor model calibrated on them, so the results illustrate the method and are not a verdict on the individual stocks.

---

## Data

The input datasets of projects 01 and 02 are not redistributed: each project has a `data/README.md` that describes the expected files and columns. To regenerate a report, place the files in the project's `data/` folder and knit the `.Rmd` file (R Markdown, `github_document` output).

Projects 04 and 05 include the datasets used for the course assignments (`First_Assignment_dataset.xlsx` and `Data set China.xlsx`). The notebook `topsis_vikor_ranking.ipynb` (project 07) downloads its own market data from Yahoo Finance the first time it runs and keeps a local copy in `data/`, which is not tracked by git.

## Repository structure

```text
.
├── README.md
├── 01 - Credit Default Prediction - Classification Model Benchmark/
├── 02 - Asset Pricing - Risk Analysis in R/
├── 03 - Hedging and Portfolio Optimization in Excel/
├── 04 - Four Factor Model Analysis of UK Asset Returns/
├── 05 - Leverage Procyclicality Analysis in Chinese Financial Institutions/
├── 06 - Macro-Finance Papers Presentations/
└── 07 - Python - Stock Ranking and Risk Metrics/
```
