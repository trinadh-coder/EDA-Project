# Exploratory Data Analysis (EDA) on Vehicle Sales Dataset

## 📌 Project Overview
An end-to-end Exploratory Data Analysis (EDA) project on a vehicle sales dataset (`vehicle_sales_dirty.csv`) focusing on data cleaning, missing value imputation, text standardization, feature encoding, outlier detection, and multi-level visualizations.

---

## 🛠️ Key Pipeline Steps

1. **Data Cleaning & Imputation:**
   * Filled missing numerical values using **Mean Imputation**.
   * Filled missing categorical attributes using **Mode Imputation**.
   * Dropped redundant duplicate columns (`Brand_dup`, `Selling_Price_dup`).
   * Standardized irregular casing across categorical text (`Brand`, `Fuel_Type`, `Transmission`, `Seller_Type`).
   * Ordinal encoded `Owner` categories (`First` $\rightarrow 1$, `Second` $\rightarrow 2$, `Third` $\rightarrow 3$).

2. **Outlier Detection:**
   * Used the **Interquartile Range (IQR) method** ($1.5 \times \text{IQR}$) across all numerical features to check for extreme values.

3. **Data Visualizations:**
   * **Univariate:** Histograms, KDE plots, Box plots, and Count plots for single-variable distributions.
   * **Bivariate:** Scatter plots, grouped Box plots, and Bar plots to compare feature relationships with `Selling_Price`.
   * **Multivariate:** Correlation Heatmaps, 3-variable Scatter plots, and Pairplots to analyze complex feature interactions.

---

## 🚀 Tech Stack
* **Language:** Python
* **Libraries:** `pandas`, `numpy`, `matplotlib`, `seaborn`


## FINAL REPORT
*Primary Valuation Driver: Original vehicle cost (Present_Price) and Brand prestige are the strongest predictors of resale price (Selling_Price).

Feature Premiums: Automatic transmission vehicles systematically command higher average resale valuations across all fuel types compared to manual models.

Depreciation Dynamics: High odometer readings (Driven_KMs) reduce market value as expected, though luxury brands buffer against sharp usage-based depreciation.

Data Integrity: After mean/mode imputation and text standardization, the dataset contains 0 statistical outliers across all numerical attributes, making it completely clean and ML-ready.
