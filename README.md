# Diagnosing a Flawed Risk Model — VaR, Expected Shortfall & Monte Carlo

## Objective

In this lab, I tested a risk model and compared different ways to measure portfolio risk.

## Methodology

- Checked a normal-distribution VaR model and compared it with historical returns.
- Calculated VaR and Expected Shortfall using Normal, Student-t, and Historical methods.
- Fitted a Student-t distribution with degrees of freedom of 4.58.
- Compared standard Monte Carlo simulation with antithetic variates.
- Used the `risk_metrics.py` module to calculate VaR and ES and ran its self-tests.
- Used AI to create a VaR backtest, revised the prompt, and checked the result with my own calculation.

## Key Findings

- The normal model understated the 99% historical VaR by 12.7%, or about $40,393 on a $10 million portfolio.
- The Student-t method captured the fat tails better than the normal model.
- Antithetic variates reduced the standard error by a factor of 1.26.
- The normal 99% VaR was breached on 1.71% of days, which is higher than the expected 1%.
