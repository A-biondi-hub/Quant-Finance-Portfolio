# Quant Finance Portfolio — Selected Notebooks

Three self-contained analyses from a quantitative finance coursework track, selected because each goes beyond applying a single formula and requires an independent methodological choice.

### [`EX7_sharpe_ratio_ranking.ipynb`](./EX7_sharpe_ratio_ranking.ipynb) — Financial Decision Making Using a Sharpe-Style Ratio
Ranks 5 tech companies on 5 real financial criteria (FY2021–2025) by combining a normalized return score with its own dispersion into a Sharpe-style risk-adjusted ranking. Shows why NVIDIA's best-in-class average performance still loses to Adobe once volatility is priced in.

### [`EX11_stochastic_dominance.ipynb`](./EX11_stochastic_dominance.ipynb) — Advanced Market Analysis: Risk Metrics & Stochastic Dominance
A 20-stock screening tool combining Sharpe, Sortino, Alpha, Treynor and formal First/Second-Order Stochastic Dominance tests into a 7-tier classification. Completes an intentionally incomplete starting template (undefined data, an empty loop) with a real-data-anchored simulation and an explicit fix for a division-by-zero edge case in the Sortino ratio.

### [`EX3_topsis_vikor_ranking.ipynb`](./EX3_topsis_vikor_ranking.ipynb) — Multi-Factor Investment Classification with TOPSIS and VIKOR
Classifies 20 real stocks (Return, Risk, Sharpe, Mean-Variance score) with a rule-based system, then cross-checks the ranking with two independent multi-criteria methods, TOPSIS and VIKOR, to see whether they agree on the top pick.

---
All three use real, sourced market data (ChartRow / SEC filings / stockanalysis.com, as cited inline), with data-availability limitations flagged explicitly rather than silently filled in. Built with NumPy and pandas.
