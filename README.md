# 🪨📄✂️ 2026 Summer Python Course Projects

English | [简体中文](README_zh.md)


> **The main project is in Project 3** — a YOLO11n-based rock-paper-scissors gesture-recognition system.
> Projects 1 and 2 contain introductory and transitional exercises in Python and machine learning, leading into the complete deep-learning project in Project 3.

---

## 📋 Project Overview

### 🔥 Project 3 — Rock-Paper-Scissors Gesture Recognition (YOLO11n) ← **Main Project**

A **YOLO11n** object-detection project that recognizes scissors, rock and paper gestures in real time.

- **Dataset**: a public Roboflow dataset containing 15,874 images, including augmented samples
- **Validation mAP50**: **0.940** · **Test mAP50**: **0.934**
- **Inference speed**: < 2.1ms per image with GPU acceleration
- **Inference outputs**: `result.png` (screenshot), `result.gif` (animation) and `result.mp4` (screen recording)
- **Supported modes**: single-image inference and real-time webcam detection

📂 [project3/](project3/) · 📄 [README →](project3/README.md)

---

### 📘 Project 1 — Python Fundamentals (Preparatory Exercises)

Fourteen introductory Python exercises covering variables, data types, operators, control flow, functions and compound data types, numbered 1.1–6.2.

📂 [project1/](project1/) · 📄 [README →](project1/README.md)

---

### 🏠 Project 2-1 — California Housing Prediction (Preparatory Project)

Random-forest regression using scikit-learn's **California Housing Dataset** to predict median neighborhood house values.

- **Algorithm**: RandomForestRegressor (200 trees, max_depth=20)
- **Evaluation**: R² = 0.8053, RMSE = 0.5052

📂 [project2_1/](project2_1/) · 📄 [README →](project2_1/README.md)

---

### 📊 Project 2-2 — Student Digital-Behavior Analysis (Preparatory Project)

Exploratory analysis and regression using a real Kaggle dataset to examine relationships between study time, screen time, sleep and CGPA.

📂 [project2_2/](project2_2/) · 📄 [README →](project2_2/README.md)

---

## 📊 Experiment Reports

| Experiment | Report |
|------|------|
| Experiment 1 | Python programming fundamentals → [📄 View](实验一_Python程序设计基础_实验报告.md) |
| Experiment 2 (2-1) | Integrated machine-learning programming: California housing prediction → [📄 View](实验二_机器学习综合程序设计_实验报告.md) |
| Experiment 2 (2-2) | Student digital behavior and academic performance → [📄 View](实验二（2-2）_学生数字行为分析_实验报告.md) |
| Experiment 3 | Integrated deep-learning programming: gesture recognition → [📄 View](实验三_深度学习综合程序设计_实验报告.md) |

---

## 🔧 Environment Overview

| Project | Main Dependencies | Role |
|------|----------|------|
| Project 1 | Standard library + math | Fundamentals and preparation |
| Project 2-1 | scikit-learn, pandas, matplotlib | Introduction to machine learning |
| Project 2-2 | pandas, seaborn, scikit-learn | Data-analysis practice |
| **Project 3** | **PyTorch, ultralytics, OpenCV** | **Main project** |

See each subdirectory's README for detailed environment requirements.
