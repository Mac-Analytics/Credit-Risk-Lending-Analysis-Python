# Credit-Risk-Lending-Portfolio-Analysis

## Table of contents
- [Project Objectives](#Project-Objectives)
- [Data Cleaning & Preparation](#Data-Cleaning-&-Preparation)
- [Questions Explored](#Questions-Explored)
- [EDA-Key Findings](#EDA-Key-Findings)
- [Recommendations](#Recommendations)
- [Tools & Techniques](#Tools-&-techniques)




## Project Objectives

The bank is facing a **high level of loan defaults**, creating increased credit-risk exposure within its lending portfolio. Management needs to understand **which borrower characteristics, loan conditions, and borrowing purposes are associated with higher default risk** and which segments contribute most to overall portfolio risk.

The lack of clear, data-driven insight makes it difficult to **identify high-risk borrowers, monitor portfolio quality, and make informed lending decisions**. This project therefore aims to analyze historical credit data to uncover key risk patterns and provide actionable insights that can support **more effective credit assessment, risk monitoring, and lending strategies**.


## Data Cleaning & Preparation

- Loaded the raw dataset
<img width="1393" height="788" alt="clean" src="https://github.com/user-attachments/assets/1fdd2e73-8c9b-4ea8-b654-647ca6b204ca" />

- Renamed columns for clarity
<img width="1406" height="717" alt="clean2" src="https://github.com/user-attachments/assets/05f9502a-6b7f-471f-ac54-3c7c50c79e01" />

- Cleaned inconsistent values in Home_Ownership and Loan_Intent to ensure consistent category names
- Converted loan status and default history columns into meaningful categories
- Derived Risk_level from the existing loan_grade classification.
<img width="1408" height="872" alt="clean3" src="https://github.com/user-attachments/assets/dd3ec44e-d08f-4093-8f61-7f0fe3347921" />

- Created additional important columns like Loan_Burden, Credit_History_Range and Age_Group for better Analysis


## ❓(EDA) Questions Explored
- KPIs
- Which loan purposes are associated with the highest default rates?
- How many applications fall into each Risk Level?
- Does higher loan burden increase default risk?
- Does previous default history indicate a higher risk of future default?
- How does home ownership status relate to default risk?
- Does employment stability influence repayment performance?
- How does loan interest rate relate to borrower risk and default?
- Does credit history length relate to default risk?
- Which age group has the highest default rate?
- Are previous defaults more common in higher-risk grades?  



## EDA-Key Findings


### KPIs
<img width="1410" height="718" alt="KPIs" src="https://github.com/user-attachments/assets/777cdff5-f356-4bb2-b7c9-b9818122689f" />

- Total Loan Applications:
- Total Default Cases:
- Total Non-default Cases:
- Default Rate (%):
- Average Interest Rate:
- Average Income Amount:
- Average Loan Amount:

### Which loan purposes are associated with the highest default rates?  
<img width="1177" height="916" alt="loan-intent-Table" src="https://github.com/user-attachments/assets/321ebb8c-9714-4c80-bb76-6f6b099dac78" />
<img width="1407" height="902" alt="loan-intent-chart" src="https://github.com/user-attachments/assets/ad0e11bd-acea-478b-ac62-fa35ba81945d" />


### Insight
Debt Consolidation loans had the highest default rate at 28.6%, followed by Medical at 26.7% and Home Improvement at 26.1%. All three categories were above the portfolio-wide default rate of approximately 21.8%, indicating that these loan purposes are associated with comparatively higher observed credit risk.


### How many applications fall into each Risk Level?  
<img width="1495" height="930" alt="Risk-Level" src="https://github.com/user-attachments/assets/9e4724f9-9bc2-45d6-a3f7-093c4a4fb541" />


### Insight
- Very Low Risk has the largest number of applications with 10,777, followed closely by Low Risk with 10,451. Together, these two categories account for the majority of the loan portfolio.
- Moderate Risk contains 6,458 applications, while Elevated Risk accounts for 3,626 applications.
- High Risk has the smallest volume at 1,269 applications.


### Does higher loan burden increase default risk?  
<img width="983" height="941" alt="loan-burden-analysis" src="https://github.com/user-attachments/assets/1500fb25-a638-4854-b3c1-5354092910f5" />

### Insight
- Yes. The analysis shows a strong positive relationship between loan burden and default risk. Default rates increase consistently as loan burden rises, from 11.7% for borrowers with a 0–10% burden to 74.2% for those above 40%.
- The risk increases particularly sharply beyond 30% loan burden, with the default rate rising from 21.9% (21–30%) to 68.7% (31–40%).


### Does previous default history indicate a higher risk of future default?
<img width="848" height="942" alt="previous-default-rate" src="https://github.com/user-attachments/assets/c923d830-1b23-408b-b7e3-d700de74328c" />

### Insight
- Yes. Borrowers with a previous default history recorded a substantially higher current default rate: 37.81% compared with 18.39% for borrowers without a previous default history.
- This represents a 19.42 percentage-point difference and means the observed default rate among borrowers with previous defaults was about 2.1 times higher.


### How does home ownership status relate to default risk?
<img width="928" height="915" alt="home-ownership" src="https://github.com/user-attachments/assets/6174aa4b-e555-47cb-ada1-4977a3342dd8" />

### Insight
- Home ownership is associated with noticeable differences in default risk. Renters recorded the highest default rate among the major borrower groups at 31.57%, followed by Mortgage holders at 12.57% and Owners at 7.47%.
- The Other category also recorded a high default rate of 30.84%, but it represents only 107 applications, so this result should be interpreted cautiously due to the small sample size.
- Renters also contributed the largest number of default cases (5,192) because they make up the largest group in the portfolio.


### Does employment stability influence repayment performance?
<img width="882" height="937" alt="employment-range" src="https://github.com/user-attachments/assets/ebe7b7f8-65bf-4059-b5e6-741f4eeface1" />

### Insight
- Yes. The analysis shows a clear inverse relationship between employment stability and default risk. Default rates decline consistently as employment duration increases—from 25.38% for borrowers employed for 0–3 years to 16.40% for those employed for more than 10 years.
- This represents an 8.98 percentage-point difference between the shortest and longest employment groups, indicating that borrowers with longer employment histories have lower observed default rates.


### How does loan interest rate relate to borrower risk and default?
<img width="906" height="922" alt="interest-by-risk-loan" src="https://github.com/user-attachments/assets/f510b28d-6443-487f-99f3-1d4729e7f8b1" />

### Insight
- Interest rates increase consistently with borrower risk level. Average interest rates rise from 7.33% for Very Low Risk to 17.47% for High Risk, indicating that higher-risk borrowers are associated with substantially higher loan pricing.
- Defaulters also had a higher average interest rate than Non-Defaulters (13.06% vs 10.44%), suggesting that higher loan pricing is associated with poorer observed repayment outcomes in this portfolio.


### Does credit history length relate to default risk?
<img width="932" height="935" alt="credit-history" src="https://github.com/user-attachments/assets/62758bc9-d717-4415-a3dd-d6353de62d85" />

### Insight
- Credit history length shows a relatively weak and inconsistent relationship with default risk. Default rates remain close across the 6–10 years (20.6%), 11–15 years (20.6%), and 16–20 years (20.8%) groups.
- Borrowers with 2–5 years of credit history recorded a slightly higher default rate of 22.5%, while the 21–30 years group had the highest rate at 25.8%.
- Therefore, longer credit history does not consistently correspond to lower default risk in this portfolio


### Which age group has the highest default rate?
<img width="887" height="922" alt="age-group" src="https://github.com/user-attachments/assets/9dd045ed-66b0-4ae2-a26d-fca7c9c5616f" />

### Insight
- Borrowers aged Above 61 recorded the highest default rate at 26.6%, followed closely by the 51–60 age group at 25.7%.
- The 31–40 group recorded the lowest default rate at 20.4%, while the 41–50 and 20–30 groups recorded 20.4% and 22.2%, respectively.
- However, the Above 61 group contains only 64 applications, so its 26.6% default rate should be interpreted cautiously because of the small sample size.


### Are previous defaults more common in higher-risk grades?  
<img width="872" height="572" alt="previous-default-history" src="https://github.com/user-attachments/assets/67bb99a1-bdfa-4c16-a87f-49455c8f13e0" />

### Insight
- Previous default history is considerably more common in the higher-risk Loan Grades. Grades A and B have no borrowers with previous defaults, while previous-default records appear from Grade C onward.
- Among the grades with previous-default records, Grade G has the highest proportion at 56.3%, followed by Grade D at 51.7% and Grade C at 50.4%.
- However, the pattern is not strictly increasing across every grade: Grade E is 48.2% and Grade F is 46.5%. So, previous defaults are more concentrated in the riskier grades overall, but the relationship is not perfectly linear.


## 💡 Recommendations

### Strengthen screening for high-risk loan purposes.
- Apply additional affordability and repayment-capacity checks to Debt Consolidation, Medical, and Home Improvement applications, which recorded the highest observed default rates.

### Set tighter controls for high loan-to-income burdens.
- Introduce additional review or lower lending limits for borrowers whose loan amount represents a high proportion of their income, as default rates increased sharply at higher loan-burden levels.

### Include employment stability in credit assessment.
- Use employment duration alongside income and other financial indicators to assess repayment capacity, with closer review for borrowers with shorter employment histories.












