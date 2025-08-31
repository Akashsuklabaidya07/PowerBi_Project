# 📊 Loan Default & Financial Risk Dashboard

---

## 📌 Problem Statement
Loan defaults are a critical challenge for banks and financial institutions. This Power BI project analyzes *loan disbursements, borrower demographics, credit scores, and default risks* to answer:
- Which borrower segments are most likely to default?
- How do *credit score, age, marital status, education, income & employment* affect risk?
- What are the *YOY trends* in loans and defaults?

---

## ⚙️ Project Workflow

1. **Data Loading** → Imported raw data (CSV/Excel) into Power BI Desktop.

2. **Data Cleaning & Profiling** → Using Power Query for data typing, handling blanks, and profiling.

3. **Transformations** → Created derived fields: Age groups, Credit score bins, Income brackets.

4. **DAX Measures** → Built calculations for Loan Totals, Default %, YOY growth, Median values, etc.

5. **Report Pages** →

    - Overview (Defaults & Loan Purpose)

    - Demographics (Age, Marital Status, Education, Employment)

    - Financial Risk Metrics (YOY trends, Income Segments)

6. **Deployment** → Published to Power BI Service with scheduled refresh.

---

## 📸 Dashboard Preview
Here are the main report pages from the Loan Default & Risk Analysis dashboard:

<p align="center">
  <img src="images/dashboard_overview.png" alt="Dashboard Overview" width="45%"/>
  <img src="images/dashboard_demographics.png" alt="Dashboard Demographics" width="45%"/>
   <img src="images/demographics.png" alt=" Demographics" width="45%"/>
</p>

---
## 📊 Insights & Observations
**1. Loan Default & Overview**

- Loan Purpose Risk → Home and Business loans are the largest segments but also riskier; they need closer monitoring.

- Employment Type Risk → Unemployed applicants show the highest default rate (3.39%), followed by part-time & self-employed.

- Reliable Segments → Full-time employees are safest with the lowest default rate (2.36%).

- Age Factor → Adults borrow the most; Teens borrow the least. Seniors and middle-aged have similar loan behaviors.

- Time Trend → Default rates peaked in 2015–16 (~11.7%), then dropped in 2017—macro conditions likely influenced this.

**2. Applicant Demographics & Financial Profile**

- Credit Score → Higher credit scores = lower loan amounts but safer lending. Most loans go to Medium & High score applicants.

- Education Level → Bachelor’s degree holders take the most loans; PhD holders take the least.

- Marital Status → No major difference in loan amounts—does not strongly affect lending strategy.

- Dependents → Having dependents does not significantly change loan risk or loan size.

**3. Financial Risk Metrics**

- YOY Loan Trends →

   * 2015 & 2018 showed strong growth.

   * 2014 & 2017 saw loan shrinkage, possibly due to policies/economic factors.

- Default Volatility → Defaults spiked in 2015, dropped in 2017, rose again in 2018 → banks must prepare for cyclical risks.

- High Income Segments → Majority of loans come from high-income borrowers (safer group). Strategy should keep focusing on them.
