# Hybrid EGARCH–BiLSTM Model for Explainable Gold Price Prediction

## Project Overview
This repository contains the code and data used for the MSc Data Science final year project titled:

**Hybrid EGARCH–BiLSTM Model for Explainable Gold Price Prediction**

The project investigates whether explicitly modelling conditional volatility using EGARCH can improve the stability, accuracy, and interpretability of deep learning–based gold price forecasting.

---

## Dataset Description and Rationale

Two datasets are used in this project for distinct and methodologically justified purposes:

### 1. Exploratory Data Analysis Dataset (2016–2025)
- **File:** `Gold Futures Historical Data-7.csv`
- **Notebook:** `EDA.ipynb`
- **Purpose:**
  - Long-term exploration of gold price behaviour
  - Identification of volatility clustering, regime persistence, and structural patterns
  - Contextual analysis of major global events (e.g. COVID-19, inflationary periods)

This dataset is **not used for model training or evaluation** and serves purely exploratory and descriptive purposes.

---

### 2. Modelling and Forecasting Dataset (2018–2025)
- **File:** `Gold Futures Historical Data-10.csv`
- **Notebook:** `BILSTM-EGARCH_model.ipynb`
- **Purpose:**
  - Training and evaluation of the forecasting models
  - EGARCH volatility estimation
  - One-day-ahead gold price prediction under realistic conditions

The modelling period is deliberately restricted to **2018–2025** to reflect more recent market dynamics and avoid over-reliance on older structural regimes.

---

## Methodology Summary

- EGARCH is used to estimate conditional volatility from gold log returns.
- Smoothed EGARCH volatility is incorporated as an exogenous input to:
  - LSTM (baseline model)
  - BiLSTM (proposed model)
- Forecasting is performed on gold Close prices using rolling windows.
- Strict chronological splits are applied to prevent data leakage.

---

## Repository Structure


