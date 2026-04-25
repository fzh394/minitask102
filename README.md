# Coca-Cola vs PepsiCo: A Financial Comparison

## 1. Problem and User

This project compares the financial performance of Coca-Cola and PepsiCo from 2020 to 2025.

The main objective is to evaluate which company performs better in terms of profitability and financial stability.  
The target users are business students and beginner investors who want to understand how accounting data and financial ratios can be used to compare company performance.

## 2. Data

The dataset used in this project was retrieved from WRDS through the `comp.funda` table, with additional industry classification information linked from `comp.company`.

The analysis focuses on two companies:

- Coca-Cola (`KO`)
- PepsiCo (`PEP`)

The sample period covers fiscal years 2020 to 2025.

The main variables used are:

- `fyear`: fiscal year
- `sale`: revenue
- `ni`: net income
- `at`: total assets
- `lt`: total liabilities
- `act`: current assets
- `lct`: current liabilities

These variables are used to calculate net profit margin, current ratio, debt ratio, and return on assets (ROA).

An industry benchmark is also constructed using firms in the same broad two-digit SIC industry group.

**Data access date:** 22 April 2026

## 3. Methods

This project uses Python, WRDS, SQL, pandas, and matplotlib.

The main steps are:

1. Connect to WRDS using Python.
2. Retrieve company-level accounting data for Coca-Cola and PepsiCo with SQL queries.
3. Combine the two company datasets into one pandas DataFrame.
4. Clean duplicate or incomplete observations.
5. Calculate four financial ratios:
   - Net Profit Margin = Net Income / Revenue
   - Current Ratio = Current Assets / Current Liabilities
   - Debt Ratio = Total Liabilities / Total Assets
   - ROA = Net Income / Total Assets
6. Build an industry benchmark using firms in the same broad SIC industry group.
7. Create comparison charts for revenue, net income, profitability, liquidity, leverage, and ROA.

A reusable function is also included so that the workflow can be adapted for comparing other listed companies.

## 4. Key Findings

- PepsiCo consistently generated higher revenue than Coca-Cola from 2020 to 2025, indicating a larger business scale.
- Coca-Cola reported a higher net profit margin than PepsiCo in most years and remained above the industry average in profitability.
- Coca-Cola also reported a higher ROA than PepsiCo and the industry average in most years, suggesting stronger asset efficiency.
- Coca-Cola generally showed a stronger current ratio than PepsiCo, although both companies were below the broader industry benchmark in liquidity.
- PepsiCo reported a higher debt ratio than Coca-Cola in most years, and both companies were more leveraged than the industry average.
- Overall, PepsiCo appears stronger in scale, while Coca-Cola appears stronger in profitability and relatively stronger in financial stability.

## 5. Repository Contents

- `Financial Comparison.ipynb` — main analysis notebook
- `figures/` — exported charts used in the project
- `README.md` — project overview and explanation

## 6. How to Run

To run this notebook, you need:

- Python
- Jupyter Notebook
- `wrds`
- `pandas`
- `matplotlib`
- `numpy`

You also need a valid WRDS account to access the data.

Run the notebook cells in order.  
The notebook connects to WRDS, retrieves accounting data, performs data cleaning, calculates ratios, builds an industry benchmark, and generates the charts.

## 7. Demo

A short demo video is included in the final submission package and can also be linked here if needed.(https://video.xjtlu.edu.cn/Mediasite/Channel/50381bcaa0e74d9582215a01776a3d8d5f/headless/watch/179ddabe47934d14ae9338c0cf1c1e741d)

## 8. Limitations and Next Steps

This project has several limitations.

First, PepsiCo has a broader business structure than Coca-Cola, including major snack brands, so the two companies are not perfectly comparable.

Second, the analysis focuses on a limited set of accounting variables and ratios, which cannot fully capture all aspects of company performance.

Third, the project is descriptive and does not include forecasting or valuation analysis.

In addition, the industry benchmark is based on a broad two-digit SIC industry grouping, so it may not fully capture all competitive differences within the market.

Possible improvements for future work include:

- adding more financial ratios
- extending the time period
- including more peer companies for industry comparison
- adding a simple valuation or forecasting component
- turning the notebook into a more general company comparison template
