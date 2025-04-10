# Estimating Influenza Cases using Numerical Methods and Machine Learning

## Overview

This project compares traditional numerical approaches with modern machine learning models for predicting **H1N1 influenza cases** using real outbreak data from São Paulo, Brazil. The analysis was conducted as part of the **CS5513 - Numerical Computation** course at **Oklahoma State University (Spring 2024)**.

## Core Objectives

- Apply Midpoint, Modified Euler, and RK4 methods on SVIR differential equations.
- Build deep learning models (1D-CNN, LSTM, FTA-LSTM) and a Random Forest regressor.
- Evaluate forecasting performance using **Mean Absolute Error (MAE)**.
- Compare **Direct Forecast** vs. **Rolling Forecast** strategies.

## Dataset

Weekly reported cases from a real **H1N1 outbreak in São Paulo (2009–2010)**.
Initial infected population: 1  
Model used: **SVIR (Susceptible-Vaccinated-Infected-Recovered)**

## Implemented Models

### 🧮 Numerical Methods
- **Midpoint Method**
- **Modified Euler (Heun's Method)**
- **Runge-Kutta 4 (RK4)**

### 🤖 Machine Learning
- **1D CNN** — Feature extractor for time series.
- **LSTM** — Recurrent model capturing sequential trends.
- **FTA-LSTM** — Attention-augmented LSTM for time and feature learning.
- **Random Forest** — Ensemble-based regressor (best performing).

## Evaluation Metric

- **Mean Absolute Error (MAE)**

| Model                  | MAE (Test) |
|------------------------|------------|
| Midpoint               | 44.35      |
| Modified Euler         | 44.31      |
| RK4                    | 44.35      |
| 1D CNN (Direct)        | 25.05      |
| LSTM (Direct)          | 20.49      |
| FTA-LSTM (Direct)      | 24.16      |
| Random Forest (Direct) | **14.67**  |

## Key Insights

- Numerical methods are consistent but less adaptive for longer forecasts.
- **Random Forest (Direct Forecast)** achieved the lowest prediction error.
- Rolling forecasts suffer from error propagation, leading to flat second peak predictions.
- ML models outperform numerical solvers in capturing real-world non-linear dynamics.

## How to Run

1. Clone the repo:
```bash
git clone https://github.com/CopotronicRifat/Numerical-Methods-for-Estimating-Influenza-Cases.git
```

2. Open and run the Jupyter notebooks in your local or Colab environment.

## License

MIT License

## Author

**Rifat Rafiuddin**  
Oklahoma State University – CS5513 (Spring 2024)

