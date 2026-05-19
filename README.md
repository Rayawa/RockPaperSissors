# 🪨📄✂️ 2026 暑期 Python 课程项目

> **本仓库的核心内容位于 Project 3** — 基于 YOLO11n 的石头剪刀布手势识别系统。
> Project 1 和 Project 2 是课程前期任务与过渡练习，帮助掌握 Python 与机器学习基础，最终汇聚到 Project 3 的完整深度学习项目。

---

## 📋 项目概览

### 🔥 Project 3 — 石头剪刀布手势识别（YOLO11n）← **核心项目**

基于 **YOLO11n** 的目标检测项目，实时识别剪刀、石头、布三种手势。

- **数据集**：Roboflow 公开数据集（15,874 张图片，含数据增强）
- **验证集 mAP50**：**0.940** · **测试集 mAP50**：**0.934**
- **推理速度**：单张图片 < 2.1ms（GPU 加速）
- **推理结果**：见 `result.png`（截图）、`result.gif`（动图）、`result.mp4`（录屏）
- **支持**：单张图片推理 + 实时摄像头检测

📂 [project3/](project3/) · 📄 [README →](project3/README.md)

---

### 📘 Project 1 — Python 基础练习（过渡练习）

入门级 Python 编程练习，涵盖变量、数据类型、运算符、流程控制、函数、组合数据类型等基础语法，共 **14 个练习文件**（编号 1.1 ~ 6.2）。

📂 [project1/](project1/) · 📄 [README →](project1/README.md)

---

### 🏠 Project 2-1 — 加州房价预测（过渡项目）

基于 scikit-learn 内置的 **California Housing Dataset**，使用随机森林回归模型预测街区房价中位数。

- **算法**：RandomForestRegressor（200 棵决策树，max_depth=20）
- **评估**：R² = 0.8053，RMSE = 0.5052

📂 [project2_1/](project2_1/) · 📄 [README →](project2_1/README.md)

---

### 📊 Project 2-2 — 学生数字行为分析（过渡项目）

基于 Kaggle 真实数据集的探索性分析与回归预测，分析学习时间、屏幕时间、睡眠等因素与 CGPA 的关系。

📂 [project2_2/](project2_2/) · 📄 [README →](project2_2/README.md)

---

## 📊 实验报告

| 实验 | 报告 |
|------|------|
| 实验一 | Python 程序设计基础 → [📄 查看](实验一_Python程序设计基础_实验报告.md) |
| 实验二（2-1） | 机器学习综合程序设计（加州房价预测）→ [📄 查看](实验二_机器学习综合程序设计_实验报告.md) |
| 实验二（2-2） | 学生数字行为与学习表现分析 → [📄 查看](实验二（2-2）_学生数字行为分析_实验报告.md) |
| 实验三 | 深度学习综合程序设计（手势识别）→ [📄 查看](实验三_深度学习综合程序设计_实验报告.md) |

---

## 🔧 环境总览

| 项目 | 主要依赖 | 定位 |
|------|----------|------|
| Project 1 | 标准库 + math | 基础练习 · 过渡 |
| Project 2-1 | scikit-learn, pandas, matplotlib | 机器学习入门 · 过渡 |
| Project 2-2 | pandas, seaborn, scikit-learn | 数据分析实践 · 过渡 |
| **Project 3** | **PyTorch, ultralytics, OpenCV** | **核心项目** |

各项目详细环境要求见子目录 README。
