# 🚗 Uber Trip Analysis — Advanced ML Project

An end-to-end advanced data science project analyzing Uber trip demand in NYC using machine learning and time series forecasting.

---

## 📋 Project Overview

| | |
|---|---|
| **Domain** | Data Analyst / Data Scientist |
| **Level** | Advanced |
| **Tools** | Python, Jupyter Notebook, Google Colab |
| **Dataset** | Uber-Jan-Feb-FOIL.csv (Jan–Feb 2015) |
| **Records** | 4,130,230 trips · 6 base companies · 59 days |

---

## 📁 Project Structure
```
uber-trip-analysis/
│
├── uber_trip_analysis.ipynb   # Main notebook (EDA + ML + Dashboard)
├── Uber-Jan-Feb-FOIL.csv      # Dataset
└── README.md                  # Project documentation
```

---

## 📊 Dataset

**Source:** NYC Taxi & Limousine Commission (TLC) via FiveThirtyEight FOIL request

**Columns:**
| Column | Description |
|---|---|
| `dispatching_base_number` | TLC base company code |
| `date` | Trip date |
| `active_vehicles` | Number of active vehicles that day |
| `trips` | Number of trips dispatched |

**Base Companies:**
| Code | Name |
|---|---|
| B02512 | Unter |
| B02598 | Hinter |
| B02617 | Weiter |
| B02682 | Schmecken |
| B02764 | Danach-NY |
| B02765 | Grun |

---

## 🔍 Project Steps

1. **Data Preprocessing** — Load, clean, parse dates, engineer features
2. **EDA** — Trips by base, day of week, daily trend, vehicle efficiency
3. **Time Series Analysis** — Seasonal decomposition (period=7 days)
4. **Feature Engineering** — 7-day lagged window features
5. **ML Models** — XGBoost, Random Forest, GBRT with GridSearchCV + TimeSeriesSplit
6. **Ensemble Model** — Weighted average using inverse MAPE
7. **Model Comparison** — MAPE comparison across all models
8. **Interactive Dashboard** — Chart.js dashboard embedded in Colab

---

## 🤖 Model Results

| Model | MAPE | Notes |
|---|---|---|
| XGBoost | Best | Strongest individual model |
| Random Forest | Mid | Solid but behind XGBoost |
| GBRT | Mid | Competitive, slowest to train |
| **Ensemble** | **Most stable** | Recommended for production |

---

## 💡 Key Findings

- 📈 Trips grew **16.4%** from January to February 2015
- 🏆 **Danach-NY** handled **46.4%** of all trips — clear market leader
- 📅 **Saturday** was consistently the busiest day every week
- ⚡ **Schmecken** was the most efficient base — highest trips per vehicle
- 🔄 Strong **7-day seasonal cycle** confirmed by decomposition
- 🎯 XGBoost + Ensemble captured weekly patterns with high accuracy

---

## 🚀 How to Run

1. Open [Google Colab](https://colab.research.google.com)
2. Upload `uber_trip_analysis.ipynb`
3. Run **Cell 1** to install dependencies
4. Run **Cell 2** — upload `Uber-Jan-Feb-FOIL.csv` when prompted
5. Run all remaining cells top to bottom

---

## 📦 Dependencies
```
pandas
numpy
matplotlib
seaborn
scikit-learn
xgboost
statsmodels
```

Install all at once:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost statsmodels
```

---

## 📌 Next Steps

- Load all 6 monthly raw files (Apr–Sep 2014) for longer trend analysis
- Add external features — weather, holidays, city events
- Try Facebook Prophet or LSTM for deeper forecasting
- Deploy dashboard as a live Streamlit app

---

## 👤 Author<img width="1762" height="703" alt="Screenshot 2026-03-17 123027" src="https://github.com/user-attachments/assets/edbdfcec-59c8-49e5-8c23-7fccd10be78f" />


Made as part of the **Unified Mentor** Data Analyst & Data Scientist project series.<img width="1670" height="696" alt="Screenshot 2026-03-17 123043" src="https://github.com/user-attachments/assets/44e0d0b4-ebab-4cce-b097-70468903e95f" />
