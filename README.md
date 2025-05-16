# Lag-Llama for Indonesian Stock Market Forecasting

This repository contains the source code, dataset, and experimental results for our paper:

**"Evaluating Lag-Llama for Probabilistic Time Series Forecasting in the Indonesian Stock Market: A Comparative Study of Univariate and Multi-Time Series"**

## 📈 Overview

Accurately predicting stock prices is crucial for investors and policymakers. This study presents the first empirical evaluation of **Lag-Llama**, a novel probabilistic time series forecasting model, applied to the **Indonesian Stock Exchange (IDX)**. We explore its forecasting capability on both **univariate** and **multi-time series** datasets of top Indonesian stocks.

### 🔍 Objective

Evaluate Lag-Llama's effectiveness in modeling temporal patterns and market volatility compared to state-of-the-art models:

- **DeepAR** (Recurrent Neural Network)
- **Temporal Fusion Transformer (TFT)**

## 🧪 Key Findings

- On a **combined dataset of BBCA, BMRI, and AMRT**, Lag-Llama achieves:
  - **CRPS = 0.0195**, closely matching TFT (**0.0179**) and outperforming DeepAR (**0.0270**)
- On **broader stock groups**, performance drops:
  - e.g., **Top 1–9 stocks** → **CRPS = 0.0517**
- **Lag-Llama** shows strong potential when forecasting **select, related stocks**, offering high precision and reliability.

## 📂 Repository Structure

```
.
├── data/                   # Normalized price data for IDX stocks
├── notebooks/             # Jupyter notebooks for preprocessing, training, evaluation
├── results/               # CRPS scores and result tables
└── README.md              # Project overview
```

## ⚙️ Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/yourusername/lag-llama-id-stock.git
cd lag-llama-id-stock
```

### 2. Set up the environment

We recommend using a virtual environment:

```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt
```

### 3. Run the experiments

You can start by opening the notebooks under the `notebooks/` directory or running:

```bash
python main_lag_llama.py --config configs/combined_bbca_bmri_amrt.json
```

## 📊 Evaluation Metric

We use the **Continuous Ranked Probability Score (CRPS)** to evaluate the quality of probabilistic forecasts. Lower CRPS values indicate better model performance.

## 📈 Datasets

The dataset contains normalized daily stock price data of the 18 most valuable IDX stocks (Q2 2024). See `data/README.md` for stock names and preprocessing details.

## 📃 Citation

If you use this code or data, please cite our paper (citation coming soon).

## 🔒 License

This project is released under the MIT License. See `LICENSE` for details.

## 🤝 Contact

For questions or collaborations, please reach out to:

**Arbi Haza Nasution**  
Universitas Islam Riau 
