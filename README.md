# Stock Market and Financial Analysis of Big Tech Company

## 1. Problem & User 
**Problem:**
the relationship between corporate financial performance and stock returns across three major tech firms (Apple, Microsoft, Alphabet) from 2020 to 2024.    
**Target user:**
long-term equity investors.

## 2. Data 
All data was obtained from the WRDS (Wharton Research Data Services) platform. Stock market data was retrieved from the CRSP daily stock file and includes daily closing price, daily return, and trading volume. Financial statement data was retrieved from the Compustat Fundamentals Annual file and includes revenue, net income, EBITDA, research and development expense, total assets, and total equity. The sample covers the period from 1 January 2020 to 31 December 2024, and data was accessed in 17 April 2026.

## 3. Methods (main Python steps)
The analysis was performed in Python using a Jupyter Notebook. The main steps are summarised as follows.

Stock and financial data were extracted from WRDS using SQL queries within the `wrds` Python package. Date columns were converted to datetime format and a year variable was created for annual aggregation. For the stock data, daily observations were grouped by ticker and year to calculate average price, mean daily return, total volume, and the standard deviation of daily returns as a measure of volatility. For the financial data, items were aggregated by ticker and year, and several financial ratios were computed, including net profit margin, EBITDA margin, R&D intensity, return on assets (ROA), and return on equity (ROE).

The two datasets were merged on company and year. A simple risk-adjusted return metric was calculated by dividing the mean daily return by return volatility. Line charts were created to visualise trends in average stock price, revenue, ROE, and ROA.

## 4. Key Findings 
- Apple’s persistently high ROE (over 150%) demonstrates that strong profitability and capital structure management support long-term stock performance.
- Microsoft’s industry-leading operational efficiency (50%+ EBITDA margin in 2024) delivers more stable risk-adjusted returns and market resilience.
- Google’s high ongoing R&D intensity (14–15% annually) corresponds with greater earnings and stock price volatility.
- All three firms saw synchronized negative returns in the 2022 sector downturn, proving profitability buffers downside risks during market shocks.
- Stronger and more stable long-term financial performance is closely positively correlated with more resilient, less volatile stock returns.

## 5. How to run 
1. Ensure a valid WRDS account and a working Python environment are prepared in advance.
2. Open `acc102_miniassignment_notebook.ipynb` and replace the placeholder WRDS username with your own credentials.
3. Run cells in order. Enter your WRDS password when the database connection prompt appears.
4. Complete WRDS authentication, then continue executing the rest of the notebook.

## 6. Product link / Demo
- GitHub Repository: https://github.com/XuwenZhou24/ACC102_MiniAssgnment_Xuwen.Zhou24/edit/main/README.md
- Demo Video: [Insert your 1–3 minute demo video link here]

## 7. Limitations & next steps
- Only annual data is used, lacking granularity and macroeconomic impact analysis.  
- Shows correlation but not causal relationships.
- Python workflow is linear and not modularized.
- Relies on visual observation without statistical modeling.
