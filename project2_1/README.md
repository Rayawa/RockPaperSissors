# Housing Regression

English | [简体中文](README_zh.md)

Random-forest regression on the California housing dataset.

Archived project retained for reference.

## Overview

The script loads the scikit-learn dataset, trains a random forest and writes predictions, a serialized model and plots. The first dataset fetch requires network access.

## Technology and Dependencies

Python 3, scikit-learn, pandas, Matplotlib and joblib.

## Repository Structure

`main.py` runs the workflow; outputs include `model.pkl`, `prediction_results.csv` and `images/`.

## Quick Start

From this directory, after preparing the required input data and dependencies:

```bash
python -m pip install scikit-learn pandas matplotlib joblib
python main.py
```
