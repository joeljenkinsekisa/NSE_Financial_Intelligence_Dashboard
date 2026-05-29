# NSE Financial Intelligence Dashboard

## Executive Overview

The NSE Financial Intelligence Dashboard is a comprehensive Power BI financial analytics project built to analyze the performance, valuation, profitability, and market behavior of companies listed on the Nairobi Securities Exchange (NSE). The project combines financial analysis, market intelligence, investment valuation, macroeconomic analysis, and risk assessment into one integrated analytical solution.

The dataset contains detailed company-level and sector-level financial indicators including revenue, net profit, market capitalization, stock prices, dividend payouts, debt-to-equity ratios, ESG scores, inflation rates, CBK rates, foreign ownership percentages, trading volumes, and sector classifications across multiple years and quarters.

The main objective of this project was to transform raw financial data into actionable investor-focused insights capable of supporting strategic investment decisions, valuation reviews, and market performance monitoring.

---

# Project Objectives

The project focused on:

* Evaluating sector performance trends across the NSE
* Identifying profitable and underperforming sectors
* Analyzing company profitability and valuation
* Measuring financial risk exposure
* Understanding macroeconomic impact on sectors
* Simulating fair value pricing using discount rate scenarios
* Building executive-level financial intelligence visuals

---

# Dashboard Structure

## 1. Sector Performance Analysis

<img width="1287" height="718" alt="sector perfromance" src="https://github.com/user-attachments/assets/b554b5cc-d51a-4141-852e-eebd2bb37ab4" />


This section focuses on sector-level performance and market momentum.

### Key Analysis

* Sector revenue comparison
* Sector market capitalization analysis
* Sector YoY return analysis
* Sector ranking heatmaps
* Profitability trends by quarter
* Sector performance distribution

### Key Finding

Agriculture emerged as the strongest performing sector with an average YoY return of 15.4%, outperforming Banking, Manufacturing, and Energy sectors. Aviation and Telco sectors also showed strong return momentum during recovery periods.

---

## 2. Company Performance & Valuation Analysis

<img width="1282" height="720" alt="company analysis" src="https://github.com/user-attachments/assets/d38156cf-1f01-4be5-bb33-0b5a18310314" />

<img width="1289" height="724" alt="company deep dive" src="https://github.com/user-attachments/assets/defd3630-b284-45c0-b1cb-2b7b3bb83b87" />

This section evaluates individual company performance, profitability, and valuation behavior.

### Key Analysis

* Top-performing companies by YoY return
* P/E Ratio vs ROE valuation analysis
* Stock price trend analysis
* Company profitability analysis
* Negative profit identification
* Executive company drillthrough analysis

### Key Finding

Several NSE-listed companies appeared significantly overvalued when compared to their simulated fair values. The average market price across companies stood at KSh 95.24 while the average simulated fair value was KSh 8.44 under the selected discount assumptions. This suggests that investors may currently be paying premiums driven more by growth expectations than intrinsic company value.

---

## 3. Financial Risk & Market Behaviour Analysis
<img width="1288" height="718" alt="financila risk and marketing " src="https://github.com/user-attachments/assets/6899a1b2-05c0-435d-bfd0-b7d8993c1ef1" />


This section evaluates risk exposure and macroeconomic influence on market sectors.

### Key Analysis

* Debt-to-equity risk analysis
* Volume traded activity analysis
* ESG score vs profitability analysis
* Foreign ownership analysis by sector
* CBK rate impact on Banking sector
* Inflation impact on FMCG companies
* Market phase analysis during Bull, Crisis, and Recovery periods

### Key Finding

Banking institutions maintained relatively high leverage positions, with debt-to-equity ratios exceeding 3.4x among several institutions. Despite this, Banking sector ROE remained resilient during periods of rising CBK rates, indicating strong operational stability under tightening monetary conditions.

---

## 4. Dividend Yield Simulator
<img width="1288" height="728" alt="divident yield simulator" src="https://github.com/user-attachments/assets/6f76a96c-e2ad-422a-a607-8ab7c00118e6" />


This section introduces scenario-based valuation analysis using dynamic discount rate simulations.

### Features

* What-if discount rate parameter
* Simulated fair value calculations
* Market price vs fair value comparison
* Premium/discount valuation analysis
* Scenario-based investment simulation
* Valuation scatter plot analysis

### Simulation Logic

The simulator uses a simplified Dividend Discount Model:

Fair Value = Dividend Per Share / Discount Rate

The dashboard dynamically recalculates simulated fair value as discount rates change between optimistic, base-case, and pessimistic valuation scenarios.

---

# Key DAX Measures

## Revenue

```DAX
Total Revenue =
SUM(NSE_Financials[Revenue_MnKES])
```

## Net Profit

```DAX
Total Net Profit =
SUM(NSE_Financials[Net_Profit_MnKES])
```

## Market Capitalization

```DAX
Total Market Cap =
SUM(NSE_Financials[Market_Cap_BnKES])
```

## Average P/E Ratio

```DAX
Average P/E Ratio =
AVERAGE(NSE_Financials[PE_Ratio])
```

## Average ROE

```DAX
Average ROE =
AVERAGE(NSE_Financials[ROE_Pct])
```

## Average Debt-to-Equity

```DAX
Average Debt-to-Equity =
AVERAGE(NSE_Financials[Debt_to_Equity])
```

## Average ESG Score

```DAX
Average ESG Score =
AVERAGE(NSE_Financials[ESG_Score])
```

## Average Simulated Fair Value

```DAX
Average Simulated Fair Value =
AVERAGEX(
    NSE_Financials,
    DIVIDE(
        NSE_Financials[Dividend_KES],
        SELECTEDVALUE('Discount Rate'[Discount Rate],12)/100
    )
)
```

---

# Business Insight

During the valuation analysis, I found that several NSE-listed companies appeared significantly overvalued when compared to their simulated fair values. The average market price across companies stood at KSh 95.24, while the average simulated fair value was only KSh 8.44 under the selected discount assumptions. This suggested that investors may currently be paying a premium based more on future growth expectations rather than intrinsic company value. The analysis highlighted the importance of valuation-focused investment decisions, especially in sectors experiencing strong market momentum where pricing risk may not be immediately visible.

---

# Skills Demonstrated

* Financial data analysis
* Power BI dashboard development
* DAX measure creation
* Power Query transformation
* Data modeling
* Investment valuation analysis
* Risk analysis
* ESG performance analysis
* Macroeconomic impact analysis
* Scenario simulation
* Executive storytelling
* Interactive dashboard design

---

# Tools & Technologies

* Power BI
* DAX
* Power Query
* Excel
* Financial Modeling
* Data Visualization

---

# Author

## Jenkins Ekisa Joel

Data & Business Analyst

* Email: [joeljenkinsekisa@gmail.com](mailto:joeljenkinsekisa@gmail.com)
* GitHub: https://github.com/joeljenkinsekisa
* Phone : +254 791 270 147
