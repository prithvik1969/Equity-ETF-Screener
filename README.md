# Equity-ETF-Screener
Equity &amp; ETF Screener – Python-based medium-term screening tool for NSE stocks and ETFs, integrating factor models with technical and fundamental indicators. Backtested over 5 years to outperform the NIFTY index by 23% CAGR, enabling data-driven portfolio allocation aligned with investment objectives and risk parameters.

\documentclass[11pt]{article}
\usepackage[margin=1in]{geometry}
\usepackage{lmodern}
\usepackage[T1]{fontenc}
\usepackage{microtype}
\usepackage{hyperref}
\usepackage{parskip}
\usepackage{listings}
\lstset{basicstyle=\ttfamily\small,breaklines=true}

\title{\Large\bfseries Equity \& ETF Screener \\ \normalsize Medium-term NSE Screener}
\author{Prithvi Kewalramani \\ (Developed during engagement at Pantomath Capital)}
\date{}

\begin{document}
\maketitle

\begin{abstract}
\noindent
\textbf{Python-based medium-term screening framework for NSE equities and ETFs.}
This project combines multi-factor modelling with technical and fundamental indicators to generate investable lists and portfolio weightings. Backtested over a configurable 5-year window, the screener produced an outperformance versus the NIFTY index of approximately \(\sim 23\%\) CAGR over the tested period.
\end{abstract}

\section*{Key features}
\begin{itemize}
  \item \textbf{Multi-factor architecture:} Supports custom factor definitions (momentum, value, quality, etc.) and flexible factor blending.
  \item \textbf{Hybrid signals:} Integrates technical indicators (moving averages, ATR, momentum) with fundamental metrics (P/E, ROE, earnings growth).
  \item \textbf{Backtesting \& walk-forward evaluation:} Configurable windows to assess robustness across market regimes.
  \item \textbf{Portfolio construction:} Rank-based selection and configurable weighting schemes with risk constraints.
  \item \textbf{Modular, reproducible codebase:} Clear separation of data ingestion, factor computation, signal engine, backtest logic, and reporting.
  \item \textbf{Exportable outputs:} Ranked lists, performance summaries, trade-level logs and diagnostic plots for downstream decision-making.
\end{itemize}

\section*{Technical overview}
\begin{itemize}
  \item \textbf{Language:} Python.
  \item \textbf{Typical libraries:} \texttt{pandas}, \texttt{numpy}, \texttt{scikit-learn} (for scaling/modeling), backtesting utilities, plotting libraries (see \texttt{requirements.txt}).
  \item \textbf{Inputs:} Historical price series, ETF constituents, and fundamental data (CSV or configurable data sources).
  \item \textbf{Outputs:} Ranked asset lists, periodic portfolio P\&L, performance metrics, and visual diagnostics (equity curve, factor exposures).
\end{itemize}

\section*{Backtest \& performance}
\begin{itemize}
  \item \textbf{Backtest period:} Default 5 years (fully configurable).
  \item \textbf{Primary result:} Outperformed NIFTY by \(\sim 23\%\) CAGR over the test window (detailed methodology, assumptions and trade logs included in the backtest notebook).
  \item \textbf{Metrics evaluated:} CAGR, max drawdown, Sharpe ratio, turnover, and alignment with client risk parameters.
\end{itemize}

\section*{Quick start}
\begin{enumerate}
  \item Clone the repository:
\begin{lstlisting}
git clone <repo-url>
cd equity-etf-screener
\end{lstlisting}
  \item Create an environment and install dependencies:
\begin{lstlisting}
python -m venv venv
source venv/bin/activate   # Windows: venv\Scripts\activate
pip install -r requirements.txt
\end{lstlisting}
  \item Add data: place historical price and fundamentals CSVs in \texttt{data/} (example templates provided).
  \item Run the example notebook to reproduce the backtest and generate reports (open \texttt{notebooks/backtest\_example.ipynb}).
\end{enumerate}

\section*{Repository layout (suggested)}
\begin{description}
  \item[\texttt{notebooks/}] Interactive backtests and analysis notebooks.
  \item[\texttt{screener/}] Core modules: data ingestion, factor builders, signal engine, portfolio constructor.
  \item[\texttt{data/}] Sample datasets and input templates.
  \item[\texttt{reports/}] Generated performance reports and plots.
  \item[\texttt{requirements.txt}] Exact package versions for reproducibility.
\end{description}

\section*{Why this screener?}
Designed for practical portfolio decision-making: it converts raw price and fundamental inputs into ranked, risk-aware selections that portfolio managers and analysts can action. The modular design allows easy extension (new factors, weighting schemes, alternate data feeds).

\section*{Contributing \& contact}
Contributions welcome — open an issue or PR. For questions or to reproduce results, contact: \texttt{prithvik1969} (GitHub) or \texttt{prithvik1969@gmail.com}.

\vfill
\noindent\small\textit{Note: Performance figures reproduce internal backtests used during the Pantomath engagement. See the backtest notebook for methodology, parameter choices, and limitations.}

\end{document}
