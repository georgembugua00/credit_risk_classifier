# Credit Risk Classifier: Cornstone of Modern Banking

#  What is Credit Risk
![WhatsApp Image 2024-03-13 at 11 00 02 AM](https://github.com/georgembugua00/credit_risk_classifier/assets/151632200/ff3ecff5-2668-4972-8036-21893a077672)

# Business Understanding

Credit risk management is a vital component of the modern banking industry. Credit risk classifiers empower banks to make data-driven decisions and optimize financial performance. When effectively implemented, such models can contribute positively to a bank's Triple Bottom Line (TBL) by:

### People:
- Improved financial inclusion by identifying creditworthy borrowers, enabling expansion of the loan portfolio and reaching previously underserved populations.

- Community development by directing loans to individuals who can leverage them for growth, fostering a ripple effect within communities.
### Planet:
Enhanced corporate social responsibility (CSR) initiatives through reduced losses from delinquent loans, allowing banks to allocate more resources to sustainability efforts.

### Profit:
Financial stability through effective risk management, ensuring long-term sustainability.

# Business Problem

Banks seeks to expand its loan portfolio while maintaining a strong Triple Bottom Line. However, a rise in loan defaults and NPLs in 2023 necessitates a more precise and accurate credit risk prediction system.

# Main Objective

The objective is to implement a credit risk classification system that improves loan approval decisions by:

Predicting loan default risk
Recommending appropriate loan terms (optional, can be added based on model capabilities)

# Data Understanding

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

- loan_status: Likely indicates the current loan status reflecting the borrower's repayment behavior and ability to meet obligations.

- loan_percent_income: Represents the loan amount as a percentage of the borrower's income. A high loan-to-income ratio indicates a larger financial burden, potentially increasing default risk.

**Credit Bureau Information:**

- cb_person_default_on_file: Likely indicates whether the borrower has any past loan defaults recorded in their credit bureau report ("Yes", "No"). A history of defaults suggests a higher risk of future defaults.

- cb_person_cred_hist_length: Represents the length of the borrower's credit history (e.g., in years). A longer credit history allows for a more comprehensive assessment of repayment behavior.

# Data Preprocessing

We addressed data quality issues to ensure the model's effectiveness:

1.**Missing Values:** Handled missing values using appropriate techniques like imputation based on feature type and distribution analysis.

2. **Outliers:** Identified and removed outliers that could significantly skew the model's learning process.

3. **Feature Engineering:** Created new features (e.g., debt-to-income ratio) to enhance model performance.

4. **Feature Scaling:** Standardized features to ensure all features contribute equally during model training.

5. **Categorical Encoding:** Converted categorical features (e.g., loan intent) into numerical representations suitable for model training.

# Exploratory Data Analysis (EDA)

We performed a comprehensive analysis to understand the data's distribution, identify outliers, and explore relationships between features. Techniques used include:

**Visualization:** Histograms, boxplots, scatterplots to visualize distributions and identify potential outliers.

1. **Univariate Analysis:** Calculating summary statistics (mean, median, standard deviation) to understand central tendency and dispersion.
![uni](https://github.com/georgembugua00/credit_risk_classifier/assets/151632200/7f11b907-3345-4e13-9165-43b3d86497b4)

2. **Bi-variate Analysis:** Analyzing relationships between pairs of features (e.g., employment length vs. loan default) to identify potential predictors.

![output](https://github.com/georgembugua00/credit_risk_classifier/assets/151632200/73c10eb7-087d-41e0-b95b-2674c975017e)

Modelling

## Feature Selection: 

Recursive Feature Elimination (RFE) was employed to identify the most relevant features for model training. 
RFE iteratively removes the least important feature based on a chosen estimator (e.g., DecisionTreeClassifier), resulting in a core set of features with the strongest predictive power for loan default risk.

## Machine Learning Algorithms: 

We experimented with Logistic Regression and Random Forest algorithms. 
Logistic Regression serves as a well-established baseline model for classification problems, while Random Forest is often effective for imbalanced datasets commonly encountered in credit risk assessment, where defaults are typically a minority class.

## Hyperparameter Tuning: 

GridSearchCV and RandomizedSearchCV were employed to optimize the performance of the chosen models. 
GridSearchCV performs an exhaustive search over a defined hyperparameter grid, while RandomizedSearchCV samples randomly from the grid, making it more efficient for large parameter spaces. 
Both techniques evaluate model performance using a scoring metric (e.g., precision) to identify the best hyperparameter combination for each model.

## Class Imbalance Mitigation: 

The credit risk data exhibits class imbalance, where loan defaults (minority class) are significantly outnumbered by non-defaults (majority class). 
This imbalance can lead to models prioritizing the majority class and performing poorly on defaults.
To address this, we explored oversampling (creating duplicate minority class observations) and undersampling (removing majority class observations) techniques, acknowledging the potential trade-offs associated with each approach.

# Model Development and Evaluation

We experimented with various machine learning algorithms to identify the best model for credit risk prediction. The key steps involved:

- **Feature Selection:** Employed techniques like RFE (Recursive Feature Elimination) to identify the most relevant features for model training.

- **Model Training and Tuning:** Trained and hyperparameter-tuned different models (e.g., Logistic Regression, Random Forest) using techniques like GridSearchCV and RandomizedSearchCV to optimize performance.

- **Class Imbalance Handling:** Addressed class imbalance (unequal distribution of loan default vs. non-default cases) using techniques like oversampling or undersampling.

- **Model Evaluation:** Evaluated model performance using various metrics like accuracy, precision, recall, F1-score, and ROC AUC score to assess the model's ability to correctly classify loan defaults.

## Results
Random Forest with RandomizedSearchCV: The Random Forest model, tuned using RandomizedSearchCV, emerged as the best performer.
This can be attributed to its ability to handle non-linear relationships in the data, its robustness to outliers, and its effectiveness in imbalanced classification problems.
