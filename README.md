# bayesian-optimisation-bt
Bayesian optimisation for cointegration-based mean reversion: from data import to Johansen tests and trading rules. (Work In Progress)

# Bayesian Optimisation for Cointegration-Based Mean Reversion (WIP)

This repository contains an ongoing research project exploring whether **Bayesian optimisation** can improve the **out-of-sample performance** of cointegration-based mean reversion strategies.

Classical cointegration tests (like the Johansen test) often look great **in-sample**, but trading performance tends to deteriorate **out-of-sample**. The core question here is:

> Can a cointegration-based mean reversion strategy be systematically tuned with Bayesian optimisation to improve out-of-sample robustness?

I’m still new to Bayesian data analysis, so this project is very much a **“learn by doing”** exercise. Suggestions, criticism, and collaboration are welcome.

---

## Repository Structure

The project currently lives in three Jupyter notebooks:

- **`data.ipynb`**  
  - Import price data (stocks/ETFs).  
  - Basic cleaning and preprocessing.  
  - Split into train / test segments.

- **`stat_tests.ipynb`**  
  - Run **ADF tests** to check integration order of individual series.  
  - Apply the **Johansen cointegration test**.  
  - Inspect eigenvalues, trace and max-eigen statistics, and cointegration ranks.

- **`johansen_trading.ipynb`**  
  - Use Johansen cointegration vectors to construct spreads.  
  - Build a simple mean-reversion trading rule on the spread (e.g. z-score thresholds).  
  - Train and test the strategy on separate segments (currently simple split, not rolling/expanding windows yet).  


As the project evolves, these will likely be refactored into reusable Python modules.
