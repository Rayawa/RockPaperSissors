# Project 2-2: Student Digital Behavior and Academic Performance

English | [简体中文](README_zh.md)


An exploratory-analysis and regression project based on real student digital-behavior data, examining how study time, screen time, sleep, exercise and attendance relate to academic performance (CGPA).

## Repository Structure

```
project2_2/
├── README.md                          # 本文件
├── DownloadCSV.py                     # kagglehub 下载数据集
├── main.py                            # 主程序：清洗 → 可视化 → 建模 → 评估
├── data/
│   └── student_digital_behavior.csv   # 原始数据集
├── outputs/
│   ├── cleaned_student_digital_behavior.csv  # 清洗后数据
│   ├── descriptive_statistics.csv           # 描述性统计
│   ├── model_results.csv                    # 模型评估对比
│   └── feature_importance.csv               # 随机森林特征重要性
└── figures/
    ├── fig1_screen_time_distribution.png    # 屏幕时间分布（直方图 + KDE）
    ├── fig2_screen_time_vs_cgpa.png         # 屏幕时间 vs CGPA 散点图
    ├── fig3_study_hours_vs_cgpa.png         # 学习时间 vs CGPA 散点图
    ├── fig4_sleep_hours_vs_cgpa.png         # 睡眠时间 vs CGPA 散点图
    ├── fig5_correlation_heatmap.png         # 数值特征相关性热力图
    └── fig6_feature_importance.png          # Top 10 特征重要性柱状图
```

## Dataset

The **[Student Lifestyle and Academic Performance Dataset](https://www.kaggle.com/datasets/rafi003/student-lifestyle-and-academic-performance-dataset)** from Kaggle.

**Original fields** (12 columns):

| Field | Description | Type |
|------|------|------|
| Age | Age | Numeric |
| Branch | Academic discipline | Categorical |
| Study_Hours_per_Day | Daily study time (hours) | Numeric |
| Sleep_Hours | Daily sleep time (hours) | Numeric |
| Screen_Time_Hours | Daily screen time (hours) | Numeric |
| Gym_Hours_per_Week | Weekly exercise time (hours) | Numeric |
| Diet_Type | Diet type | Categorical |
| Attendance_Percentage | Attendance (%) | Numeric |
| Stress_Level_1_to_10 | Stress level (1–10) | Numeric |
| Residence | Accommodation type | Categorical |
| Internal_Marks | Internal assessment marks | Numeric |
| **CGPA** | **Grade point average (target)** | Numeric |

## Data Cleaning

The main program performs these steps automatically:

1. **Field selection** — keep only model inputs, excluding `Internal_Marks` to prevent data leakage.
2. **Deduplication** — remove duplicate rows.
3. **Missing values** — fill numeric columns with medians and categorical columns with modes.
4. **Outlier filtering** — apply reasonable ranges to age, study time, sleep and other fields.

## Exploratory Data Analysis (EDA)

The main program generates 6 visualizations:

| Figure | Content |
|------|------|
| fig1 | Screen-time distribution: histogram and KDE |
| fig2 | Screen time versus CGPA |
| fig3 | Study time versus CGPA |
| fig4 | Sleep time versus CGPA |
| fig5 | Correlation heatmap of numeric features |
| fig6 | Top 10 feature importances from the random forest |

## Modeling and Evaluation

### Model Comparison

Two regression models are trained and compared:

| Model | Description |
|------|------|
| Linear Regression | Baseline linear-regression model |
| Random Forest | Random-forest regression with 100 trees |

### Feature Encoding

Categorical variables (`Branch`, `Diet_Type`, `Residence`) are converted to numeric inputs using one-hot encoding (`drop_first=True`).

### Training/Test Split

80% training / 20% test, with `random_state=42`.

## Running the Project

### 1. Download the Dataset (Optional)

```bash
cd project2_2
python DownloadCSV.py
```

Install `kagglehub` and configure a Kaggle API key. Alternatively, download the dataset manually from [Kaggle](https://www.kaggle.com/datasets/rafi003/student-lifestyle-and-academic-performance-dataset) and place it in `data/`.

### 2. Run the Complete Analysis

```bash
python main.py
```

Outputs:
- Console summaries of the data, row counts before and after cleaning, descriptive statistics, model evaluations and feature importances
- `outputs/` — CSV result files
- `figures/` — visualization files

## Requirements

```bash
pip install pandas matplotlib seaborn scikit-learn
```

- Python 3.8+
- pandas
- matplotlib
- seaborn
- scikit-learn
- kagglehub (needed only for dataset downloading)
