# Coca-Cola vs PepsiCo: A Financial Comparison

## 1. Problem and User

This project compares the financial performance of Coca-Cola and PepsiCo from 2020 to 2025.

The main objective is to evaluate which company performs better in terms of profitability and financial stability. The target users are business students and beginner investors who want to understand how accounting data and financial ratios can be used to compare company performance.

## 2. Data

The dataset used in this project was retrieved from WRDS through the `comp.funda` table.

The analysis focuses on two companies:

* Coca-Cola (`KO`)
* PepsiCo (`PEP`)

The sample period covers fiscal years 2020 to 2025.

The main variables used are:

* `fyear`: fiscal year
* `sale`: revenue
* `ni`: net income
* `at`: total assets
* `lt`: total liabilities
* `act`: current assets
* `lct`: current liabilities

These variables are used to calculate net profit margin, current ratio, and debt ratio.

**Data access date:** 14 April 2026

## 3. Methods

This project uses Python, WRDS, SQL, pandas, and matplotlib.

The main steps are:

1. Connect to WRDS using the `wrds` package.
2. Retrieve company-level accounting data from `comp.funda` with SQL queries.
3. Combine Coca-Cola and PepsiCo data into one pandas DataFrame.
4. Clean duplicate or incomplete observations.
5. Calculate three financial ratios:

   * Net Profit Margin = Net Income / Revenue
   * Current Ratio = Current Assets / Current Liabilities
   * Debt Ratio = Total Liabilities / Total Assets
6. Create line charts to compare the two companies over time.

## 4. Key Findings

* PepsiCo consistently generated higher revenue than Coca-Cola from 2020 to 2025, suggesting a larger business scale.
* Coca-Cola reported a higher net profit margin across most of the sample period, indicating stronger profitability.
* Coca-Cola generally showed a higher current ratio, suggesting a stronger short-term liquidity position.
* PepsiCo reported a higher debt ratio in most years, indicating heavier reliance on liabilities.
* Overall, PepsiCo appears stronger in scale, while Coca-Cola appears stronger in profitability and financial stability.

## 5. Repository Contents

* `Financial Comparison notebook.ipynb` — main analysis notebook
* `figures/` — exported charts used in the project
* `README.md` — project overview and explanation

## 6. How to Run

To run this notebook, you need:

* Python
* Jupyter Notebook
* `wrds`
* `pandas`
* `matplotlib`

A valid WRDS account and internet connection are required for first-time access.

Run the notebook cells in order. The notebook connects to WRDS, retrieves the data, performs data cleaning, calculates ratios, and generates the charts.

## 7. Demo

A short demo video is included in the final submission package and can also be linked here if needed.

## 8. Limitations and Next Steps

This project has several limitations.

First, PepsiCo has a broader business structure than Coca-Cola, including major snack brands, so the two companies are not perfectly comparable.

Second, the analysis focuses on a limited set of accounting variables and ratios, which cannot fully capture all aspects of company performance.

Third, the project is descriptive and does not include forecasting or valuation analysis.

Possible improvements for future work include:

* adding more financial ratios
* extending the time period
* including more peer companies for industry comparison
* adding a simple valuation or forecasting component
