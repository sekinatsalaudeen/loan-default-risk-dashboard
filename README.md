# loan-default-risk-dashboard
Power BI dashboard analyzing 255K loan records for default risk drivers.

Loan Default Risk Dashboard (Power BI)
An interactive, 4-page Power BI dashboard analyzing 255,347 loan records to uncover key risk drivers, financial exposures, and borrower profile characteristics for a lending portfolio risk use case.

📋 Project Overview
Managing loan default risk is critical for maintaining financial health in lending institutions. This project investigates over $33 billion in total loan volume to pinpoint structural factors driving defaults, quantify portfolio exposure, and deliver actionable insights for risk management teams.

📊 Key Findings & Insights
Age is the Strongest Predictor: Borrower age emerged as the single strongest demographic predictor of default. Borrowers aged 18–25 exhibited a 20.76% default rate, compared to just 5.05% for those aged 60 and above—a massive 15.7-percentage-point spread.

High-Risk Segments: Unemployed borrowers in the 18–25 age bracket showed an alarming 23.82% default rate, more than double the overall portfolio average of 11.61%.

Portfolio Exposure: Identified $4 billion (13.15%) of the $33 billion loan book tied up in defaulted loans.

Loan Size Discrepancy: Defaulted loans were found to be, on average, 13% larger than non-defaulted loans, highlighting a need for stricter underwriting on larger-ticket loans.

🛠️ Technical Implementation & Architecture
Data Modeling: Designed a robust Star Schema data model to optimize query performance and maintain clear relationships between fact and dimension tables.

DAX Calculations: Wrote 15+ advanced DAX measures (utilizing time intelligence, conditional logic, and aggregations) to power dynamic metrics.

Advanced Visualizations: Implemented AI-driven visuals including Decomposition Trees to explore multi-level risk breakdowns, alongside custom conditional formatting to highlight high-exposure metrics instantly.


