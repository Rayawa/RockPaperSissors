# Lifestyle Data Analysis

English | [简体中文](README_zh.md)

Exploratory analysis and regression using a lifestyle and academic-performance dataset.

Archived project retained for reference.

## Overview

The workflow cleans tabular data, produces figures and compares linear and random-forest regression. It uses a public dataset rather than records about project contributors.

## Technology and Dependencies

Python 3, pandas, Matplotlib, Seaborn and scikit-learn; kagglehub for optional downloading.

## Repository Structure

`main.py` analyzes data; `DownloadCSV.py` downloads the dataset. The input is `data/student_digital_behavior.csv`; results go to `outputs/` and `figures/`.

## Quick Start

From this directory, after preparing the required input data and dependencies:

```bash
python -m pip install pandas matplotlib seaborn scikit-learn
python main.py
```

Place the CSV at the input path first. `DownloadCSV.py` uses kagglehub and prints its cache path; copy the desired CSV into `data/` before running the analysis.
