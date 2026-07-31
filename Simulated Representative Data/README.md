# Simulated Representative Data

This folder contains the synthetic dataset used to motivate the need for piecewise-linear regression and change-point detection in the teaching case:

> **When Linear Regression Isn't Enough: Building Optimization Models for Change-Point Detection and Trend Analysis**

The data illustrate a time series whose underlying trend changes multiple times, making a single linear regression model inadequate. This example is used as the introductory motivating example in the teaching case. 

## Files

### `motivating_piecewise_linear_data_and_fit.csv`

This CSV file contains:

- Simulated time-series observations
- Continuous piecewise-linear fitted values
- Locations of the detected change-points

The dataset is intended to visually demonstrate how piecewise-linear fitting captures multiple local trends that cannot be accurately represented by a single regression line.

## Purpose

This dataset can be used to:

- Visualize multiple trend changes in time-series data
- Compare linear regression with piecewise-linear regression
- Understand the concept of change-points
- Demonstrate continuous piecewise-linear fitting
- Generate figures for classroom demonstrations and tutorials

## File Format

The dataset is provided as a comma-separated values (`.csv`) file and can be opened using spreadsheet software or Python.

Example:

```python
import pandas as pd

df = pd.read_csv("motivating_piecewise_linear_data_and_fit.csv")
```

## Notes

This is a **simulated** dataset created solely for educational and illustrative purposes. It does not correspond to any real-world system or application, but is designed to clearly demonstrate the advantages of optimization-based change-point detection over fitting a single linear regression model.
