# HR Attrition Analysis: Uncovering the Why Behind Employee Turnover

## Project Overview
This project analyzes employee attrition patterns using the IBM HR Analytics dataset and presents the findings through exploratory analysis, statistical testing, engineered business features, and an interactive Power BI dashboard. The dataset contains 1,470 employee records, with an overall attrition rate of 16.12%.This project also builds a complete ML pipeline — to help HR teams proactively identify at-risk employees.

## Business objective
The primary goal of this project is to understand employee turnover by identifying the key drivers of attrition. To achieve this, we developed a comprehensive dashboard that enables HR teams to monitor workforce risk and retention patterns. Additionally, the project leverages a machine learning logistic regression model to predict which employees are at a high risk of leaving. The core focus lies in advanced analytics, model interpretation, and the generation of actionable business insights.

**Dataset:** IBM HR Analytics Employee Attrition Dataset (1,470 employees, 35 features)  
**Source:** [Kaggle](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset)

Records: 1,470 employees
Final dataset after feature engineering: 39 columns
Overall attrition count: 237 employees
Overall attrition rate: 16.12%

## Project Phases

| Phase | Notebook | Description |
|-------|----------|-------------|
| 1 | EDA | Univariate, bivariate, correlation analysis |
| 2 | Statistical Testing | Chi-Square, Mann-Whitney U tests |
| 3 | Feature Engineering | RiskScore, BurnoutFlag, SatisfactionIndex |
| 4 | ML Modelling | Logistic Regression with threshold tuning |
| 5 | Power BI Dashboard | 3-page interactive dashboard |


## Project workflow
1. Exploratory Data Analysis
I explored employee attrition across department, job role, age group, income bracket, overtime status, job level, satisfaction, and travel frequency etc. to identify major patterns and outliers. These findings formed the basis for the dashboard design and later statistical testing.

2. Statistical Testing
I used statistical testing to validate whether important business variables were significantly associated with attrition. This helped move the analysis beyond visual trends and supported stronger business interpretation.

3. Feature Engineering
To make the analysis more business-friendly, I created seven derived features: RiskScore, RiskCategory, IncomeBracket, AgeGroup, TenureGroup, SatisfactionIndex, and BurnoutFlag. These features made it easier to segment employees into interpretable groups and improved dashboard storytelling.

4. Modelling
A Logistic Regression model was used only as a supporting analytical layer to validate the importance of attrition drivers and to create employee risk probabilities for the dashboard. The model used 47 features after encoding and achieved recall of 0.68 and AUC-ROC of 0.8408 with 5-fold CV AUC of 0.8460 ± 0.0529.

## Model summary
Although this project is presented as a data analytics project, I included a Logistic Regression model to validate patterns found during analysis and to generate attrition probability scores for dashboard segmentation. The model achieved 83% accuracy, 0.84 AUC-ROC, 0.85 CV AUC, 0.68 recall for employees who left, and used a 0.20 threshold.

## Key insights
-- Employees who work overtime show much higher attrition, with 30.53% attrition for overtime employees versus 10.44% for non-overtime employees.
-- Sales Representatives have the highest attrition rate among job roles at 39.76%, followed by Laboratory Technicians at 23.94% and Human Resources at 23.08%.
-- Sales and Human Resources departments have higher attrition than Research & Development, with attrition rates of 20.63%, 19.05%, and 13.84% respectively.
-- Employees who travel frequently have the highest attrition rate at 24.91%, compared with 14.96% for travel rarely and 8.00% for non-travel employees.
-- The custom RiskCategory feature separates employees clearly: Low Risk has 3.56% attrition, Moderate Risk 6.91%, High Risk 32.31%, and Critical Risk 77.50%.
-- The dashboard identifies 80 employees in the Critical Risk segment.
-- Income-based segmentation shows stronger attrition concentration in lower income groups, with the highest share in Medium (3K–7K) and Low (<3K) brackets.

## Dashboard overview
The Power BI dashboard is divided into three pages:

Page 1: Executive overview
This page summarizes workforce attrition using KPI cards and breakdowns by job role, department, business travel, overtime, income, age group, satisfaction, and job level. It is designed for quick HR leadership review.

Page 2: Analytical insights
This page combines the strongest analytical patterns with supporting model metrics, risk segmentation views, and probability-based comparisons across department, job role, overtime, and income. It helps explain which employee groups are most exposed to attrition risk.

Page 3: Employee risk explorer
This page provides interactive slicing by risk level, department, overtime, business travel, age group, and income bracket. It allows users to inspect employee segments more closely and supports targeted HR interventions.

## Tools used
-- MS-Excel
-- Python
-- Pandas
-- NumPy
-- Matplotlib
-- Seaborn
-- SciPy
-- Scikit-learn
-- Power BI

## Tech Stack
- **Python:** Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn
- **Statistics:** Chi-Square test, Mann-Whitney U test
- **ML:** Logistic Regression, StandardScaler.
- **Visualization:** Power BI, Matplotlib, Seaborn

---

## Repository Structure
├── Data/ → Raw and processed datasets
├── notebooks/ → Jupyter notebooks (Phase 1–4)
├── Dashboard/ → Dashboard screenshots
├── Plots/ → EDA and Model evaluation plots
└── requirements.txt → Python dependencies

---

## Dashboard Preview

[Dashboard](./Dashboard/HR_attrition_powerbi.pdf)

Page 1: Executive Overview | Page 2: ML Model Insights | Page 3: Employee Risk Tracker

---

## Author

**Yash Kumar**  
MSc Statistics | Data Science Aspirant
[LinkedIn](https://www.linkedin.com/in/yash-kumar-4b5668279/) 
