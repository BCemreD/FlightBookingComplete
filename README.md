# FlightBookingComplete

# ✈️ Customer Booking Prediction

Predict whether a customer will complete a flight booking based on behavioral and trip-related variables.

---

## 📌 Project Overview

This project is part of a machine learning task focused on classification. The goal is to build a model that can predict whether a customer will complete their flight reservation. The dataset includes both behavioral and transactional features.

---

## 🧮 Dataset Summary

- **Total samples:** 50,000
- **Target variable:** `booking_complete` (0 = not completed, 1 = completed)
- **Selected features:**
  - `length_of_stay` (numeric)
  - `flight_duration` (numeric)
  - `flight_day` (categorical)
  - `sales_channel` (categorical)
  - `trip_type` (categorical)
  - `wants_extra_baggage` (int64)
  - `wants_preferred_seat` (int64)

---

## ⚙️ Methodology

1. **Data Exploration**
   - Feature distribution analysis (numerical and categorical)
   - Dropped non-informative features (e.g., `route`)

2. **Data Preparation**
   - Label encoding for categorical variables
   - Train-test split with stratification
   - Applied **class_weight** and **SMOTE** to balance the target variable

3. **Model Training**
   - Algorithm: `RandomForestClassifier`
   - Tuned with `random_state` for reproducibility
   - Selected for its ability to interpret feature importance

4. **Model Evaluation**
   - Accuracy: **69%**
   - F1-Score (Class 1): **0.28**
   - Recall (Class 1): **0.41**
   - Evaluation via confusion matrix and feature importance plot

---

## 📈 Results


---

## 🧠 Insights

- Most important variables:  
  - `length_of_stay`, `flight_duration`, `flight_day`
- Despite class imbalance, SMOTE allowed the model to identify class 1 with ~41% recall.
- Future performance can improve with behavioral features (e.g., device type, browsing history).

---
