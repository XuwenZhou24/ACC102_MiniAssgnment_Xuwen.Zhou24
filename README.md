# Stock Market and Financial Analysis of Big Tech Company

## 1. Problem & User 
**Problem:**
the relationship between corporate financial performance and stock returns across three major tech firms (Apple, Microsoft, Alphabet) from 2020 to 2024.    
**Target user:**
long-term equity investors.

## 2. Data 
All data was obtained from the WRDS (Wharton Research Data Services) platform. Stock market data was retrieved from the CRSP daily stock file and includes daily closing price, daily return, and trading volume. Financial statement data was retrieved from the Compustat Fundamentals Annual file and includes revenue, net income, EBITDA, research and development expense, total assets, and total equity. The sample covers the period from 1 January 2020 to 31 December 2024, and data was accessed in 17 April 2026.

## 3. Methods (main Python steps)
**1. Data Preprocessing:**
- Date Standardization: Convert date columns to  datetime  format and create a year variable for consistent annual time alignment across datasets
- Naming Unification: Apply  rename()  to standardize column naming conventions

**2. Data Aggregation & Metric Calculation**
- Stock Data Aggregation: Daily observations were grouped by  ticker  and  year  using  groupby()  and  agg()  to compute annual metrics including average stock price, mean daily return, total trading volume, and standard deviation of daily returns as a volatility measure.
- Financial Data Aggregation: Financial items were similarly aggregated by  ticker  and  year , with key performance ratios manually calculated from standardized financial items: net profit margin, EBITDA margin, R&D intensity, return on assets (ROA), and return on equity (ROE).

**3. Dataset Integration**
- Merge: Use  pd.merge()  on company (ticker) and year to combine stock and financial datasets
- Derived Metric: Calculate risk-adjusted return = mean daily return / return volatility

**4. Data Visualization**
- Tool: pandas built-in plotting functionality
- Chart Type: Line charts
- Visualized Dimensions: Average stock price trends, revenue trends, ROE trends, ROA trends

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
