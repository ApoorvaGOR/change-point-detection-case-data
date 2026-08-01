# Hurricane Nicholas Power Outage Data

This folder contains the county-level power outage time series used in the teaching case:

> **When Linear Regression Isn't Enough: Building Optimization Models for Change-Point Detection and Trend Analysis**

The dataset is used to demonstrate **multidimensional continuous piecewise-linear fitting with shared change-points**, where each county has its own outage trajectory while all counties share a common set of change-point locations. This example is discussed in Section 3.1 of the accompanying teaching case.

## File

### `Hurricane_Nicholas_Power_Outage_Data.xlsx`

This workbook contains county-level power outage time series for the period

**September 14, 2021 – September 18, 2021 (end of day)**

recorded at **15-minute intervals**.

Each row corresponds to one Texas county, and each column (after the first) represents the **total number of customers without electric power** at a particular 15-minute timestamp.

## Data Description

The first column contains the county **FIPS code**, while the remaining columns contain the outage counts over time.

**FIPS (Federal Information Processing Standards)** codes are unique five-digit identifiers assigned by the U.S. federal government to counties and county-equivalent administrative regions. For Texas counties, the first two digits (`48`) denote the state of Texas, while the remaining three digits uniquely identify the county.

The dataset contains outage trajectories for the following twelve Texas counties:

| FIPS | County |
|------:|----------------|
| 48015 | Austin County |
| 48039 | Brazoria County |
| 48071 | Chambers County |
| 48089 | Colorado County |
| 48157 | Fort Bend County |
| 48167 | Galveston County |
| 48201 | Harris County |
| 48291 | Liberty County |
| 48321 | Matagorda County |
| 48339 | Montgomery County |
| 48473 | Waller County |
| 48481 | Wharton County |

Each observation represents the **number of customers experiencing a power outage** in the corresponding county at a given 15-minute timestamp.

## Data Sources

The data are compiled entirely from **publicly available (open-source)** resources.

- **County-level power outage data** were obtained from the **U.S. Department of Energy's EAGLE-I (Electricity Infrastructure Operations Center) platform**, which reports the number of utility customers without electric service over time.
- The accompanying hurricane track and wind-field information used in the teaching case is obtained from **NOAA's HURDAT2 hurricane archive**. 

## Purpose

This dataset is intended for educational and research purposes, including:

- Time-series visualization
- Power outage trend analysis
- Change-point detection
- Continuous piecewise-linear fitting
- Multidimensional fitting with shared change-points
- Mixed-integer optimization for infrastructure resilience analysis

## File Format

The dataset is provided as a Microsoft Excel (`.xlsx`) workbook and can be read directly using spreadsheet software or Python.

Example:

```python
import pandas as pd

df = pd.read_excel("Hurricane_Nicholas_Power_Outage_Data.xlsx")
```

## Notes

- All timestamps are spaced **15 minutes apart**.
- Outage counts denote the **total number of customers without electric service** at each reporting time.
- The dataset focuses on the counties most severely affected by **Hurricane Nicholas (September 2021)** and is intended to illustrate optimization-based change-point detection in multidimensional time series.
