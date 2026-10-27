# RockPaperSissors

English | [简体中文](README_zh.md)

Python exercises and machine-learning examples culminating in YOLO hand-gesture detection.

Archived project retained for reference.

## Overview

The repository progresses from standalone Python exercises to housing regression, lifestyle-data analysis and rock-paper-scissors detection. The detector includes training, validation, image prediction and webcam scripts. Saved metrics and media describe earlier runs and may vary with data, weights and hardware.

## Technology and Dependencies

Python 3. The analysis projects use pandas, scikit-learn, Matplotlib, Seaborn and joblib. Detection uses PyTorch, Ultralytics and OpenCV; Roboflow and kagglehub are optional download helpers. The training script selects CUDA; edit its device setting for other environments.

## Repository Structure

- `project1/` — Python fundamentals
- `project2_1/` — California housing regression
- `project2_2/` — lifestyle data analysis
- `project3/` — YOLO gesture detection
- `testEnvironment.py` — environment inspection script

## Quick Start

Create a Python virtual environment, then choose a subproject:

```bash
python3 -m venv .venv
source .venv/bin/activate
python project1/1.1.py
```

For detection, install the PyTorch build suitable for the machine, then `python -m pip install ultralytics opencv-python`. Run from `project3/`, check `train.py` and the dataset YAML, and run `python train.py`. With compatible weights at `runs/detect/train/weights/best.pt`, run `python detect.py` for camera 0; press Q to exit. Dataset and trained weights may need to be supplied locally. See each subdirectory README for its inputs and dependencies.
