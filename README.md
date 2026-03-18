# 🚕 Taxi Fare Prediction

A machine learning project to predict the total amount paid by travelers for NYC taxi rides using ensemble methods. Achieved an **R² score of 0.9603** on the Kaggle leaderboard.

---

## 🏆 Results

| Metric | Value |
|---|---|
| Kaggle Leaderboard R² | **0.9603** |
| Best Local Validation R² | **0.9514** |
| Best Local Validation RMSE | **5.1427** |
| Best Model | **Extra Trees Regressor** |

![Leaderboard Score](images/leaderboard_.png)

---

## 📋 Problem Statement

Given a dataset of NYC taxi rides, predict the `total_amount` paid by the traveler. The dataset includes features such as pickup/dropoff timestamps, trip distance, passenger count, payment type, and various surcharge columns.

**Evaluation Metric:** R² Score (higher is better)

---

## 📁 Project Structure

```
taxi-fare-prediction/
├── images/
│   ├── leaderboard_.png
│   ├── model_comparison.png
│   ├── feature_importance.png
│   └── correlation_heatmap.png
├── taxi_fare_prediction.ipynb
├── requirements.txt
├── .gitignore
└── README.md
```

---

## 📊 Dataset

The dataset comes from the [Kaggle MLP Term-1 2026 Assignment](https://www.kaggle.com/t/a7dfe6cf90844dd28af5e893c0572008).

| File | Rows | Columns | Description |
|---|---|---|---|
| `train.csv` | 10,000 | 17 | Training data with target variable |
| `test.csv` | 1,500 | 17 | Test data without target variable |
| `sample_submission.csv` | 1,500 | 2 | Submission format reference |

### Column Descriptions

| Column | Type | Description |
|---|---|---|
| `total_amount` | float | **Target** — Total fare paid by traveler |
| `VendorID` | int | Taxi vendor identifier |
| `tpep_pickup_datetime` | object | Pickup timestamp |
| `tpep_dropoff_datetime` | object | Dropoff timestamp |
| `passenger_count` | float | Number of passengers |
| `trip_distance` | float | Trip distance in miles |
| `RatecodeID` | float | Rate code for the ride |
| `store_and_fwd_flag` | object | Trip data storage flag (Y/N) |
| `PULocationID` | int | Pickup location ID |
| `DOLocationID` | int | Dropoff location ID |
| `payment_type` | object | Payment method used |
| `extra` | float | Extra charges |
| `tip_amount` | float | Tip amount |
| `tolls_amount` | float | Toll charges |
| `improvement_surcharge` | float | Improvement surcharge |
| `congestion_surcharge` | float | Congestion surcharge |
| `Airport_fee` | float | Airport fee |

---

## 🔍 Exploratory Data Analysis

### Key Findings

- **10,000 training samples** with 17 features
- **Missing values** found in 5 columns: `passenger_count`, `RatecodeID`, `store_and_fwd_flag`, `congestion_surcharge`, `Airport_fee` (366 rows each)
- **No duplicate rows** found
- **100 negative `total_amount`** values (refunds/reversals) — kept in training data
- **1 extreme outlier** above $500 — removed
- `total_amount` ranges from **-129.30 to 485.10** with a mean of **$29.74**

### Correlation Heatmap

![Correlation Heatmap](images/correlation_heatmap.png)

Key correlations with `total_amount`:
- `trip_distance`: **0.89** — strongest predictor
- `tip_amount`: **0.67**
- `tolls_amount`: **0.68**
- `Airport_fee`: **0.58**

---

## 🛠️ Feature Engineering

Created **9 new features** from existing columns:

| Feature | Description |
|---|---|
| `pickup_hour` | Hour of pickup (0-23) |
| `pickup_day` | Day of month |
| `pickup_month` | Month of year |
| `pickup_year` | Year |
| `pickup_weekday` | Day of week (0=Monday) |
| `trip_duration_min` | Trip duration in minutes |
| `is_rush_hour` | 1 if pickup between 7-9am or 5-7pm |
| `is_night` | 1 if pickup between 10pm-5am |
| `is_weekend` | 1 if pickup on Saturday or Sunday |

**Total features used:** 23

---

## ⚙️ Data Preprocessing

### Outlier Handling
```
total_amount > 500  : 1 row removed   (extreme anomaly)
trip_distance < 0   : 0 rows removed  (physically impossible)
total_amount < 0    : KEPT            (test set contains them too — critical insight!)
passenger_count = 0 : IMPUTED         (sensor/entry error)
```

> **Key Insight:** Initially removing negative `total_amount` values caused the leaderboard score to drop to 0.77. Including them pushed the score to **0.9603** because the test set contains similar negative entries representing refunds.

### Missing Value Imputation
- `passenger_count` → filled with **median** from training set
- `RatecodeID` → filled with **mode** from training set
- `congestion_surcharge`, `Airport_fee` → filled with **0**
- `store_and_fwd_flag` → filled with **0** (mapped N→0)

### Encoding
- `payment_type` (5 categories: Credit Card, Cash, UPI, Unknown, Wallet) → **LabelEncoder**
  - Fitted on both train and test combined to handle unseen categories
- `store_and_fwd_flag` (Y/N) → mapped to **1/0** during feature engineering

### Scaling
- **Tree-based models** (RF, XGBoost, LightGBM, ExtraTrees): Scale-invariant → **no scaling**
- **Linear models** (LinearRegression, Ridge): Sensitive to magnitude → **StandardScaler**

---

## 🤖 Models Trained

7 different models were trained and compared on the validation set (20% holdout):

| Model | R² Score | RMSE |
|---|---|---|
| **Extra Trees** | **0.9514** | **5.1427** |
| XGBoost (Tuned) | 0.9250 | 6.3893 |
| Random Forest (Tuned) | 0.9203 | 6.5851 |
| LightGBM | 0.9095 | 7.0202 |
| Ridge (Tuned) | 0.8748 | 8.2565 |
| Linear Regression | 0.8746 | 8.2599 |
| Decision Tree | 0.8681 | 8.4741 |

### Hyperparameter Tuning
- **Ridge**: GridSearchCV over alpha = [0.1, 1.0, 10.0, 100.0] → best alpha = 10.0
- **Random Forest**: Tuned n_estimators=200, max_depth=None, min_samples_leaf=2
- **XGBoost**: Tuned n_estimators=1000, learning_rate=0.03, max_depth=7, subsample=0.8

![Model Comparison](images/model_comparison.png)

---

## 📈 Feature Importance

![Feature Importance](images/feature_importance.png)

Top 5 most important features according to XGBoost:
1. `improvement_surcharge` — 0.30
2. `trip_distance` — 0.24
3. `tolls_amount` — 0.20
4. `RatecodeID` — 0.09
5. `congestion_surcharge` — 0.03

---

## 🚀 How to Run

### 1. Clone the Repository
```bash
git clone https://github.com/Kunal-Somani/taxi-fare-prediction.git
cd taxi-fare-prediction
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
```

### 3. Get the Dataset
1. Go to the [Kaggle competition](https://www.kaggle.com/t/a7dfe6cf90844dd28af5e893c0572008)
2. Join the competition
3. Download `train.csv`, `test.csv`, `sample_submission.csv`
4. Place them in the project root folder

### 4. Run the Notebook
```bash
jupyter notebook taxi_fare_prediction.ipynb
```
Run all cells in order — the final cell will generate `submission.csv`

---

## 📦 Requirements

```
pandas
numpy
matplotlib
seaborn
scikit-learn
xgboost
lightgbm
```

Install all with:
```bash
pip install -r requirements.txt
```

---

## 💡 Key Takeaways

1. **Keeping negative fares** in training data was critical — test set contains refunds/reversals
2. **Imputing missing values** instead of dropping rows preserved 366 extra training samples
3. **Extra Trees** outperformed XGBoost and Random Forest on this dataset
4. **Feature engineering** from datetime columns (rush hour, night, weekend flags) improved model performance
5. **Combining train+test** for LabelEncoder fitting prevents unseen category errors

---

## 👤 Author

**Kunal Somani**
- Kaggle: [K100mani](https://www.kaggle.com/kunal100mani)
- GitHub: [Kunal-Somani](https://github.com/Kunal-Somani)

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
