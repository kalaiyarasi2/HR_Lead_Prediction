HR Lead Prediction - Machine Learning Challenge 🚀

Overview

This project aims to predict which companies are "hot leads" for HR services. We used machine learning models to analyze company funding, hiring trends, and industry growth to make accurate predictions.

Problem Statement

HR service providers want to focus on companies that are most likely to buy their services. Instead of guessing, we use data to predict if a company will engage with HR services.

The dataset contains information like:

Funding rounds (How many times the company raised money)
Total funding received
Hiring activity (Job postings, employee growth)
Industry and regional trends
Our goal is to train a model that can predict whether a company is a hot lead (1) or not a hot lead (0)
____________________________________________________________________________________________________________________________________________________________________________________________

Dataset
The dataset contains:

📌 Features (Inputs to the model)
________________________________________________________________________________________________
Feature Name	            |          Description                                                |
__________________________|_____________________________________________________________________|
company_id	              |      Unique ID of the company                                       |
industry	                |      The industry the company belongs to                            |
funding_rounds	          |      Number of funding rounds                                       |
total_funding	            |      Total amount of money raised                                   |
job_postings_30d	        |      Job postings in the last 30 days                               |
employee_growth_pct	      |      Percentage employee growth in the last 6 months                |
hiring_roles	            |      Types of roles the company is hiring for                       |
industry_growth_rate	    |      Growth rate of the company's industry                          |
regional_employment_trend	|      Employment trend in the company's region                       |
funding_per_employee	    |      Total funding divided by number of employees                   |
days_since_last_funding	  |      Days since last funding round                                  |
growth_momentum           |      A score based on funding & hiring trends                       |
__________________________|_____________________________________________________________________|

🎯 Target Variable (Output we want to predict)

________________________________________________________________________________________________
Feature Name	   |   Description                                                                |
_________________|______________________________________________________________________________|
is_hot_lead	     |  1 if the company is a hot lead, 0 otherwise                                 |
_________________|______________________________________________________________________________|
____________________________________________________________________________________________________________________________________________________________________________________________

Approach

1️⃣ Data Preprocessing & Feature Engineering
✅ Handling missing values: We removed or filled missing values.
✅ Encoding categorical data: Converted text data (like "industry") into numbers.
✅ Feature scaling: Standardized numerical features for better model performance.
✅ Feature engineering: Added new features like Funding Per Employee and Growth Index.

2️⃣ Model Selection & Training
We trained multiple models and picked the best one based on F1-score:
✔ Logistic Regression 🏆 (Baseline Model)
✔ Random Forest Classifier 🌲
✔ XGBoost Classifier ⚡ (Best performer!)

3️⃣ Making Predictions & Submission
The best model predicted which companies were hot leads.
We saved predictions in submission.csv (company_id, is_hot_lead).
Uploaded the results to GitHub and submitted them to the competition.

____________________________________________________________________________________________________________________________________________________________________________________________
How to Run the Code? 🖥️

1️⃣ Install dependencies

pip install pandas numpy scikit-learn xgboost

2️⃣ Run the main script

python main.py

3️⃣ Check the generated submission file (submission.csv).

____________________________________________________________________________________________________________________________________________________________________________________________
Results & Evaluation

The model's performance was evaluated using:
✅ F1-Score (Primary metric, balances precision & recall)
✅ Accuracy, Precision, and Recall (Supporting metrics)
____________________________________________________________________________________________________________________________________________________________________________________________

Final Submission
📂 GitHub Repository contains:

✅ Source Code (All preprocessing & training steps)
✅ Predictions (submission.csv)
✅ Documentation (README.md)Submission Format (submission.csv example):

__________________________
company_id |	is_hot_lead | 
___________|______________|
COMP_000001	|     1       |
COMP_000002	|     0       |
COMP_000003	|     1       |
____________|_____________|

___________________________________________________________________________________________________________________________________________________________________________________________
