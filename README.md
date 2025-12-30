# Trader Behavior Insights – Data Science Assignment

**Candidate Name:** [Yagna Suthar]  
**Email:** [yagna.suthar@gmail.com]  
**Mobile Number:** [+91-9265679968]  

---
## Google colab links 
**Notebook_1:** https://colab.research.google.com/drive/1eh8yq20Mrq5iqiN9wMJYgDsP-ARefhfL?usp=sharing
**Notebook_2:** https://colab.research.google.com/drive/10mmhQ-eWONCMEYVRsfN1gq-cPaBNYzny?usp=sharing



## Project Overview

This project analyzes the relationship between **trader behavior** and **Bitcoin market sentiment**. Using historical trader data from Hyperliquid and the Bitcoin Fear & Greed Index, the goal is to uncover patterns in trader profitability, risk, trade volume, and fees relative to market sentiment.  

**Objective:**  
- Analyze how trading behavior (profitability, risk, volume, leverage) aligns or diverges from market sentiment (Fear vs Greed).  
- Identify hidden trends and signals that could inform smarter trading strategies in the Web3 ecosystem.  

---

## Datasets

1. **Historical Trader Data (Hyperliquid)**  
   - Contains account trades, execution price, trade size, side, timestamp, closed PnL, fee, leverage, etc.  
   - Sample columns: `Account`, `Coin`, `Execution Price`, `Size Tokens`, `Size USD`, `Side`, `Timestamp IST`, `Closed PnL`, `Fee`, `Leverage`.  

2. **Bitcoin Market Sentiment Dataset (Fear & Greed Index)**  
   - Contains daily sentiment values with classification: Fear, Extreme Fear, Greed, Extreme Greed.  
   - Normalized to two categories: `Fear` and `Greed`.  

**Dataset Links:**  
- [Historical Trader Data](https://drive.google.com/file/d/1IAfLZwu6rJzyWKgBToqwSmmVYU6VbjVs/view?usp=sharing)  
- [Fear & Greed Index](https://drive.google.com/file/d/1PgQC0tO8XN-wqkNyghWc_-mnrYv_nhSf/view?usp=sharing)  

---

## Project Structure

ds_<candidate_name>/
├── notebook_1.ipynb                # Data loading, cleaning, preprocessing, merging datasets
├── notebook_2.ipynb                # Visualizations, EDA, and insights
├── csv_files/
│   └── final_df.csv                # Cleaned and merged dataset
├── outputs/
│   ├── Trader_Profitability_by_Market_Sentiment.png
│   ├── Trade_Volume_by_Market_Sentiment.png
│   ├── Trading_Fee_by_Market_Sentiment.png
│   ├── Correlation_Between_Trade_Features.png
│   ├── scatterplot.png
│   └── Proportion_of_Profitable.png
├── ds_report.pdf                    # Complete analysis report
└── README.md                        # Project description and instructions


---

## Methodology

### 1. Data Preprocessing (Notebook 1)
- Load both datasets in Google Colab.  
- Convert date columns to `datetime` format.  
- Normalize market sentiment: `Fear` and `Extreme Fear` → `Fear`; `Greed` and `Extreme Greed` → `Greed`.  
- Drop irrelevant columns from trader dataset.  
- Merge datasets on `date` to align each trade with the corresponding sentiment.  
- Save final cleaned dataset as `csv_files/final_df.csv`.  

### 2. Exploratory Data Analysis & Visualizations (Notebook 2)
- Boxplots for **Closed PnL**, **Trade Volume (USD)**, and **Fees** against sentiment.  
- Heatmap for correlation among numeric trade features.  
- Scatterplot of `Size USD` vs `Closed PnL` (sampled 5k trades).  
- Bar chart showing **proportion of profitable trades** by sentiment.  
- Save all visualizations in `outputs/` folder.  

---

## Key Insights

- Traders trade **larger volumes during Greed periods**, reflecting market confidence.  
- Average **profitability is slightly higher during Greed**, but extreme losses can occur in any sentiment.  
- **Fees** scale with trade size; higher trade sizes → higher fees.  
- **Weak correlation** between trade size and profitability, indicating risk management is essential.  
- **Proportion of profitable trades** is slightly higher in Greed periods, suggesting sentiment-aware trading strategies can be beneficial.  

---

## Usage Instructions

1. Clone the repository:
```bash
git clone https://github.com/YagnaSuthar/ds_YagnaSuthar.git
cd ds_YagnaSuthar
