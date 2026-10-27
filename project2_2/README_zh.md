# Lifestyle Data Analysis

[English](README.md) | 简体中文

使用生活习惯与学业表现数据集的探索分析和回归示例。

归档项目，保留用于参考。

## 项目概述

流程清洗表格数据、生成图件，并比较线性回归与随机森林回归。使用公开数据集，不记录项目参与者信息。

## 技术栈与依赖

Python 3、pandas、Matplotlib、Seaborn、scikit-learn；可选下载另需 kagglehub。

## 文件结构

`main.py` 分析数据，`DownloadCSV.py` 下载数据集。输入为 `data/student_digital_behavior.csv`，结果输出到 `outputs/` 与 `figures/`。

## 快速上手

在本目录准备好所需输入数据与依赖后执行：

```bash
python -m pip install pandas matplotlib seaborn scikit-learn
python main.py
```

先将 CSV 放入输入路径。`DownloadCSV.py` 使用 kagglehub 并打印缓存位置，需将对应 CSV 复制到 `data/` 后再分析。
