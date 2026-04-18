📊 Customer Churn Analysis & Prediction

📌 Overview
This project analyzes customer churn behavior in a telecommunications dataset to identify high-risk customers and the key factors influencing churn. The goal is to generate actionable insights that improve customer retention and support data-driven decision-making.

📂 Project Structure
customer-churn-analysis/
├── notebooks/
├── images/
├── report/
├── README.md
├── requirements.txt

📂 Dataset
Records: 7,043 customers
Features: 21 variables (seniorcitizens, tenure, partner, dependents etc.)
Target Variable: Churn (Yes/No)
The dataset is imbalanced:
73.5% Non-churn
26.5% Churn

🔍 Key Insights
📈 Senior citizens churn significantly more
41.7% vs 23.6% (non-seniors)
📉 Month-to-month contracts drive churn
~23.5% of churned customers are on this plan
🌐 Fibre optic users show higher churn rates
Largest proportion of churned customers
👨‍👩‍👧 Customers without dependents/partners churn more

⚙️ Methodology
- Data cleaning and preprocessing
- Exploratory Data Analysis (EDA)
- Key Findings
- Model training and evaluation
- Business Recommendation
- Conclusion

🧠 Feature Engineering & Selection
- Converted categorical variables using one-hot encoding
- Identified multicollinearity:
- Strong correlation between tenure and total_charges (0.85)
- Dropped total_charges to reduce redundancy and overfitting      

🤖 Models Used
- Random Forest (primary model)
- Logistic Regression
- XGBoost

Evaluation Metrics
- Accuracy
- Precision
- Recall
- F1 Score

📊 Model Performance (Random Forest)
- Accuracy: 0.79
- Precision: 0.64
- Recall: 0.49
- F1 Score: 0.56

🔍 Key Evaluation Insight
The model demonstrates moderate precision but relatively low recall, indicating that while churn predictions are reasonably accurate, a significant number of churned customers are not identified.

📉 Confusion Matrix Insight
✔️ 1,400 non-churn correctly predicted
✔️ 276 churn correctly predicted
❗ 285 churn cases missed (False Negatives)
❗ 152 incorrect churn predictions (False Positives)

👉 This highlights a key limitation: missed churn customers, which directly impacts retention strategies.

🧠 Feature Importance
Top predictors of churn include:
- Tenure
- Monthly Charges
- Contract Type
- Internet Service (Fibre Optic)

💼 Business Recommendations
🎯 Target high-risk groups (senior citizens) with tailored retention strategies
📉 Reduce reliance on month-to-month contracts through incentives
💰 Re-evaluate pricing for fibre optic services
🎁 Offer loyalty rewards for long-tenure customers

Limitations
Dataset is imbalanced, which may bias predictions toward non-churn
Model recall is relatively low (0.49), meaning many churn cases are missed
Further improvements could include:
Threshold tuning
Resampling techniques (e.g., SMOTE)
Advanced model tuning

📄 Full Report
For a detailed analysis, see the full report:
👉 report/churn_analysis_report.pdf

🚀 Tech Stack
- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- XGBoost