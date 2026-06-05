# Data Download Instructions

The raw PLFS Excel files that power this project are published by the
Ministry of Statistics and Programme Implementation (MoSPI) and must
be downloaded directly from their website. They are not included in
this repository.

---

## PLFS Annual Reports

**Website:** https://mospi.gov.in/publications-reports

Search for "PLFS" and download the Annual Report for each year below.
Rename files exactly as shown and place in the correct folder.

---

### Year: 2022-23 — Place files in `PLFS 22-23 tables/`

| File name | Table number | Contents |
|---|---|---|
| `PLFS 22-23 LFPR.xlsx` | Table 6 | Labour Force Participation Rate by state |
| `PLFS 22-23 WPR.xlsx` | Table 7 | Worker Population Ratio by state |
| `PLFS 22-23 EMP STATUS.xlsx` | Table 9 | Employment status distribution by state |
| `PLFS 22-23 INDUSTRY.xlsx` | Table 16 | Workers by industry section (NIC-2008) |
| `PLFS 22-23 ENTERPRISE.xlsx` | Table 22 | Workers by enterprise type by state |
| `PLFS 22-23 WAGE REGULAR.xlsx` | Table 24 | Average monthly wage of regular workers |
| `PLFS 22-23 WAGE CASUAL.xlsx` | Table 25 | Average daily wage of casual workers |
| `PLFS 22-23 WAGE SELF.xlsx` | Table 26 | Average monthly earnings from self-employment |
| `PLFS 22-23 HOURS.xlsx` | Table 28 | Hours available for additional work |

---

### Year: 2023-24 — Place files in `PLFS 23-24 tables/`

| File name | Table number | Contents |
|---|---|---|
| `PLFS 23-24 LFPR.xlsx` | Table 16.0 | Labour Force Participation Rate by state |
| `PLFS 23-24 WPR.xlsx` | Table 17.0 | Worker Population Ratio by state |
| `PLFS 23-24 EMP STATUS.xlsx` | Table 19 | Employment status distribution by state |
| `PLFS 23-24 INDUSTRY.xlsx` | Table 27 | Workers by industry section (NIC-2008) |
| `PLFS 23-24 ENTERPRISE.xlsx` | Table 35 | Workers by enterprise type by state |
| `PLFS 23-24 WAGE REGULAR.xlsx` | Table 38 | Average monthly wage of regular workers |
| `PLFS 23-24 WAGE CASUAL.xlsx` | Table 39 | Average daily wage of casual workers |
| `PLFS 23-24 WAGE SELF.xlsx` | Table 40 | Average monthly earnings from self-employment |
| `PLFS 23-24 HOURS.xlsx` | Table 42 | Hours available for additional work |

---

### Year: 2025 — Place files in `PLFS 25 tables/`

**Note:** The 2025 PLFS uses a revamped sampling methodology introduced
from January 2025. MoSPI cautions against direct comparison with earlier
rounds. Table numbers match the 2023-24 scheme.

| File name | Table number | Contents |
|---|---|---|
| `PLFS 25 LFPR.xlsx` | Table 16.0 | Labour Force Participation Rate by state |
| `PLFS 25 WPR.xlsx` | Table 17.0 | Worker Population Ratio by state |
| `PLFS 25 EMP STATUS.xlsx` | Table 19 | Employment status distribution by state |
| `PLFS 25 INDUSTRY.xlsx` | Table 27 | Workers by industry section (NIC-2008) |
| `PLFS 25 ENTERPRISE.xlsx` | Table 35 | Workers by enterprise type by state |
| `PLFS 25 WAGE REGULAR.xlsx` | Table 38 | Average monthly wage of regular workers |
| `PLFS 25 WAGE CASUAL.xlsx` | Table 39 | Average daily wage of casual workers |
| `PLFS 25 WAGE SELF.xlsx` | Table 40 | Average monthly earnings from self-employment |
| `PLFS 25 HOURS.xlsx` | Table 42 | Hours available for additional work |

---

## RBI GVA Data

**Website:** https://rbi.org.in/Scripts/AnnualPublications.aspx

Navigate to: Handbook of Statistics on Indian States. Download
**Table 26: Gross State Value Added (Constant Prices)**.

Save as `gva.xlsx` in the project root folder. The notebook uses
Sheet 2 (`T_26(ii)`) covering years 2017-18 through 2024-25.

---

## NREGA Job Card Data

**Website:** https://nrega.nic.in

Navigate to: Reports → R1 → Job Card Related Reports →
Category wise Household/Workers.

Download the state-wise report and save as `nrega.xlsx` in the
project root folder. The notebook uses Column D (issued job cards
in lakhs).

---

## Literacy Data

`Table29.6-States.xlsx` is included in this repository.
No download needed.

---

## File Naming Notes

The notebook identifies files by exact name. If you rename anything
update the `FILES` dictionary in Cell 5 of the notebook to match.

Built and tested on Python 3.14 on Windows. If running on Mac or
Linux replace backslashes with forward slashes in the `BASE` path
in Cell 1.