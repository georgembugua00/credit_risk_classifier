# Credit Risk Classifier: Cornstone of Modern Banking

#  What is Credit Risk
![WhatsApp Image 2024-03-13 at 11 00 02 AM](https://github.com/georgembugua00/credit_risk_classifier/assets/151632200/ff3ecff5-2668-4972-8036-21893a077672)

# Factors Influencing Credit Risk

![WhatsApp Image 2024-03-13 at 11 00 03 AM](https://github.com/georgembugua00/credit_risk_classifier/assets/151632200/d33a3ac1-346f-46e2-9fe4-e02c57311b2b)


# Mitigating Risk

![WhatsApp Image 2024-03-13 at 11 00 03 AM (1)](https://github.com/georgembugua00/credit_risk_classifier/assets/151632200/80b43b93-eae4-4042-b1bf-f40b30246a04)


## Business Understanding

Credit risk management is a vital component of the modern banking industry. Credit risk classifiers empower banks to make data-driven decisions and optimize financial performance. When effectively implemented, such models can contribute positively to a bank's Triple Bottom Line (TBL) by:

People:
Improved financial inclusion by identifying creditworthy borrowers, enabling expansion of the loan portfolio and reaching previously underserved populations.
Community development by directing loans to individuals who can leverage them for growth, fostering a ripple effect within communities.
Planet:
Enhanced corporate social responsibility (CSR) initiatives through reduced losses from delinquent loans, allowing banks to allocate more resources to sustainability efforts.
Profit:
Financial stability through effective risk management, ensuring long-term sustainability.
## Business Problem

Equity Bank seeks to expand its loan portfolio while maintaining a strong Triple Bottom Line. However, a rise in loan defaults and NPLs in 2023 necessitates a more precise and accurate credit risk prediction system.

## Main Objective

The objective is to implement a credit risk classification system that improves loan approval decisions by:

Predicting loan default risk
Recommending appropriate loan terms (optional, can be added based on model capabilities)
## Data Understanding

The system will leverage the following borrower and loan data:

**Personal Information:**

- person_age: Likely represents the borrower's age in years. Younger borrowers may have shorter credit histories and less stable income, potentially impacting creditworthiness.

- person_income: Indicates the borrower's annual income, a crucial factor in assessing loan eligibility and repayment capacity.

- person_home_ownership: Specifies homeownership status ("RENT", "MORTGAGE", "OWN"). Homeownership can be a positive indicator of financial stability.
- person_emp_length: Represents the borrower's employment length (e.g., in years). Stable employment signifies a consistent income source, essential for loan repayment.

**Loan Information:**

- loan_intent: Likely indicates the borrower's purpose for taking the loan (e.g., "debt_consolidation", "home_improvement"). The loan purpose can impact risk assessment as some purposes may be deemed riskier than others.

- loan_grade: Represents the credit rating assigned to the loan by the lender, reflecting the perceived risk based on the borrower's creditworthiness.

- loan_amnt: Specifies the loan amount requested, with higher loan amounts generally translating to higher risk for the lender.

- loan_int_rate: Indicates the interest rate charged on the loan, often determined by the borrower's creditworthiness and loan grade.

**Loan Status and Repayment History:**

- loan_status: Likely indicates the current loan status (e.g., "current", "late", "charged_off"), reflecting the borrower's repayment behavior and ability to meet obligations.

- loan_percent_income: Represents the loan amount as a percentage of the borrower's income. A high loan-to-income ratio indicates a larger financial burden, potentially increasing default risk.

**Credit Bureau Information:**

- cb_person_default_on_file: Likely indicates whether the borrower has any past loan defaults recorded in their credit bureau report ("Yes", "No"). A history of defaults suggests a higher risk of future defaults.

- cb_person_cred_hist_length: Represents the length of the borrower's credit history (e.g., in years). A longer credit history allows for a more comprehensive assessment of repayment behavior.
