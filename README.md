# 📊 Loan Default & Financial Risk Dashboard  

### 🔗 Dashboard Link : [Add your Power BI Service Link here]  

---

## 📌 Problem Statement  

Loan defaults are a critical challenge for banks and financial institutions. High default rates can impact liquidity, profitability, and long-term stability.  

This Power BI dashboard analyzes **loan disbursements, borrower demographics, credit scores, and default risks** to answer questions such as:  

- Which **borrower categories** are most likely to default?  
- What is the impact of **credit score, age, marital status, and education** on loan repayment?  
- How do **loan purposes** (home, business, education, auto, etc.) affect total lending and default risk?  
- What are the **year-over-year (YOY) trends** in loan disbursements and defaults?  

By using this dashboard, financial institutions can **improve risk assessment models, lending policies, and customer targeting strategies**.  

---

## ⚙️ Steps Followed  

1. **Data Loading**  
   - Imported dataset (CSV/Excel) into Power BI Desktop.  

2. **Data Cleaning (Power Query Editor)**  
   - Checked *column quality, distribution, and profiling*.  
   - Handled missing values.  
   - Standardized categories (Employment Type, Credit Score, Education).  

3. **Data Transformation**  
   - Created **Age Groups** (Teen, Adults, Middle Adults, Senior Citizens).  
   - Created **Credit Score Categories** (Low, Medium, High, Very Low).  
   - Created **Income Brackets** (Low Income, Medium Income, High Income).  

4. **DAX Measures Created**
   
-- Total Loan Amount
Total Loan Amount = SUM(Loan_default[LoanAmount])

-- Default Rate (%)
Default Rate % = 
DIVIDE(SUM(Loan_default[Default_Flag]), COUNT(Loan_default[Loan_ID])) * 100

-- YOY Loan Amount Change
YOY Loan Amount Change = 
DIVIDE([Total Loan Amount] - CALCULATE([Total Loan Amount], DATEADD('Calendar'[Date], -1, YEAR)),
       CALCULATE([Total Loan Amount], DATEADD('Calendar'[Date], -1, YEAR)))

-- YOY Default Loan Change
YOY Default Change = 
DIVIDE([Default Loans] - CALCULATE([Default Loans], DATEADD('Calendar'[Date], -1, YEAR)),
       CALCULATE([Default Loans], DATEADD('Calendar'[Date], -1, YEAR)))

-- YTD Loan Amount
YTD Loan Amount = TOTALYTD([Total Loan Amount], 'Calendar'[Date])
Report Design

Page 1 – Loan Default & Overview

Page 2 – Applicant Demographics & Financial Profile

Page 3 – Financial Risk Metrics

Page 4 – Education & Loan Behavior

Page 5 – Regional & Geographic Insights

Page 6 – Employment & Income Risk Analysis

Formatting & Branding

Applied themes & color palettes.

Added slicers for Age, Credit Score, Employment, and Education.

Added text boxes for dashboard titles.

Publishing

Report published to Power BI Service for collaboration and sharing.

📸 Snapshots

Loan Default & Overview Page

Applicant Demographics & Financial Profile Page

Financial Risk Metrics Page

Education & Loan Behavior Page

Regional & Geographic Insights Page

Employment & Income Risk Analysis Page

(Add your screenshots here in the GitHub repo)

📊 Insights
1️⃣ Loan Distribution & Purpose

Home Loans (6543M) had the highest loan amounts, followed by Business (6522M) and Education (6311M).

Adults & Middle Adults borrowed the highest loan amounts, averaging above 127K.

2️⃣ Default Analysis

Unemployed borrowers have the highest default rate (3.39%).

Default peaks were seen in 2015–2016 (11.7%), followed by stabilization.

3️⃣ Applicant Demographics

Median loan amount decreases with higher credit scores → low/medium scores borrow more.

Married borrowers with high credit scores are more reliable than single/divorced.

Dependents have little effect, but middle-aged borrowers with dependents borrow more.

4️⃣ Education & Loan Behavior

Highest number of loans: Bachelor’s (64K) and High School graduates (63K+).

Lower loans among PhD holders (~63K).

5️⃣ Regional & Geographic Insights

Loan disbursement is highest in metropolitan cities compared to rural areas.

Default rates are higher in rural & semi-urban regions, indicating weaker repayment capacity.

Urban borrowers have higher loan amounts but lower default risk, suggesting stronger financial profiles.

Certain regions show a consistent growth in loan demand, useful for branch-level expansion strategies.

6️⃣ Employment & Income Risk Analysis

High-income borrowers hold the majority of loans (32.5Bn), but low/medium income borrowers show higher risk levels.

Full-time employees are the most reliable in repayments, while part-time and unemployed categories show default spikes.

Income bracket analysis highlights that medium income borrowers take higher loan amounts relative to repayment capacity, raising risk.

Employment stability directly correlates with default probability → stable jobs = safer borrowers.

✅ Conclusion

This dashboard provides a 360° financial risk assessment for banks:

Identifies high-risk borrower groups (unemployed, part-time, low credit score, rural borrowers).

Shows how loan purpose, region, and demographics affect lending patterns.

Highlights default trends over years, income brackets, and job categories.

Supports better loan approvals, risk scoring, and recovery strategies.

With these insights, financial institutions can reduce default exposure, strengthen credit policies, and maximize profitability.
