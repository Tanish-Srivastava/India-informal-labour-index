# Regression Results

All regressions use cross-sectional OLS on state-level averages
across PLFS 2022-23, 2023-24, and 2025 (N=27 states).

## Files

- `main_regression.txt` : primary specification with HC1 robust
  standard errors (N=27)
- `robustness_northeast_exclusion.txt` : robustness check excluding
  Northeast states and small UTs (N=16)
- `robustness_population_weighted.txt` : robustness check using
  population-weighted WLS (N=27)

## Key Finding

Per capita GVA significantly reduces SII (p=0.005) but has no effect
on EGI (p=0.91). Agricultural share significantly increases EGI
(p=0.005) but does not worsen SII. This dimensional asymmetry holds
across all three specifications:

| Specification | GVA on SII | Agri on EGI |
|---|---|---|
| Main (N=27, HC1) | -14.69 (p=0.005) *** | +1.25 (p=0.005) *** |
| Excl. Northeast (N=16) | -26.05 (p<0.001) *** | +0.86 (p=0.001) *** |
| Population-weighted (N=27) | -17.19 (p=0.002) *** | +0.74 (p<0.001) *** |
