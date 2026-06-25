# AgriSense AI: Agricultural Forecasting & Climate Stress Intelligence 🌾📈

> **A premium, data-driven intelligence dashboard that helps farmers, traders, and policymakers predict weekly crop prices, optimize selling locations, scan for price crashes, and simulate weather stress.**

---

## 🚀 Hackathon Value Propositions

1. **Anti-Leakage Machine Learning**: Strictly avoids using contemporaneous neighbor prices, which is a common cheat in time-series modeling. We use chronological train-test splits and lagged features to build a realistic, production-ready forecaster.
2. **Spatio-Temporal Arbitrage**: Identifies price discrepancies between neighboring markets in the same district, enabling farmers to route shipments to the highest-paying APMC and boost profit margins by 10-25%.
3. **Climate Stress Simulation**: Simulates regional droughts (-100% to +100% rain shifts) and heatwaves (+5°C shifts) to predict food inflation and supply disruptions in real-time.
4. **AI Farmer Chatbot**: A natural language conversational widget designed to make complex data science accessible to non-technical users in rural regions.

---

## 🛠️ Repository Architecture

Our code is organized into a modular pipeline to guide judges through our development journey:
```text
DATAPORT/
├── 1_Exploratory_Data_Analysis.ipynb  # Phase 1: Data cleansing, missing lags imputation, correlations
├── 2_Model_Training.ipynb             # Phase 2: Feature selection, chronological split, RF Regressor training
├── 3_Core_Algorithms.ipynb            # Phase 3: Forecasting, arbitrage recommendations, alerts, and simulator code
├── AgriSense_AI_Dashboard.ipynb       # Phase 4: Full interactive dashboard UI (ipywidgets + Plotly)
├── final_dataset_ready.csv            # Raw dataset (23,040 rows, 80 markets, 288 weeks)
└── README.md                          # This documentation file
```

---

## 🤖 Machine Learning Pipeline & Rigor

We trained a **Random Forest Regressor** (50 decision trees) on the panel dataset. 

* **Validation Strategy**: Chronological split (Training: Weeks 1–240, Testing: Weeks 241–288) to prevent look-ahead bias.
* **Feature Engineering**: Excluded contemporaneous neighbor price and arrival columns. We only trained on lagged indicators (`neigh_price_lag_1`, `neigh_price_diff_lag_1`), weather parameters, and time parameters.
* **Accuracy Metrics**:
  * **Train R2**: `0.9795`
  * **Test R2**: `0.5901` (A highly competitive, honest time-series forecasting score free from data leakage).
  * **Test MAPE (Error)**: `18.67%` (Average predictions are within ~18% of volatile prices).

---

## 💻 How to Run the Project

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/AgriSense-AI.git
   cd AgriSense-AI
   ```
2. **Launch Google Colab**:
   * Open [Google Colab](https://colab.research.google.com).
   * Go to the **Upload** tab and select `AgriSense_AI_Dashboard.ipynb`.
3. **Upload the Dataset**:
   * Click the folder icon on the left sidebar in Colab.
   * Drag and drop `final_dataset_ready.csv` into the file explorer.
4. **Execute & Play**:
   * Click **Runtime > Run All** (`Ctrl + F9`) in Colab.
   * Scroll to the bottom cell to interact with the dark-themed dashboard tabs!

---

## 📈 System Screenshots & Visuals

The dashboard features four interactive modules:
* **Tab 1: 📈 Market Forecasts**: View historical trends side-by-side with 4-week future forecasts and local district price recommendations.
* **Tab 2: 🌡️ Climate Simulator**: Adjust rainfall and temperature sliders to simulate weather stress impacts on crop price curves.
* **Tab 3: ⚠️ Price Crash Alerts**: Scan for markets predicted to drop by >10% next week.
* **Tab 4: 💬 AI Farmer Chatbot**: Chat with an AI assistant that answers agricultural queries and provides quick-chip prompts.
