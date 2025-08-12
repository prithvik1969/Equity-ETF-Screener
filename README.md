# Equity-ETF-Screener
Equity &amp; ETF Screener – Python-based medium-term screening tool for NSE stocks and ETFs, integrating factor models with technical and fundamental indicators. Backtested over 5 years to outperform the NIFTY index by 23% CAGR, enabling data-driven portfolio allocation aligned with investment objectives and risk parameters.


Nice — here’s a longer, GitHub-ready README-style description you can drop into your repo. I kept it professional, clear, and aligned with the resume text while adding useful sections (features, tech, usage, backtest notes) so a reviewer or recruiter immediately understands what the project does and how to run it.

# Equity & ETF Screener — Medium-term NSE Screener

**Python-based medium-term screening framework for NSE equities and ETFs.**
Combines multi-factor modelling with technical and fundamental indicators to generate investable lists and portfolio weightings. Built and backtested during my time at Pantomath Capital, the screener was validated on 5 years of historical data and produced a net outperformance versus the NIFTY index of **+23% CAGR** over the test period.

---

## Key features

* Multi-factor architecture — supports custom factor definitions (e.g., momentum, value, quality) and factor blending.
* Hybrid signals — integrates both technical indicators (e.g., moving averages, ATR, momentum) and fundamental metrics (e.g., P/E, ROE, earnings growth).
* Backtesting & walk-forward evaluation — configurable backtest windowing to assess robustness over multiple market regimes.
* Portfolio construction — rank-based selection and configurable weighting schemes with risk parameter constraints to align with client objectives.
* Modular, reproducible codebase — clear separation of data ingestion, factor calculation, signal construction, backtest engine, and reporting.
* Exportable results — generates performance summaries, selection lists, and trade-level logs for downstream portfolio decision-making.

---

## Technical overview

* Language: Python
* Typical libraries used: pandas, numpy, scikit-learn (for factor scaling and modelling), backtesting utilities, and plotting for diagnostics. (See `requirements.txt` for exact dependencies.)
* Inputs: historical price series, ETF constituents, and fundamental data (configurable data sources / CSV import).
* Outputs: ranked stock/ETF lists, daily/periodic portfolio P\&L, performance metrics, and visual diagnostics (equity curve, factor exposures).

---

## Backtest & performance

* Backtest period: 5 years (configurable).
* Primary result: outperformed NIFTY by **\~23% CAGR** over the tested window (details, assumptions, and trade-level logs included in the backtest notebook).
* Evaluation focuses on CAGR, drawdown, turnover, and alignment to client risk parameters (customizable).

> Note: performance numbers shown in the repository reproduce the internal backtest used during the Pantomath engagement; please refer to the backtest notebook for methodology, parameter choices, and limitations.

---

## Quick start

1. Clone the repo:

   ```bash
   git clone <repo-url>
   cd equity-etf-screener
   ```
2. Create a Python environment and install dependencies:

   ```bash
   python -m venv venv
   source venv/bin/activate   # or `venv\Scripts\activate` on Windows
   pip install -r requirements.txt
   ```
3. Populate `data/` with historical price and fundamentals CSVs (example files and format are provided).
4. Run the example notebook to reproduce the backtest and generate reports:

   ```bash
   jupyter lab
   # open notebooks/backtest_example.ipynb
   ```

---

## Repository layout (suggested)

* `notebooks/` — interactive backtests and analysis notebooks (recommended starting point).
* `screener/` — core modules: data ingestion, factor builders, signal engine, portfolio constructor.
* `data/` — sample datasets and input templates.
* `reports/` — generated performance reports and charts.
* `requirements.txt` — exact package versions for reproducibility.

---

## Why this screener?

Built for practical portfolio decision-making: it converts raw price and fundamental data into ranked, risk-aware selections that portfolio managers can act on. The modular design makes it straightforward to add new factors, change weighting schemes, or plug in alternate data sources.

---

## Contributing & contact

Contributions and improvements welcome — open an issue or PR. For questions or to reproduce the Pantomath results, contact: `prithvik1969` (GitHub) or [prithvik1969@gmail.com](mailto:prithvik1969@gmail.com).

---

Would you like this converted into a ready-to-save `README.md` file (I can generate the file content for you), or tailored to a slightly more technical audience (add code snippets and exact factor formulas)?
