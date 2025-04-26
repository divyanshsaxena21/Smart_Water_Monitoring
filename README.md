# 💧 Smart Water Monitoring

Water scarcity is an increasingly global issue, with urban households playing a major role in water wastage due to inefficient consumption habits. Traditional water meters provide only total usage data without insights into consumption patterns, making it difficult for homeowners to optimize their water usage effectively.

**Smart water monitoring systems**, powered by **machine learning**, can help households predict their water consumption and adopt effective conservation measures.

---

## 🎯 Task

The goal of this project is to develop a **Machine Learning model** that predicts **daily water consumption** for individual households based on:

- Historical usage patterns  
- Household characteristics  
- Weather conditions  
- Conservation behaviors  

---

## 📁 Dataset Description

The dataset folder contains the following files:

- `train.csv` – (14000 rows × 12 columns)  
- `test.csv` – (6000 rows × 11 columns)  
- `sample_submission.csv` – (5 rows × 2 columns)

### Columns Description

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
| `Water_Consumption`       | Actual water consumption in that period (**Target Variable**) |

---

## 🧮 Evaluation Metric

\[
\text{Score} = \max\left(0,\ 100 - \sqrt{\text{MSE}}\right)
\]

Where:

- MSE = Mean Squared Error between actual and predicted values.

---

## 📝 Result Submission Guidelines

- **Index** must be `Timestamp` (as in the test file).
- **Target** is the `Water_Consumption` column.
- The submission must:
  - Be in `.csv` format only.
  - Be of size **6000 × 2**.
  - Follow the column format as shown in `sample_submission.csv`.

---
