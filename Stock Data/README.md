# Stock Data

This folder contains the stock-price datasets used in the teaching case:

> **When Linear Regression Isn't Enough: Building Optimization Models for Change-Point Detection and Trend Analysis**

The datasets illustrate different variants of piecewise-linear (PWL) fitting on historical stock-price data, including both continuous and discontinuous models, as well as multidimensional fitting with shared change-points. These examples are discussed in Section 3.2 of the accompanying teaching case. 

## Files

### `Amazon_Stock_Data_CPWL_fit.xlsx`

Historical daily closing prices for **Amazon (AMZN)** together with the corresponding **continuous piecewise-linear (CPWL)** fit.

The fitted model enforces continuity between adjacent linear segments, producing a smooth transition at every change-point.

---

### `Amazon_Stock_Data_PWL_fit.xlsx`

Historical daily closing prices for **Amazon (AMZN)** together with a **piecewise-linear fit without continuity**.

Unlike the continuous formulation, neighboring segments are allowed to have discontinuities at the detected change-points.

---

### `6_Dimensional_Stock_Price_PWL_fit.xlsx`

A multidimensional example containing daily closing prices for six technology companies:

- Apple (AAPL)
- Microsoft (MSFT)
- Amazon (AMZN)
- Alphabet (GOOGL)
- Meta Platforms (META)
- Tesla (TSLA)

Each stock is fitted using its own piecewise-linear function while all six time series share a common set of change-point locations. This demonstrates multidimensional change-point detection using shared breakpoints across correlated time series. :contentReference[oaicite:1]{index=1}

## Purpose

These datasets are intended for studying:

- Linear regression versus piecewise-linear regression
- Continuous versus discontinuous piecewise-linear fitting
- Change-point detection
- Shared change-point detection across multiple correlated time series
- Mixed-integer optimization formulations for trend analysis

## File Format

All datasets are provided as Microsoft Excel (`.xlsx`) workbooks and can be opened using Microsoft Excel, LibreOffice Calc, or Python libraries such as `pandas`.

Example:

```python
import pandas as pd

df = pd.read_excel("Amazon_Stock_Data_CPWL_fit.xlsx")
```

## Data Source

Historical stock-price data correspond to daily closing prices obtained from publicly available financial market data.

The fitted piecewise-linear models are provided for educational purposes to illustrate optimization-based change-point detection and trend analysis.
