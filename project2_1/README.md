# Project 2-1: California Housing Prediction (Random Forest)

English | [简体中文](README_zh.md)


A scikit-learn regression project that trains a random forest on the **California housing dataset** to predict median neighborhood house values from housing features.

## Repository Structure

```
project2_1/
├── README.md                # This file
├── main.py                  # Main program: training, prediction, evaluation, visualization
├── model.pkl                # Trained RandomForest model (joblib serialization)
├── prediction_results.csv   # Actual versus predicted test-set values
└── images/
    ├── feature_importance.png    # Feature importance bar chart
    └── prediction_scatter.png    # Actual versus predicted scatter plot
```

## Dataset

**California Housing Dataset** (provided through scikit-learn)

- Samples: 20,640 neighborhood records
- Features: 8
- Target: `MedHouseVal` (median house value, in units of USD 100,000)

| Feature | Description | Type |
|------|------|------|
| MedInc | Median neighborhood income | Continuous |
| HouseAge | Median house age | Continuous |
| AveRooms | Average room count | Continuous |
| AveBedrms | Average bedroom count | Continuous |
| Population | Neighborhood population | Continuous |
| AveOccup | Average occupancy | Continuous |
| Latitude | Latitude | Continuous |
| Longitude | Longitude | Continuous |

## Model

**Algorithm**: RandomForestRegressor (random-forest regression)

**Hyperparameters**:
- `n_estimators=200` — 200 decision trees
- `max_depth=20` — depth limit to reduce overfitting
- `random_state=42` — reproducible results
- `n_jobs=-1` — parallel training on all CPU cores

### Evaluation Results

| Metric | Value |
|------|------|
| MSE | 0.2552 |
| RMSE | 0.5052 |
| R² | 0.8053 |

R² = 0.8053: the model explains approximately 80.5% of the variance in house values, indicating good performance.

### Top 5 Feature Importances

1. **MedInc** (median income) — the strongest predictor
2. **AveOccup** (average occupancy)
3. **Latitude**
4. **Longitude**
5. **HouseAge** (house age)

Income and geographic location are the principal predictors of house values.

## Running the Project

```bash
cd project2_1
python main.py
```

Outputs:
- Dataset information, training progress and evaluation metrics in the console
- `model.pkl` — trained model
- `prediction_results.csv` — predictions
- `images/feature_importance.png` — feature-importance plot
- `images/prediction_scatter.png` — actual-versus-predicted scatter plot

## Requirements

```bash
pip install scikit-learn pandas matplotlib joblib
```

- Python 3.8+
- scikit-learn
- pandas
- matplotlib
- joblib
