# Impact of Policy Changes on Work Permits in Canada (2010–2029)  
![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python)  
![License](https://img.shields.io/badge/License-MIT-green)  
![Last Commit](https://img.shields.io/github/last-commit/harwinderjitsingh/Impact-of-Policy-Changes-on-Work-Permits-in-Canada-2010-2024-with-a-5-Year-future-Trends-2024-2029-)  

## 📌 Overview  
This project analyzes historical trends (2010–2024) and forecasts future work permit issuances in Canada (2024–2029) using **time series forecasting** (SARIMA) and **machine learning** (XGBoost, Random Forest). The goal is to evaluate how policy changes impact permit volumes, aiding policymakers, employers, and educational institutions in workforce planning.  

## 🔎 Research Questions  
1. **How accurately can work permit issuance be forecasted?**  
   - Evaluated using Mean Absolute Error (MAE) across SARIMA, XGBoost, and Random Forest models.  
2. **Which modeling approach yields the best results?**  
   - Compared traditional time-series (SARIMA) with ensemble ML methods (XGBoost/Random Forest).  
3. **What are the key drivers of work permit trends?**  
   - Analyzed policy impacts, country-specific patterns, and institutional contributions.  

---

## 🔍 Key Insights  
- **Approval Rates**: 85% average approval rate (70–95% range).  
- **Country Trends**: India dominates permit issuance (4× more than UK/USA).  
- **Institutions**: Private institutions process 43.5% of permits (vs. 34.1% colleges, 22.4% universities).  
- **Model Performance**: SARIMA outperformed with **MAE of 1,879.89**.  
- **Forecast**: 466.17K permits projected for 2025–2029, with seasonal peaks in Q3.  

---

## 📂 Dataset  
**Source**: [Immigration, Refugees and Citizenship Canada (IRCC)](https://open.canada.ca/data/en/dataset/052642bb-3fd9-4828-b608-c81dff7e539c)  

**Features**:  
- Temporal: Year, month, policy change dates.  
- Permit Metrics: Issued/expired counts, renewal rates, acceptance rates.  
- Contextual: Country of origin, institution type, program level, unemployment/job vacancy rates.  
- Policy Impact: Categorized as positive/neutral/negative.  

---

## 🛠️ Methodology  
### 1. **Data Preprocessing**  
- Handled missing values, duplicates, and datetime conversion.  
- Feature engineering for numeric variables (e.g., lag features for time series).  

### 2. **Models**  
| Model          | Use Case                  | Hyperparameters      |  
|----------------|---------------------------|----------------------|  
| **SARIMA**     | Long-term seasonal trends | Optimized via grid search |  
| **XGBoost**    | Short-term predictions    | `n_estimators=100`   |  
| **Random Forest** | Feature importance      | `n_estimators=100`   |  

### 3. **Evaluation**  
- **Metric**: Mean Absolute Error (MAE).  
- **Results**:  
  - SARIMA: MAE = 1,879.89  
  - XGBoost: MAE = 2,450.32  
  - Random Forest: MAE = 2,512.15  

---

## 📊 Dashboards  
### Historical Trends (2015–2020)  
- **65K permits issued** vs. **32K expired**.  
- **Job Vacancies**: Master’s programs had highest demand (42.83%).  
- **Top Countries**: Philippines, Nigeria, Ghana led in permit volumes.  

### Forecasting (2025–2029)  
- **466.17K permits projected**, with cyclical fluctuations.  
- Interactive filters for year/range exploration.  

![Dashboard Preview](media/image21.jpeg)  

---

## 🚀 Installation  
```bash  
git clone https://github.com/Harwinderjitsingh/Impact-of-Policy-Changes-on-Work-Permits-in-Canada-2010-2024-with-a-5-Year-future-Trends-2024-2029-.git  
cd Impact-of-Policy-Changes-on-Work-Permits-in-Canada-2010-2024-with-a-5-Year-future-Trends-2024-2029-  
pip install -r requirements.txt  # Install dependencies  
