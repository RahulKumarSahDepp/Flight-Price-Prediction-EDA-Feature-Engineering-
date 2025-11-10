# ✈️ Flight Price Prediction – EDA & Feature Engineering  
**A comprehensive exploratory data analysis and feature engineering workflow to clean, transform, and encode raw flight dataset into a machine-learning-ready format (all numerical columns).**  
*(≈200 characters)*

---

## 📌 Project Overview
Airline ticket pricing is affected by multiple factors including flight duration, route, stops, source/destination city, and airline brand.  
This project performs full **Exploratory Data Analysis (EDA)** and **Feature Engineering** on a raw flight dataset and converts all categorical/string variables into numerical form for ML model training.

✅ Total rows: **10,683**  
✅ Initial columns: **11**  
✅ After processing: All features converted into **integer or numeric**  
✅ Suitable for Regression models (Linear Regression, Random Forest, XGBoost, etc.)

---

## ✅ Dataset – Original Columns & Types
| Column | Type | Description |
|--------|------|-------------|
| Airline | object | Airline name |
| Date_of_Journey | object | Flight date |
| Source | object | Departure city |
| Destination | object | Arrival city |
| Route | object | Multi-stop route |
| Dep_Time | object | Departure time |
| Arrival_Time | object | Arrival time |
| Duration | object | Total travel time |
| Total_Stops | object | Number of stops |
| Additional_Info | object | Extra flight details |
| Price | int64 | Target variable |

---

## 🔧 Data Pre-Processing Steps
✔ Removed missing & inconsistent records  
✔ Fixed wrong string formats  
✔ Extracted date-related features  
✔ Split timestamps into hours/minutes  
✔ Converted categorical features to numerical  
✔ Ensured no null values remain

---

## 📊 EDA Performed
- Airline vs Price comparison
- Source/Destination price distribution
- Stops vs Price relation
- Duration vs Price trend
- Boxplots, histograms, correlation heatmap
- Outlier detection using IQR

---

## 🧪 Feature Engineering (Final Numeric Dataset)

### ✅ Extracted New Features
| New Feature | Description |
|-------------|-------------|
| Journey_Day | Day of flight |
| Journey_Month | Month of flight |
| Dep_Hour / Dep_Minute | Departure time split |
| Arrival_Hour / Arrival_Minute | Arrival time split |
| Duration_Hours / Duration_Minutes | Converted from string |

### ✅ Encoded Features
- `Total_Stops` → 0, 1, 2, 3, 4
- Label/One-Hot Encoding for:
  - Airline
  - Source
  - Destination
  - Additional_Info

✅ **All columns numeric** and ready for model training.

---

## ✅ Final Dataset Example
| Feature | Type |
|----------|------|
| Airline (encoded) | int |
| Source (encoded) | int |
| Destination (encoded) | int |
| Journey_Day | int |
| Journey_Month | int |
| Duration_Hours | int |
| Duration_Minutes | int |
| Total_Stops | int |
| Price | int |

---

## ⚙️ Installation
```
pip install pandas numpy matplotlib seaborn scikit-learn
```

## Run
```
python src/preprocessing.py
```
