# Hand-Gesture Detection

English | [简体中文](README_zh.md)

YOLO detection of rock, paper and scissors gestures.

Archived project retained for reference.

## Overview

Scripts cover dataset download, YOLO11n training, validation/test evaluation, image prediction and webcam inference. Configure dataset access locally; do not put service credentials in documentation.

## Technology and Dependencies

Python 3, a compatible PyTorch installation, Ultralytics and OpenCV; Roboflow for optional dataset downloading. The training script requests CUDA.

## Repository Structure

`train.py`, `evaluate.py`, `test.py`, `predict.py` and `detect.py`. Training expects `rock-paper-scissors-11/data.yaml`; inference expects `runs/detect/train/weights/best.pt`.

## Quick Start

From this directory, after preparing the required input data and dependencies:

```bash
python -m pip install ultralytics opencv-python
python train.py
python detect.py
```

Install PyTorch separately for the local compute environment. Supply the dataset before training, or the expected trained weights before detection. For image prediction, provide `my_hand.jpg`; press Q to close webcam inference.
