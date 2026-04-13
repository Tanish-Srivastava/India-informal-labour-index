---
jupyter:
  kernelspec:
    display_name: Python 3
    language: python
    name: python3
  language_info:
    codemirror_mode:
      name: ipython
      version: 3
    file_extension: .py
    mimetype: text/x-python
    name: python
    nbconvert_exporter: python
    pygments_lexer: ipython3
    version: 3.14.3
  nbformat: 4
  nbformat_minor: 5
---

::: {#fb46bdcc .cell .markdown}
# Data Download Instructions

The raw PLFS Excel files that power this project are published by the
Ministry of Statistics and Programme Implementation (MoSPI) and must be
downloaded directly from their website. They are not included in this
repository.

------------------------------------------------------------------------

## PLFS Annual Reports

**Website:** <https://mospi.gov.in/publications-reports>

Search for \"PLFS\" and download the Annual Report for each of the three
years below. Each report has a separate Excel download for its Appendix
A tables. Download the individual table files listed and rename them
exactly as shown.

------------------------------------------------------------------------

### Year: 2022-23 (July 2022 -- June 2023) {#year-2022-23-july-2022--june-2023}

Place files in: `PLFS 22-23 tables/`

  --------------------------------------------------------------------------------
  File name to save as             Table number in report  Contents
  -------------------------------- ----------------------- -----------------------
  `PLFS 22-23 LFPR.xlsx`           Table 6                 Labour Force
                                                           Participation Rate by
                                                           state, usual status

  `PLFS 22-23 WPR.xlsx`            Table 7                 Worker Population Ratio
                                                           by state, usual status

  `PLFS 22-23 EMP STATUS.xlsx`     Table 9                 Employment status
                                                           distribution by state

  `PLFS 22-23 INDUSTRY.xlsx`       Table 16                Workers by industry
                                                           section (NIC-2008) by
                                                           state

  `PLFS 22-23 ENTERPRISE.xlsx`     Table 22                Workers by enterprise
                                                           type by state

  `PLFS 22-23 WAGE REGULAR.xlsx`   Table 24                Average monthly wage of
                                                           regular workers by
                                                           state

  `PLFS 22-23 WAGE CASUAL.xlsx`    Table 25                Average daily wage of
                                                           casual workers by state

  `PLFS 22-23 WAGE SELF.xlsx`      Table 26                Average monthly
                                                           earnings from
                                                           self-employment by
                                                           state

  `PLFS 22-23 HOURS.xlsx`          Table 28                Hours available for
                                                           additional work by
                                                           state
  --------------------------------------------------------------------------------

------------------------------------------------------------------------

### Year: 2023-24 (July 2023 -- June 2024) {#year-2023-24-july-2023--june-2024}

Place files in: `PLFS 23-24 tables/`

  --------------------------------------------------------------------------------
  File name to save as             Table number in report  Contents
  -------------------------------- ----------------------- -----------------------
  `PLFS 23-24 LFPR.xlsx`           Table 16.0              Labour Force
                                                           Participation Rate by
                                                           state, usual status

  `PLFS 23-24 WPR.xlsx`            Table 17.0              Worker Population Ratio
                                                           by state, usual status

  `PLFS 23-24 EMP STATUS.xlsx`     Table 19                Employment status
                                                           distribution by state

  `PLFS 23-24 INDUSTRY.xlsx`       Table 27                Workers by industry
                                                           section (NIC-2008) by
                                                           state

  `PLFS 23-24 ENTERPRISE.xlsx`     Table 35                Workers by enterprise
                                                           type by state

  `PLFS 23-24 WAGE REGULAR.xlsx`   Table 38                Average monthly wage of
                                                           regular workers by
                                                           state

  `PLFS 23-24 WAGE CASUAL.xlsx`    Table 39                Average daily wage of
                                                           casual workers by state

  `PLFS 23-24 WAGE SELF.xlsx`      Table 40                Average monthly
                                                           earnings from
                                                           self-employment by
                                                           state

  `PLFS 23-24 HOURS.xlsx`          Table 42                Hours available for
                                                           additional work by
                                                           state
  --------------------------------------------------------------------------------

------------------------------------------------------------------------

### Year: 2025 (January -- December 2025) {#year-2025-january--december-2025}

Place files in: `PLFS 25 tables/`

**Important note:** The 2025 PLFS uses a revamped sampling methodology
introduced from January 2025 onwards. MoSPI cautions against direct
comparison with earlier rounds. Table numbers in the 2025 report match
the 2023-24 numbering scheme.

  -----------------------------------------------------------------------------
  File name to save as          Table number in report  Contents
  ----------------------------- ----------------------- -----------------------
  `PLFS 25 LFPR.xlsx`           Table 16.0              Labour Force
                                                        Participation Rate by
                                                        state, usual status

  `PLFS 25 WPR.xlsx`            Table 17.0              Worker Population Ratio
                                                        by state, usual status

  `PLFS 25 EMP STATUS.xlsx`     Table 19                Employment status
                                                        distribution by state

  `PLFS 25 INDUSTRY.xlsx`       Table 27                Workers by industry
                                                        section (NIC-2008) by
                                                        state

  `PLFS 25 ENTERPRISE.xlsx`     Table 35                Workers by enterprise
                                                        type by state

  `PLFS 25 WAGE REGULAR.xlsx`   Table 38                Average monthly wage of
                                                        regular workers by
                                                        state

  `PLFS 25 WAGE CASUAL.xlsx`    Table 39                Average daily wage of
                                                        casual workers by state

  `PLFS 25 WAGE SELF.xlsx`      Table 40                Average monthly
                                                        earnings from
                                                        self-employment by
                                                        state

  `PLFS 25 HOURS.xlsx`          Table 42                Hours available for
                                                        additional work by
                                                        state
  -----------------------------------------------------------------------------

------------------------------------------------------------------------

## RBI GVA Data

**Website:** <https://rbi.org.in/Scripts/AnnualPublications.aspx>

Navigate to: Handbook of Statistics on Indian States

Under the State Domestic Product section, download: **Table 26: Gross
State Value Added (Constant Prices)**

Save as: `gva.xlsx` in the project root folder (not inside any
subfolder).

The notebook uses Sheet 2 (`T_26(ii)`) of this file, which covers states
not in Sheet 1 and includes the years 2017-18 through 2024-25.

------------------------------------------------------------------------

## NREGA Job Card Data

**Website:** <https://nrega.nic.in>

Navigate to: Reports → R1. Beneficiary Detail →

1.  Job Card Related Reports →
2.  Category wise Household/Workers

Download the state-wise report for the current financial year. Save as:
`nrega.xlsx` in the project root folder.

The notebook uses Column D (Issued job cards, in lakhs) from this file.

------------------------------------------------------------------------

## Literacy Data

The file `Table29.6-States.xlsx` is included in this repository. It
contains state-level literacy rates from the PLFS 2022-23 Annual Report,
Table 29.6. No download is needed for this file.

------------------------------------------------------------------------

## Notes on File Naming

The notebook identifies files by their exact names. If you rename a file
differently from the convention above, update the `FILES` dictionary and
`YEARS` dictionary in Cell 5 of the notebook to match.

The notebook was built and tested on Python 3.14 on Windows. File paths
use raw strings (`r"..."`) to handle backslashes. If running on Mac or
Linux, replace backslashes with forward slashes in the `BASE` path in
Cell 1.
:::

::: {#f6f320b0 .cell .code}
``` python
```
:::
