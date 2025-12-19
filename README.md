# Mutual Fund Performance Predictor

Predicts top-performing mutual funds across **1-year, 3-year, and 5-year horizons** using machine learning.

## Overview
This project uses historical mutual fund data (~4000 funds with 25+ features) to **classify and rank top-performing funds**.  
We build a **Random Forest classifier** for each horizon and generate a **combined consistency score** to identify funds consistently performing well.

### Key Features Used
- `expense_ratio` – Fund’s expense ratio (%)  
- `fund_size_cr` – Fund size in crores  
- `sharpe` – Sharpe ratio  
- `beta` – Beta  
- `alpha` – Alpha  
- `sortino` – Sortino ratio  
- `min_sip` – Minimum SIP amount  
- `min_lumpsum` – Minimum lump sum investment  
- `fund_age_yr` – Fund age in years  
- Additional features: fund manager, rating, category, sub-category, risk level

## Dataset
- Total funds: 647  
- Total features: 28  
- Source: Mutual Funds India - Detailed(kaggle)  

## Model Performance
| Horizon | Accuracy | ROC-AUC |
|---------|---------|---------|
| 1-year  | 0.81    | 0.82    |
| 3-year  | 0.91    | 0.94    |
| 5-year  | 0.85    | 0.91    |

## Outputs
- **Top predicted funds** for 1-year, 3-year, and 5-year horizons with probability scores  
- **Combined consistency score** to identify consistently top-performing funds  
- Outputs saved in `output/` folder:  
  - `top_fund_1yr.csv`  
  - `top_fund_3yr.csv`  
  - `top_fund_5yr.csv`  

## How to Run
1. Clone the repository:
git clone https://github.com/<your-username>/mutual-fund-predictor.git
cd mutual-fund-predictor

2. Install dependencies:
pip install -r requirements.txt

3. Run Jupyter Notebook
jupyter notebook mutual_fund_prediction.ipynb

4.The top predicted funds and outputs will be saved in the output/ folder.
