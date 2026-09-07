# SimuQuant Showroom

## Overview
A showcase repository for **SimuQuant**, a proprietary quantitative trading and simulation framework written in Python. While the core algorithmic engine remains private to protect institutional-grade proprietary strategies, this public workspace highlights the architecture, visualization standards, and analytical depth of the project. SimuQuant represents a comprehensive Monte Carlo simulation suite focused on multi-layered statistical validation for advanced equity and derivative strategies.

![SimuQuant Front Page](assets/SimuQuant_FrontPage.png)

---

## Key Architecture & Pipeline
* **Automated Data Ingestion:** Daily cron-scheduled dispatchers pull, clean, and normalize end-of-day historical time-series data directly from Yahoo Finance (`data/quality/`).
* **Low-Layer Brute Force Engine:** High-performance computational layers process raw market data to execute exhaustive combinatorial searches across historical price matrices (`asim/layer2_advanced_simulation/`).
* **Mid-Layer Cluster Recognition:** Unsupervised machine learning models and clustering algorithms categorize market regimes, volatility states, and structural breaks (`asim/layer3_insight_engine/`).
* **High-Layer Monte Carlo Simulations:** The apex layer executes millions of path-dependent simulation iterations to stress-test specific trading hypotheses.

## Development Workflow & Governance
To maintain production-grade reliability and architectural integrity, SimuQuant adheres to a strict branching and code review workflow:
* **Feature/Dev Branches:** All iterative updates, refactoring, and algorithmic adjustments are developed locally on isolated feature or development branches (`dev/*`).
* **Pull Request (PR) Gatekeeping:** Changes cannot be pushed directly to the `main` branch. Every modification requires a formal Pull Request targeting `main`.
* **Self-Approval & Quality Gates:** PRs undergo internal review and validation against unit test suites (`pytest`) before receiving approval and being merged into the production branch.

### Dispatcher & CLI Control
![Dispatcher Menu Part 1](assets/SimuQuant_HelpMenu_1.png)
![Dispatcher Menu Part 2](assets/SimuQuant_HelpMenu_2.png)

---

## Core Quantitative Modules
* **Seasonality Profiling:** Multi-factor temporal decomposition isolating recurring calendar anomalies, intraday-to-interday drift, and cyclical momentum shifts (`asim/seasonality/`).
* **Buy-on-Dip Optimization:** Stochastic modeling of drawdown thresholds, dynamic entry triggers, and recovery probability distributions across varied market regimes (`asim/timing/`).
* **Position Sizing Frameworks:** Comparative analytical implementations of Kelly Criterion, Optimal f, volatility-parity scaling, and dynamic risk-budgeting models (`asim/money_manager/`).

![Analytical Figures](assets/SimuQuant_Figures.png)

---

## Visualization Standards & Engineering Highlights
* **Bloomberg-Style Aesthetics:** Custom-styled matplotlib and seaborn visual outputs mimicking terminal-grade data density, featuring high-contrast dark backgrounds (`#0e1117` / terminal black), monospaced typography, and precise grid layouts tailored for professional risk presentation (`utils/insights/timing_mc_plots.py`).
* **Rigorous Testing Standards:** Full `pytest` integration covering over 1,000 unit and integration tests for end-to-end signal pipelines, data integrity checks, and regression tests (`test/`).

![Test Suite Overview](assets/SimuQuant_Tests.png)

### Risk & Macro Monitoring
![Stress Scenario Monitor](assets/SimuQuant_StressSzenario_Reminder_To_Monitor.png)

### Money Management Monte Carlo Simulations Across Multiple Symbols
```text
Top 2 Test Results per Symbol:

Symbol: [REDACTED_ASSET_1]

Rank 1
Symbol                                          [REDACTED_ASSET_1]
Model                                           Volatility-Based
Kelly-Fraction                                              0.04
Initial_Capital                                         100000.0
Avg_Ending_Capital                                    202933.68
Std_Ending_Capital                                     41917.97
Sharpe_Ratio                                           2.455605
Sharpe_Ratio_Annualized                                 2.76825
Avg_Max_Drawdown                                      19776.24
Worst_Max_Drawdown                                    44575.05
AvgProfit_MaxDD                                      10.261449
AvgProfit_WorstMaxDD                                  4.552629
Range_Ending_Capital                                       NaN
Robustness                                                 1.0
Rating                                                    HIGH
Risk_per_Trade_Currency                                4000.00
Risk_Comment                   ≈ 4.0% Risk at 100,000.0 € Capital

Rank 2
Symbol                                          [REDACTED_ASSET_1]
Model                                           Volatility-Based
Kelly-Fraction                                              0.02
Initial_Capital                                         100000.0
Avg_Ending_Capital                                    150707.24
Std_Ending_Capital                                     18229.46
Sharpe_Ratio                                           2.781612
Sharpe_Ratio_Annualized                                2.597725
Avg_Max_Drawdown                                      12168.21
Worst_Max_Drawdown                                    27446.42
AvgProfit_MaxDD                                       12.38532
AvgProfit_WorstMaxDD                                  5.490959
Range_Ending_Capital                                       NaN
Robustness                                                 1.0
Rating                                                    HIGH
Risk_per_Trade_Currency                                2000.00
Risk_Comment                   ≈ 2.0% Risk at 100,000.0 € Capital

Symbol: [REDACTED_ASSET_2]

Rank 16
Symbol                                          [REDACTED_ASSET_2]
Model                                                      VaR 95%
Kelly-Fraction                                           16.042133
Initial_Capital                                         100000.0
Avg_Ending_Capital                                    202905.90
Std_Ending_Capital                                     19690.31
Sharpe_Ratio                                           5.232502
Sharpe_Ratio_Annualized                                5.803145
Avg_Max_Drawdown                                       5392.42
Worst_Max_Drawdown                                    15999.20
AvgProfit_MaxDD                                      37.651584
AvgProfit_WorstMaxDD                                 12.689615
Range_Ending_Capital                                       NaN
Robustness                                                 1.0
Rating                                                    HIGH
Risk_per_Trade_Currency                                2000.00
Risk_Comment                   ≈ 2.0% Risk at 100,000.0 € Capital

Rank 17
Symbol                                          [REDACTED_ASSET_2]
Model                                                      VaR 99%
Kelly-Fraction                                           16.042133
Initial_Capital                                         100000.0
Avg_Ending_Capital                                    202681.82
Std_Ending_Capital                                     19702.82
Sharpe_Ratio                                           5.217794
Sharpe_Ratio_Annualized                                 5.82566
Avg_Max_Drawdown                                       5554.40
Worst_Max_Drawdown                                    16999.98
AvgProfit_MaxDD                                      36.513402
AvgProfit_WorstMaxDD                                 11.929989
Range_Ending_Capital                                       NaN
Robustness                                                 1.0
Rating                                                    HIGH
Risk_per_Trade_Currency                                2000.00
Risk_Comment                   ≈ 2.0% Risk at 100,000.0 € Capital
```

---

## Project Tree
```text
SimuQuant-Showroom/
├── asim/                    # Core multi-layered simulation & insight engines
│   ├── layer2_advanced_simulation/ # Brute-force parameter sweeps & MC variants
│   ├── layer3_insight_engine/      # Regime clustering & statistical analyzers
│   ├── money_manager/              # Position sizing (Dynamic/Static risk models)
│   ├── reporting_center/           # Bloomberg-style dashboards & HTML reporting
│   ├── seasonality/                # Temporal decomposition & cycle scouts
│   └── market-timing-analysis/     # Tactical entry triggers & regime timing
├── config/                  # YAML-based environment & symbol configurations
├── data/                    # Automated ETL, cleaning, gap-scanning & diagnostics
├── products/                # Strategy deployment products (Alpha 1 & 2)
├── test/                    # Comprehensive unit & integration test suites (PyTest)
└── utils/                   # Shared utilities, grid search, & visualization engines
```

Disclaimer: The implementation details, optimization layers, vectorization methods, and proprietary position-sizing/Monte Carlo execution models contained in the private repository are strictly confidential. This showroom is intended solely for portfolio and recruitment evaluation.