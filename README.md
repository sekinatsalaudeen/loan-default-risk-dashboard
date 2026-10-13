Loan Default Risk Dashboard

An interactive 4-page Power BI dashboard analyzing 255,347 loan records to identify which borrower characteristics most predict default, built for a lending risk use case.

Dataset: Loan Default Prediction Dataset (Kaggle, 255,347 rows, 18 columns) 
Tools: Power BI, Power Query, DAX

Overview

The loan book carries $33bn in total exposure across 255,347 loans, with an overall default rate of 11.61%. This project set out to answer: which borrowers are most likely to default, and how much money is actually at risk?


Key finding: Age is the strongest single predictor of default in this dataset, borrowers aged 18–25 default at 20.76%, compared to just 5.05% for borrowers 60+, a 15.7-point spread. The single riskiest segment is unemployed borrowers aged 18–25, who default at 23.82% — more than double the portfolio average.

Dashboard Pages
1. Overview

Headline KPIs (total loans, default rate, total exposure, exposure %), an Employment Type × Age Bracket chart showing the riskiest borrower combinations, and supporting views on credit score, co-signer/dependents, and age.

2. Borrower Profile

Who borrows: breakdowns by age, education, employment type, and marital status, plus average income and average loan size by group. Notably, loan volume, loan size, and income show little variation across education and employment type despite default rate varying significantly by employment type, meaning risk here isn't explained by income or loan size.

3. Loan Purpose and Amount

What loans are for and how much: exposure, interest rate, and loan term by purpose. Interest rate (~13.5%), loan term (~36 months), and loan amount are all nearly flat across loan purpose, purpose has little bearing on cost or risk.


4. Risk Drivers

Brings every risk finding together: an interactive Decomposition Tree for exploring compounding risk factors, a Credit Score × DTI Ratio matrix, and Defaulted Exposure by Employment Type.

Show Image

Key Findings
Factor	Finding	Spread
Age Bracket	18–25: 20.76% vs 60+: 5.05%	15.71 points
Co-signer + Dependents	Neither: 14.19% vs Both: 9.47%	4.72 points
Employment Type	Unemployed: 13.55% vs Full-time: 9.46%	4.09 points
Credit Score × DTI	Poor+High: 12.83% vs Excellent+Low: 8.61%	4.22 points
Credit Score	Poor: 12.47% vs Excellent: 10.18%	2.29 points
Loan Purpose	Business: 12.33% vs Home: 10.23%	2.10 points
DTI Ratio	High: 12.02% vs Low: 10.36%	1.66 points
Mortgage	No: 12.35% vs Yes: 10.88%	1.47 points

Exposure: Defaulted loans account for 13.15% of total loan value ($4bn of $33bn), slightly higher than their 11.61% share of loan count defaulted loans average $144.5K vs $127.6K for all loans, roughly 13% larger.

Data Model

Built as a star schema: a central Loans fact table connected to dimension tables for Education, EmploymentType, MaritalStatus, and LoanPurpose. Banded columns (Age Bracket, Credit Score Band, DTI Band, Months Employed Band) were added via Power Query conditional columns to support segment-level analysis.

15+ DAX measures were built, including Default Rate, Exposure %, Avg Defaulted Loan, and segment-specific CALCULATE variants.

Files
LOAN DEFAULT.pbix — the Power BI file
LOAN DEFAULT DASHBOARD VIEWS.pdf — exported images of all 4 dashboard pages
Limitations
The dataset has no date field, so it's a static snapshot rather than a time series — trend analysis and forecasting weren't possible.
Findings describe correlation, not causation.
A few deep, multi-factor combinations explored in the Decomposition Tree are based on small subgroups (under 200 loans) and should be read as directional rather than precise.
