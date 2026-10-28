# Project 3: Rock-Paper-Scissors Gesture Detection

English | [简体中文](README_zh.md)


A YOLO11n object-detection project for rock, paper and scissors hand gestures.

## Overview

The project trains an Ultralytics YOLO11n detector to recognize Scissors, Rock and Paper gestures in webcam images in real time.

## Dataset

The dataset is version v11 (YOLOv8n-100epochs) of [rock-paper-scissors-sxsw](https://universe.roboflow.com/roboflow-58fyf/rock-paper-scissors-sxsw) on Roboflow, containing **15,874 images** created by contributors to the SXSW 2023 “World's Largest Game of Rock, Paper, Scissors” challenge.

### Preprocessing
- Automatic rotation to correct EXIF orientation
- Resize to 640×640 using stretch-to-fit

### Augmentation (7 Versions per Original Image)
- Horizontal flip with 50% probability
- Random rotation from -12° to +12°
- Random shear from -2° to +2°
- Brightness adjustment from -25% to +25%
- Exposure adjustment from -25% to +25%
- Random Gaussian blur from 0 to 1.5 pixels
- Salt-and-pepper noise on 1% of pixels

### Classes
- Paper
- Rock
- Scissors

## Requirements

- Python 3.12+
- PyTorch 2.7+
- CUDA-compatible GPU for training; optional for inference
- ultralytics
- opencv-python
- roboflow for dataset downloading

## File Structure

```
project3/
├── README.md                    # This file
├── console.md                   # Console logs
├── download_data.py             # Download dataset from Roboflow
├── train.py                     # Train model
├── evaluate.py                  # Evaluate on validation set
├── test.py                      # Evaluate on test set
├── predict.py                   # Single-image inference
├── detect.py                    # Live camera detection
├── yolo11n.pt                   # YOLO11n pretrained weights
├── yolo26n.pt                   # YOLO26n pretrained weights
├── result.png                   # Inference result screenshot
├── result.gif                   # Live detection animation
├── result.mp4                   # Live detection recording
├── rock-paper-scissors-11/      # Dataset directory
│   ├── data.yaml                # Dataset configuration
│   ├── train/                   # Training set (images + labels)
│   ├── valid/                   # Validation set
│   └── test/                    # Test set
└── runs/
    └── detect/
        ├── train/               # Training outputs (weights, metric curves, training images)
        ├── val/                 # Validation evaluation outputs
        └── val-2/               # Test evaluation outputs
```

## Usage

### 1. Download the Dataset

```bash
python download_data.py
```

A valid Roboflow API Key is required (included in the script in the original setup).

### 2. Train the Model

```bash
python train.py
```

Training parameters:
- Model: `yolo11n.pt`
- Input size: 640×640
- Epochs：50
- Batch size：16
- Workers：8
- Optimizer: AdamW
- Device: CUDA

Training took approximately **3.07 hours** (50 epochs, RTX 5060 Laptop GPU).

### 3. Evaluate the Model

```bash
# Validation evaluation
python evaluate.py

# Test evaluation
python test.py
```

**Validation results:**
| Class     | Images | Instances | P     | R     | mAP50 | mAP50-95 |
|-----------|--------|-----------|-------|-------|-------|----------|
| all       | 588    | 406       | 0.942 | 0.891 | 0.940 | 0.697    |
| Paper     | 134    | 141       | 0.934 | 0.894 | 0.936 | 0.690    |
| Rock      | 125    | 147       | 0.949 | 0.898 | 0.943 | 0.689    |
| Scissors  | 114    | 118       | 0.944 | 0.881 | 0.940 | 0.714    |

**Test results:**
| Class     | Images | Instances | P     | R     | mAP50 | mAP50-95 |
|-----------|--------|-----------|-------|-------|-------|----------|
| all       | 320    | 210       | 0.898 | 0.920 | 0.934 | 0.693    |
| Paper     | 72     | 72        | 0.868 | 0.861 | 0.904 | 0.630    |
| Rock      | 63     | 72        | 0.938 | 0.944 | 0.951 | 0.715    |
| Scissors  | 64     | 66        | 0.887 | 0.953 | 0.947 | 0.734    |

### 4. Single-Image Prediction

```bash
python predict.py
```

The default input is `my_hand.jpg`; detection results are saved under `runs/detect/`.

### 5. Real-Time Webcam Detection

```bash
python detect.py
```

- Opens the system webcam for real-time detection
- Displays FPS in the window
- Press `Q` to quit

## Inference Examples

The project directory contains these inference outputs:

| File | Description |
|------|------|
| `result.png` | Single-image inference screenshot |
| `result.gif` | Real-time webcam animation cycling through the gestures |
| `result.mp4` | Full real-time detection recording |

![Inference result](result.png)

![Real-time detection animation](result.gif)

## Training Logs

See `console.md`.

## Training Environment

- GPU: NVIDIA GeForce RTX 5060 Laptop GPU (8GB VRAM)
- CUDA: 11.8
- PyTorch: 2.7.1
- Ultralytics: 8.4.48
- Python: 3.12.13
