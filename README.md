# ESG Performance vs. Financial Profitability: A Data Science Approach

A data science investigation exploring the relationship between Corporate Social Responsibility (ESG scores) and financial performance (ROA) in the technology and software sectors, demonstrating the critical impact of sample size on statistical conclusions.

## 📊 Project Overview

This project was developed as a group assignment for the **Data Science for Finance** course. Our objective was to investigate the relationship between Corporate Social Responsibility (specifically ESG scores) and financial performance, measured by **Return on Assets (ROA)**, within the technology and software sectors.

The project highlights a **critical lesson in data science**: the impact of sample size on correlation. While initial small-scale testing showed a positive trendline, expanding our dataset revealed a negative relationship between high ESG risk scores and financial efficiency.

## 📁 Data Sources & Methodology

To build our dataset, we integrated three distinct sources:

### Data Integration Pipeline

1. **Financial Data**: Pulled via the `yfinance` API to obtain real-time market data
2. **Historical Financials**: For data points missing from the API, we manually parsed **SEC 10-K filings** to ensure a complete dataset for financial ratios calculations
3. **ESG Risk Scores**: Sourced from Kaggle, representing the environmental, social, and governance risk levels of the companies involved

### ⚠️ Disclaimer

The ESG risk scores used in this project are for **illustrative and academic purposes only**. We cannot certify the absolute accuracy or current validity of these scores, as ESG reporting standards vary significantly across providers.

## 🔧 Technical Implementation

### Data Processing
- Used **Pandas** to clean data and calculate financial ratios, specifically focusing on:
  - `ROA` = Net Income / Total Assets
- Merged multiple data sources with different schemas into unified analysis dataset

### Statistical Analysis
- Utilized `numpy.polyfit` to calculate and plot linear trendlines
- Performed correlation analysis across ESG dimensions (Environment, Social, Governance)
- Compared statistical significance between small and large sample sizes

### Visualization
- Generated comprehensive **bar charts** showing individual company ESG breakdowns
- Created **scatter plots** with trendlines to visualize cross-metric correlations
- Built comparative visualizations highlighting the sample size effect

## 📈 Key Findings: The Sample Size Paradox

Our analysis went through two distinct phases that revealed fundamentally different conclusions:

### Phase 1: Small Sample Size (N=4)

Initially, we analyzed a small group of "Big Tech" firms:
- `GOOG` (Google/Alphabet)
- `MSFT` (Microsoft)
- `META` (Meta/Facebook)
- `ORCL` (Oracle)

**Results**: The trendlines for **Environment**, **Social**, and **Governance** were all **positive**. This suggested that higher ESG risk scores were associated with higher ROA.

**Initial Interpretation**: Market-leading tech companies might tolerate higher ESG risks while maintaining exceptional profitability through market dominance and innovation.

### Phase 2: Larger Sample Size (N=10+)

Recognizing that the initial results might be biased by the exceptional performance of market leaders, we expanded the dataset to include:
- Adobe (`ADBE`)
- ACI Worldwide (`ACIW`)
- Autodesk (`ADSK`)
- Electronic Arts (`EA`)
- Paycom Software (`PAYC`)
- Match Group (`MTCH`)
- Additional mid-cap and small-cap software companies

**Results**: The trendlines **inverted**. With a broader sample, we observed a **negative correlation** between ESG risk scores and ROA.

### Critical Insight

This reversal demonstrates a fundamental principle in data science: **conclusions drawn from small samples can be misleading**. The initial positive correlation was an artifact of sampling only the highest-performing outliers.

**Revised Interpretation**: For the broader software industry, companies with higher ESG risk scores tend to have lower ROA. Conversely, the most financially efficient companies (higher ROA) are managing their ESG risks more effectively (lower risk scores).

**Possible Explanations**:
1. **Operational Efficiency**: Companies with strong ESG practices may have better operational discipline overall
2. **Risk Management**: Lower ESG risk correlates with better overall risk management capabilities
3. **Long-term Value**: ESG-conscious companies may prioritize sustainable profitability over short-term gains
4. **Market Selection Bias**: The "Big 4" tech giants have unique market positions that don't generalize to the broader sector

## 📊 Statistical Metrics

### Correlation Analysis

**Small Sample (N=4)**:
- Environment Score vs. ROA: **Positive correlation**
- Social Score vs. ROA: **Positive correlation**
- Governance Score vs. ROA: **Positive correlation**

**Large Sample (N=10+)**:
- Environment Score vs. ROA: **Negative correlation**
- Social Score vs. ROA: **Negative correlation**
- Governance Score vs. ROA: **Negative correlation**

### Sample Size Impact

The project demonstrates how:
- Small samples can produce **statistically insignificant or misleading patterns**
- Outliers (market leaders) can dominate small-sample conclusions
- Larger samples reveal **more generalizable relationships**
- The direction of correlation can completely reverse with adequate sample size

## 🚀 How to Run

### Prerequisites
```bash
pip install yfinance pandas numpy matplotlib
```

### Execution
1. Clone the repository
2. Navigate to project directory
3. Run the main analysis script:
```bash
python MainScript.py
```

### Expected Output
- CSV files with cleaned financial and ESG data
- Scatter plots showing ESG vs. ROA relationships for both sample sizes
- Bar charts comparing individual company ESG breakdowns
- Trendline visualizations demonstrating the sample size effect

## 📚 Key Takeaways

1. **Sample Size Matters**: Always validate findings with adequately sized datasets before drawing conclusions
2. **Outlier Awareness**: Exceptional performers (Big Tech) may not represent broader industry trends
3. **Data Integration Challenges**: Combining API data with manual SEC filings requires careful validation
4. **ESG Complexity**: The relationship between ESG and financial performance is nuanced and sector-dependent
5. **Replication Importance**: Expanding sample sizes can completely change research conclusions

## 🎓 Academic Context

This project was completed as part of a **Data Science for Finance** course, demonstrating:
- Practical application of statistical analysis to finance
- Critical evaluation of data science methodologies
- Integration of multiple data sources (APIs, government filings, datasets)
- Clear communication of counterintuitive findings

## 👥 Contributors

Ismail Khalloufi, Zakaria El Halfi, Charaf El Maniani, Taha Farouki

---

*Note: This project is intended for educational purposes and demonstrates important statistical principles through real-world financial data analysis.*
