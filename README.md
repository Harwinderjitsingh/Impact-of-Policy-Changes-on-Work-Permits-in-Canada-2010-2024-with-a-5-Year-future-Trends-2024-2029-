# Impact of Policy Changes on Work Permits in Canada (2010–2029)
![Bitcoin Dashboard](https://img.shields.io/badge/Powered%20By-Python-blue?logo=python) 
![License](https://img.shields.io/badge/License-MIT-green)
![Last Commit](https://img.shields.io/github/last-commit/harwinderjitsingh/Impact-of-Policy-Changes-on-Work-Permits-in-Canada-2010-2024-with-a-5-Year-future-Trends-2024-2029-)


## 📌 Overview
This project analyzes historical trends and forecasts future work permit issuances in Canada (2010-2024) with 5-year projections (2024-2029). Combining time series analysis and machine learning, we evaluate how policy changes impact permit volumes to support data-driven immigration decisions.

## 🔍 Key Insights
- **85% average approval rate** for work permits (70-95% range)
- **India dominates permit issuance** (4x more than other countries)
- **Private institutions process 43.5%** of permits (vs 34.1% colleges, 22.4% universities)
- **SARIMA model outperformed** others with MAE of 1,879.89

## 📂 Dataset
Source: [Immigration, Refugees and Citizenship Canada (IRCC)](https://open.canada.ca/data/en/dataset/052642bb-3fd9-4828-b608-c81dff7e539c)

**Key Features:**
- Monthly permit issuance/expiry (2010-2024)
- Country of origin
- Institution types
- Policy change impacts
- Economic indicators (unemployment/job vacancy rates)

## 🛠️ Methodology
1. **Data Processing**
   - Handled missing values & duplicates
   - Feature engineering for temporal patterns

2. **Models Compared**
   - **SARIMA** (for seasonal trends)
   - **Random Forest** (n_estimators=100)
   - **XGBoost** (n_estimators=100)

3. **Evaluation Metric**
   - Mean Absolute Error (MAE)

## 📈 Results
| Model       | MAE     | Best For               |
|-------------|---------|------------------------|
| SARIMA      | 1,879.89| Long-term forecasting  |
| XGBoost     | 2,450.32| Short-term predictions |
| Random Forest| 2,512.15| Feature importance     |

**Forecast Highlights:**
- Expected **X% increase** in permits by 2029
- Seasonal peaks in **Q3 annually**
- Policy changes correlate with **±15% volume fluctuations**

## 🖥️ Installation
```bash
git clone https://github.com/yourusername/work-permit-forecasting.git
cd work-permit-forecasting
pip install -r requirements.txt
