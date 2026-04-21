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
- Apple maintained the highest return on equity across the period, with values consistently above 150%, reflecting a combination of strong net income and a reduced equity base due to share repurchases.
- Microsoft showed the strongest operating margins, with EBITDA margin exceeding 50% in 2024, indicating high operational efficiency.
- Google allocated the largest share of revenue to research and development, with R&D intensity remaining around 14–15% annually.
- All three firms experienced negative mean daily returns in 2022, consistent with the broader technology sector downturn during that year.
- When comparing risk-adjusted returns, Microsoft and Google exhibited a steadier recovery in 2023 and 2024, while Apple's ratio was more variable.

## 5. How to run 
A valid WRDS account is required to execute the notebook.
Install the required packages:
Open 'acc102_miniassignment_notebook.ipynb'notebook and replace the placeholder WRDS username with your own credentials. Run all cells in order. The notebook will prompt for a password when establishing the connection. 

## 6. Product link / Demo
-GitHub Repository: https://github.com/XuwenZhou24/ACC102_MiniAssgnment_Xuwen.Zhou24/edit/main/README.md
-Demo Video: [Insert your 1–3 minute demo video link here]

## 7. Limitations & next steps
- The analysis covers only three companies over a five-year period, which limits the ability to draw broader sector-wide conclusions.
- Annual aggregation smooths over quarterly fluctuations and masks events that occur within each year.
- ROE figures are affected by differing share buyback policies across firms, making direct comparison less straightforward.
- Future work could extend the time series to ten years, incorporate quarterly data, and add free cash flow analysis to distinguish operational performance from financial engineering.
