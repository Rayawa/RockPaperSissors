# Housing Regression

[English](README.md) | 简体中文

基于加州房价数据集的随机森林回归。

归档项目，保留用于参考。

## 项目概述

脚本加载 scikit-learn 数据集，训练随机森林并输出预测、模型和图件；首次获取数据集需要网络。

## 技术栈与依赖

Python 3、scikit-learn、pandas、Matplotlib、joblib。

## 文件结构

`main.py` 执行流程；输出包括 `model.pkl`、`prediction_results.csv` 和 `images/`。

## 快速上手

在本目录准备好所需输入数据与依赖后执行：

```bash
python -m pip install scikit-learn pandas matplotlib joblib
python main.py
```
