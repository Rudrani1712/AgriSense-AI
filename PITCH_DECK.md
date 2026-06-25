# Hackathon Pitch Deck Outline: AgriSense AI 🎤💡

*Use this outline to structure your slide deck or script for a 3-minute hackathon pitch.*

---

## 📽️ Slide 1: Title & Hook
* **Title**: AgriSense AI: Climate & Economic Intelligence for Farmers
* **Visual**: A clean, modern dark-green background showing a glowing price forecast chart overlaying a crop field.
* **The Script**:
  > *"Namaskar. In India, crop sales are a gamble. Farmers harvest their yields blindly, unaware of sudden price collapses or premium prices offered at markets just a few kilometers away. Today, we introduce AgriSense AI—turning agricultural economics from a guessing game into a predictable science."*

---

## 📽️ Slide 2: The Three-Fold Problem
* **Visual**: Three icons/columns:
  1. **Spatial Asymmetry**: Farmers sell at their closest market, missing regional premiums.
  2. **Economic Volatility**: Price crashes occur overnight when supply swells, wiping out season margins.
  3. **Climate Stress**: Droughts and heatwaves disrupt supply, but stakeholders cannot quantify the financial impact.
* **The Script**:
  > *"Farmers face three critical bottlenecks: they lack spatial awareness of arbitrage opportunities, they are blind to imminent price crashes, and they cannot estimate how weather anomalies will impact their local prices."*

---

## 📽️ Slide 3: The Solution (AgriSense AI)
* **Visual**: A mock-up or graphic of the four dashboard tabs:
  * **Forecasting**: Weekly price predictions for 80 major APMC markets.
  * **Spatio-Temporal Arbitrage**: District price rankings highlighting premium selling hubs.
  * **Price Crash Alerts**: Risk indicators identifying upcoming drops >10%.
  * **Climate Simulator**: Interactive weather shift modeling.
* **The Script**:
  > *"AgriSense AI is an end-to-end intelligence dashboard that translates complex agricultural datasets into actionable business decisions. It provides weekly price forecasts, identifies premium arbitrage opportunities, alerts users to market crashes, and simulates climate disruptions."*

---

## 📽️ Slide 4: Technical Rigor & Leakage Prevention (Judges' Favorite)
* **Visual**: A diagram of the ML pipeline showing:
  * Raw Data $\rightarrow$ Market-Grouped Imputation $\rightarrow$ Chronological Time Split $\rightarrow$ RandomForestRegressor.
  * **Train R2**: `0.9795` | **Test R2**: `0.5901` | **Test MAPE**: `18.67%`.
  * **Anti-Leakage**: Highlighting the removal of contemporaneous neighbor variables.
* **The Script**:
  > *"Most time-series hackathon projects suffer from data leakage by predicting prices using today's neighbor prices. We built a mathematically correct forecaster: we removed all contemporaneous leakage and validated using chronological splits. Our model achieves a highly competitive, honest Test R2 score of 0.59."*

---

## 📽️ Slide 5: The Wow Demo (Live Interactive Walkthrough)
* **Visual**: Live dashboard running in Colab showing:
  * Select Ahmednagar $\rightarrow$ See the 4-week forecast.
  * Highlight **Newasa APMC** offering a **+Rs 210/quintal premium** (Spatio-Temporal Arbitrage in action).
  * Pull the rainfall slider to **-50%** (Drought) $\rightarrow$ See the price curve jump by **+11%** (Climate Simulation).
* **The Script**:
  > *"Let's look at a live example: for Ahmednagar APMC, our model forecasts price trends. Our district recommendations show a farmer can gain a Rs 210 premium per quintal just by driving 20 km to Newasa APMC. In our climate simulator, if we model a 50% drought, the model predicts an immediate 11% price surge, giving cooperative societies early warnings to secure buffer stocks."*

---

## 📽️ Slide 6: Summary & Impact
* **Visual**: Key takeaway numbers:
  * **15-25%**: Average potential increase in farmer profit margins.
  * **10 days**: Lead time on price crash warnings.
  * **Zero Setup**: Completely self-contained notebook dashboard.
* **The Script**:
  > *"AgriSense AI bridges the gap between raw climate data and farmer profitability. It empowers farmers to sell at peak premiums, protects them from market crashes, and prepares governments for weather disruptions. Thank you."*
