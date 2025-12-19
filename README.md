ESG Performance vs. Financial Profitability: A Data Science Approach

Project Overview:
This project was developed as a group assignment for the Data Science for Finance course. Our objective was to investigate the relationship between Corporate Social Responsibility (specifically ESG scores) and financial performance, measured by Return on Assets (ROA), within the technology and software sectors.

The project highlights a critical lesson in data science: the impact of sample size on correlation. While initial small-scale testing showed a positive trendline, expanding our dataset revealed a negative relationship between high ESG risk scores and financial efficiency.

Data Sources & Methodology
To build our dataset, we integrated three distinct sources:

Financial Data: Pulled via the yfinance API to obtain real-time market data.

Historical Financials: For data points missing from the API, we manually parsed SEC 10-K filings to ensure a complete longitudinal dataset for ROA calculations.

ESG Risk Scores: Sourced from Kaggle. These scores represent the environmental, social, and governance risk levels of the companies involved.

⚠️ Disclaimer
The ESG risk scores used in this project are for illustrative and academic purposes only. We cannot certify the absolute accuracy or current validity of these scores, as ESG reporting standards vary significantly across providers.

Technical Implementation
Data Processing: We used Pandas to clean data and calculate financial ratios, specifically focusing on ROA (Net Income / Total Assets).

Statistical Analysis: To determine the relationship between variables, we utilized numpy.polyfit to calculate and plot linear trendlines.

Visualization: Generated comprehensive bar charts and scatter plots to compare individual company ESG breakdowns and cross-metric correlations.

Key Findings: The "Sample Size" Revelation
Our analysis went through two distinct phases:

Phase 1: Small Sample Size (N=4)
Initially, we analyzed a small group of "Big Tech" firms (GOOG, MSFT, META, ORCL). In this limited scope, the trendlines for Environment, Social, and Governance were all positive. This suggested that higher ESG risk scores were associated with higher ROA.

Phase 2: Larger Sample Size (N=10+)
Recognizing that the initial results might be skewed by the exceptional performance of market leaders, we expanded the dataset to include companies like ADBE, ACIW, ADSK, EA, PAYC, and MTCH.

The Result: The trendlines inverted. With a broader sample, we observed a negative correlation.

Interpretation: This suggests that for the broader software industry in 2022, companies with higher ESG risk scores tended to have lower ROA, or conversely, that the most efficient companies (higher ROA) were managing their ESG risks more effectively (lower scores).

How to Run
Clone the repository.

Install dependencies: pip install yfinance pandas numpy matplotlib.

Run the Jupyter Notebook ESG_Finance_Analysis.ipynb.

Contributors: Ismail Khalloufi, Zakaria El Halfi, Charaf El Maniani, Taha Farouki
