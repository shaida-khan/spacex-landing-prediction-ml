# Falcon 9 Landing Success Prediction 🚀

## 🚀 Open the Project

👉 [01 Data Collection](./01_API_Data_Collection.ipynb)  
👉 [02 Data Cleaning & Wrangling](./02_Data_Wrangling_and_Cleaning.ipynb)

## 📌 Overview

This project predicts the success of SpaceX Falcon 9 first-stage landings using machine learning.  

An end-to-end pipeline was built using data collected from the SpaceX API, including data cleaning, feature engineering, exploratory analysis, and model evaluation.  

The objective is to identify key factors influencing landing success and support data-driven decision making in aerospace operations.

The goal is to understand which factors most strongly influence landing success and compare baseline and ensemble models under class imbalance.

---

## Data Source

- **SpaceX REST API (v4)**
  - `/v4/launches/past`
  - `/v4/rockets/{id}`

Only **Falcon 9 launches** were retained for analysis.

---

## Project Structure

├── 01_API_Data_Collection.ipynb
├── 02_Data_Wrangling.ipynb
├── data/
│ ├── falcon9_step1_api_data.csv
│ ├── falcon9_step2_cleaned.csv


---

## 🔧 Features

- `core_flight` — Number of flights for the booster
- `core_reused` — Whether the booster was reused
- `landing_type` — ASDS, RTLS, Ocean
- `landpad` — Landing pad identifier (one-hot encoded)

**Target variable**

- `Class` → `1 = successful landing`, `0 = failed landing`

---

## Models Trained

- **Logistic Regression** (baseline)
- **Random Forest Classifier** (balanced class weights)

---

## 📊 Results Summary

| Model | Accuracy | Strengths | Limitations |
|------|----------|-----------|-------------|
| Logistic Regression | ~94% | High recall for successful landings | Lower detection of failed landings |
| Random Forest | ~77% | Better at detecting failed landings | Lower overall accuracy |

### Key Insights

- Logistic Regression performs well in predicting successful landings  
- Random Forest improves detection of failed landings  
- Model trade-off observed between accuracy and failure detection
---

## 🤖 Models Used

- Logistic Regression  
- Random Forest  
- Model comparison and evaluation (Accuracy, Recall)

## Tools & Libraries

- Python
- Pandas, NumPy
- Scikit-learn
- Matplotlib

---

## Author
**Shaida**  
IBM Data Science Professional Certificate
