# RockPaperSissors

[English](README.md) | 简体中文

由 Python 基础与机器学习示例组成、以 YOLO 手势检测为主要项目的代码集合。

归档项目，保留用于参考。

## 项目概述

仓库从独立 Python 练习逐步扩展到房价回归、行为数据分析和石头剪刀布检测。检测项目包含训练、评估、图片推理及摄像头脚本；保存的指标和素材对应既有运行结果，实际结果取决于数据、权重及硬件。

## 技术栈与依赖

Python 3。分析项目使用 pandas、scikit-learn、Matplotlib、Seaborn、joblib；检测项目使用 PyTorch、Ultralytics、OpenCV。Roboflow 和 kagglehub 用于可选下载。训练脚本选择 CUDA，其他环境需修改设备设置。

## 文件结构

- `project1/` — Python 基础
- `project2_1/` — 加州房价回归
- `project2_2/` — 行为数据分析
- `project3/` — YOLO 手势检测
- `testEnvironment.py` — 环境检查脚本

## 快速上手

创建虚拟环境后选择子项目：

```bash
python3 -m venv .venv
source .venv/bin/activate
python project1/1.1.py
```

检测项目需先安装适合本机的 PyTorch，再执行 `python -m pip install ultralytics opencv-python`。进入 `project3/`，核对 `train.py` 与数据集 YAML 后执行 `python train.py`。将兼容权重放在 `runs/detect/train/weights/best.pt` 后，可运行 `python detect.py` 使用摄像头 0，按 Q 退出。数据集和训练权重可能需要自行在本地准备。各子目录 README 说明具体输入与依赖。
