# Hand-Gesture Detection

[English](README.md) | 简体中文

基于 YOLO 的石头、布与剪刀手势检测。

归档项目，保留用于参考。

## 项目概述

脚本覆盖数据下载、YOLO11n 训练、验证和测试集评估、图片与摄像头推理。数据服务访问在本地配置。

## 技术栈与依赖

Python 3、兼容 PyTorch、Ultralytics、OpenCV；可选数据下载另需 Roboflow。训练脚本指定 CUDA。

## 文件结构

`train.py`、`evaluate.py`、`test.py`、`predict.py`、`detect.py`。训练读取 `rock-paper-scissors-11/data.yaml`，推理读取 `runs/detect/train/weights/best.pt`。

## 快速上手

在本目录准备好所需输入数据与依赖后执行：

```bash
python -m pip install ultralytics opencv-python
python train.py
python detect.py
```

先按本机计算环境安装 PyTorch。训练前准备数据集，检测前准备对应训练权重；图片推理另需 `my_hand.jpg`，摄像头推理按 Q 退出。
