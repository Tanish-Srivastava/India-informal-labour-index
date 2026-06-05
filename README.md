# Informal Labour Market Stress Index (ILMSI)
### A Two-Dimensional State-Level Analysis of Informal Worker 
### Vulnerability in India | PLFS 2022-23, 2023-24, and 2025

---

## Overview

Standard macroeconomic indicators like GDP and GVA say little about
conditions faced by the roughly 90% of India's workforce employed
informally. This project constructs two complementary indices of
informal labour vulnerability for 32 Indian states across three
PLFS survey years, and tests what macroeconomic forces drive each.

1) **Earnings Gap Index (EGI)**

measures the wage penalty for being informal. Built from:
 - `wage_precarity`: ratio of regular monthly wages to casual monthly wages (casual daily wage × 30)
 - `self_reg_ratio`: ratio of regular monthly wages to self-employment earnings

2) **Structural Informality Index (SII)** 

measures how informal the labour market structure itself is. Built from:
- `casual_share`: share of workers in casual employment
- `informality`: share of workers in proprietary/partnership enterprises (MoSPI/NCEUS operational definition)

Both indices are constructed via Principal Component Analysis and
rescaled to 0-100. Higher scores indicate greater stress.

---

## Key Finding

The two dimensions of informal labour vulnerability respond to
**different macroeconomic forces**:

| Predictor | Effect on SII | Effect on EGI |
|---|---|---|
| Per capita GVA | **-14.69 (p=0.005)** | -0.44 (p=0.91) |
| Agricultural share | -0.97 (p=0.085) | **+1.25 (p=0.005)** |

Economic development reduces structural informality but does not
narrow the formal-informal earnings gap. Agricultural dependence
widens the earnings gap but does not worsen structural informality.
Both findings hold across three robustness specifications.

---

## Data Sources

| Source | Used For |
|---|---|
| PLFS Annual Reports 2022-23, 2023-24, 2025 (MoSPI) | All index variables |
| RBI Handbook of Statistics, Table 26 | Per capita GVA |
| PLFS Table 29.6 | State literacy rates |
| Census 2011 | Urbanisation and population |

Raw PLFS files are not included. See `Data/README.md` for download
instructions and exact table numbers.

---

## Methodology

Nine PLFS tables extracted per year across 32 states. Four variables
engineered and split into two sub-indices via separate PCA runs.
Cross-sectional OLS on 27-state averages with HC1 robust standard
errors. Robustness checks: sample exclusion of Northeast states and
small UTs (N=16, R²=0.73), population-weighted WLS (N=27, R²=0.64).

---

## Repository Structure

**Notebook**
- `PLSF Project - Main.ipynb` : full pipeline from data extraction to regression

**Data Files**
- `plfs_master_panel.csv` : panel dataset, approximately 96 state-year observations
- `plfs_ilmsi.csv` : final EGI and SII scores per state and year
- `gva.xlsx` : RBI Handbook Table 26, Gross State Value Added at constant prices
- `Table29.6-States.xlsx` : PLFS state-level literacy rates

**Outputs**
- `egi_sii_trendlines.png` : main figure: EGI vs SII quadrant scatter, three years
- `egi_sii_bars.png` : EGI and SII scores side by side for all 27 states
- `egi_sii_by_year.png` : state movement across three PLFS rounds

**Data Documentation**
- `Data/README.md` : download instructions and exact table numbers for all raw files
## How to Reproduce

1. Clone this repository
2. Download PLFS tables per `Data/README.md`
3. Update `BASE` path in Cell 1 of the notebook
4. Run notebook top to bottom
pip install pandas numpy scikit-learn statsmodels
matplotlib scipy openpyxl linearmodels

---

*Data: MoSPI Periodic Labour Force Survey. RBI Handbook of Statistics on Indian States. Census 2011, Office of the Registrar General.*

*Independent academic research. Not affiliated with or endorsed by MoSPI or RBI.*
