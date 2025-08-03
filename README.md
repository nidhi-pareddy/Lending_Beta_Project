# Lending Beta Project

This repository contains the code and documentation for the **Lending Beta Project**, which seeks to quantify and classify the sensitivity of lending activity across U.S. Metropolitan Statistical Areas (MSAs) to broader macroeconomic conditions. The project introduces a `Lending Beta` metric for each MSA, derived from comparing local lending trends (LEAP) to national economic activity (MEAP), and supports downstream analysis of cyclical behavior in different regions.

## 📊 Project Goals

- Calculate a "Lending Beta" for each MSA to represent responsiveness to national economic conditions.
- Categorize MSAs into **Procyclical**, **Neutral**, **Countercyclical**, and **Hyper-Procyclical** groups.
- Explore correlations between beta values and Credit Union (CU) counts within each MSA.
- Visualize and interpret beta distributions and their connection to MSA characteristics.

## 📁 Repository Structure
├── data/ # Raw and cleaned input datasets (e.g., LEAP, MEAP, CU data, MSA mapping)
├── notebooks/ # Jupyter notebooks for exploratory analysis and visualization
├── scripts/ # Core preprocessing and analysis code
├── output/ # Merged datasets, plots, and final classification results
├── README.md # Project documentation


## 🧮 Key Concepts

- **LEAP (Local Economic Activity Proxy):** Measures local lending volume trends per MSA.
- **MEAP (Macroeconomic Activity Proxy):** Aggregated national economic trends (e.g., GDP, unemployment, CPI).
- **Lending Beta:** Calculated using OLS regression between LEAP (y) and MEAP (x) per MSA to measure economic sensitivity.
- **Beta Classifications:**
  - `High Beta`: Highly procyclical lending (e.g., β > 1.5 or in top quantiles)
  - `Low Beta`: Countercyclical or negative β
  - `Mid Beta`: Typical or stable lending behavior

## 📌 Methodology Summary

1. **Data Cleaning:** Merge and align LEAP and MEAP datasets by date and MSA.
2. **Beta Calculation:** Use regression to estimate Lending Beta per MSA.
3. **Classification:** Categorize MSAs based on Lending Beta distribution.
4. **Credit Union Integration:** Map ZIP codes to MSAs and count number of CUs in each.
5. **Exploratory Visualizations:** 
   - Histogram of Beta values by classification
   - CU count distributions per beta group
   - CU count vs Beta comparisons

## 🔍 Insights

- MSAs with extreme Lending Beta values (very high or very low) tend to have significantly **fewer Credit Unions**.
- Credit union presence might act as a proxy for economic diversity or financial resilience at the regional level.

## 📦 Dependencies

- Python 3.x
- pandas
- numpy
- seaborn
- matplotlib
- statsmodels
