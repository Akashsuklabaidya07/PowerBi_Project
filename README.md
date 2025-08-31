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
