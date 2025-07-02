# 🛎️ Booking.com Hotel Rating Prediction

This project simulates the role of a data scientist at **Booking.com** tasked with uncovering potentially dishonest hotels. The method? Build a machine learning model that predicts hotel ratings based on various features of the booking. If the prediction is significantly off — something shady might be going on.

---

## 🎯 Objective

Predict the **true rating** of a hotel based on booking-related features such as:
- Hotel name
- Tags
- Booking dates
- Geolocation
- Type of stay (e.g., solo, family, short/long trip)

Hotels with large mismatches between actual and predicted ratings may require manual review.

---

## 📁 Project Structure
* EDA_Project_3_model.ipynb
* README.md
* requirements.txt

All analysis is contained within the notebook, organized into:
- 🧹 Data Cleaning
- 🔍 Exploratory Data Analysis
- 🏗️ Feature Engineering
- 📊 Model Training & Evaluation
- 🧠 Model Insights and Conclusions

---

## 🧰 Dataset Highlights

- Real Booking.com data
- Columns include:
  - `hotel_name`
  - `tags` (meta data about guest type, trip length, etc.)
  - `review_score`
  - `review_date`, `checkin_date`, etc.
  - `lat`, `lng`
  - Booking metadata (number of nights, guests, etc.)

---

## 🛠️ Feature Engineering

- Extracted temporal features (season, weekday, time since booking, etc.)
- Parsed hotel `tags` for useful clues
- Cleaned and manually imputed missing coordinates
- Added geographic distance from city center

---

## 📈 Modeling

- Baseline: Linear Regression
- Main Model: **Gradient Boosting Regressor**
- Evaluation metric: **MAE (Mean Absolute Error)**

---

## 🏁 Results

| Model                    | MAE     |
|--------------------------|---------|
| Linear Regression        | ~0.54   |
| Gradient Boosting        | **~0.42** |

> Note: Lower MAE indicates better accuracy in predicting hotel ratings.

---

## 🔎 Use Case

Hotels with a **large gap** between their actual and predicted scores may be flagged for review. This approach can be integrated into Booking’s internal trust and safety tools.

---

## 📦 Requirements

- Python 3.8+
- pandas, numpy
- seaborn, matplotlib
- scikit-learn
- xgboost

Install dependencies with:

```bash
pip install -r requirements.txt
