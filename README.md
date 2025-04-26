# 💧 Smart Water Monitoring

Water scarcity is an increasingly global issue, with urban households contributing significantly to water wastage due to inefficient consumption habits. Traditional water meters provide only cumulative usage data, offering little insight into consumption patterns.

**Smart Water Monitoring Systems**, powered by **Machine Learning**, offer predictive insights into water consumption, empowering households to optimize usage and adopt sustainable practices.

---

## 🎯 Project Objective

Develop a **Machine Learning model** that predicts **daily water consumption** for individual households using:

- Historical water usage
- Household demographics
- Weather conditions
- Conservation behaviors

---

## 📁 Dataset Description

The dataset contains three main files:

- `train.csv` – 14,000 rows × 12 columns  
- `test.csv` – 6,000 rows × 11 columns  
- `sample_submission.csv` – 5 rows × 2 columns

### 📌 Features

| Column Name               | Description                                                  |
|---------------------------|--------------------------------------------------------------|
| `Timestamp`               | Unique timestamp of an entry                                 |
| `Residents`               | Number of people living in the household                     |
| `Apartment_Type`          | Type of apartment                                            |
| `Temperature`             | Average temperature during the time period                   |
| `Humidity`                | Average humidity during the time period                      |
| `Water_Price`             | Water price at that time                                     |
| `Period_Consumption_Index`| Relative water usage for each 8-hour period                  |
| `Income_Level`            | Income level of the household                                |
| `Guests`                  | Number of guests present                                     |
| `Amenities`               | Types of amenities available in the household                |
| `Appliance_Usage`         | Whether water appliances are being used                      |
| `Water_Consumption`       | Actual water consumption in that period (**Target**)         |

---

## 🧮 Evaluation Metric

\[
\text{Score} = \max\left(0,\ 100 - \sqrt{\text{MSE}}\right)
\]

- **MSE (Mean Squared Error)** is used to evaluate predictions.
- Final score is inversely proportional to RMSE.

---

## 🤖 Model Performance

### 📊 AdaBoost Regressor
- **MAE:** 34.78  
- **MSE:** 1591.16  
- **RMSE:** 39.89  
- **R² Score:** 0.7156

### 📊 LightGBM Regressor
- **MAE:** 7.00  
- **MSE:** 127.53  
- **RMSE:** 11.29  
- **R² Score:** 0.9772

### 📊 XGBoost Regressor
- **MAE:** 8.38  
- **MSE:** 169.59  
- **RMSE:** 13.02  
- **R² Score:** 0.9697

### 📊 Ensemble Model (AdaBoost + LightGBM + XGBoost)
- **MAE:** 14.44  
- **MSE:** 305.93  
- **RMSE:** 17.49  
- **R² Score:** 0.9453

---

## 🏆 Achievement

I was ranked **Top 60** in this national-level machine learning competition for water consumption prediction.

---

## 📤 Submission Format

- Output must be a `.csv` file of shape **6000 × 2**
- Use `Timestamp` as the index
- Predict the `Water_Consumption` column
- Columns and format must match `sample_submission.csv`

---

## 🚀 Tech Stack

- Python  
- Pandas, NumPy  
- Scikit-learn  
- LightGBM  
- XGBoost  
- AdaBoost  
- Matplotlib, Seaborn (for visualization)

---

## 📌 Future Improvements

- Integrate time-series techniques (e.g., LSTM/GRU)
- Add feature engineering for cyclical time features (e.g., hour of day)
- Hyperparameter tuning using Optuna or GridSearchCV

---
