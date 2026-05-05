Diabetes Treatment Effectiveness — Real-World Evidence (RWE) Study
Overview
This project presents a real-world evidence (RWE) analysis exploring the relationship between treatment exposure (simulated Metformin vs non-Metformin groups) and diabetes outcomes using observational health data.
The goal is to demonstrate how epidemiological methods can be applied to real-world datasets to evaluate treatment effectiveness outside of controlled clinical trials.
________________________________________
Objective
To assess whether patients in a simulated Metformin treatment group have different odds of diabetes outcomes compared to a non-Metformin group using real-world data.
________________________________________
Dataset
This project uses the Pima Indians Diabetes Dataset.
Dataset source:
https://www.kaggle.com/datasets/uciml/pima-indians-diabetes-database
How to use the dataset
1.	Download dataset from Kaggle
2.	Place the file in the /data folder
3.	Rename file to:diabetes.csv
________________________________________
Methodology
1. Data Preparation
•	Loaded and explored patient-level clinical variables
•	Handled basic data cleaning
•	Created derived variables for analysis
2. Treatment Definition (Simulated)
Since treatment labels were not available, a proxy was defined:
•	Metformin Group → Lower glucose levels
•	Non-Metformin Group → Higher glucose levels
This is a simulated treatment assignment and does not represent actual prescriptions.
________________________________________
3. Outcome Definition
•	Binary diabetes outcome variable (0 = No Diabetes, 1 = Diabetes)
________________________________________
4. Statistical Analysis
Crude Analysis
•	Group comparison using mean outcome rates
Epidemiological Analysis
•	Constructed 2×2 contingency table
•	Estimated:
o	Odds Ratio (OR)
o	95% Confidence Intervals (CI)
Confounder Assessment
•	Examined correlations between:
o	Glucose
o	BMI
o	Age
o	Blood Pressure
•	Identified potential confounding variables influencing both:
o	Treatment assignment
o	Outcome risk
________________________________________
Key Results
•	Patients in the non-Metformin group showed higher odds of diabetes outcome
•	Estimated Odds Ratio indicated a strong association between treatment group and outcome
•	Confidence intervals suggested statistical significance
Results should be interpreted with caution due to observational design.
________________________________________
Limitations
•	Treatment groups are simulated (not actual clinical exposure)
•	Presence of confounding variables (age, BMI, glucose severity)
•	No adjustment for confounders (crude OR only)
•	Observational design → cannot infer causality
________________________________________
Key Learnings
•	Application of epidemiological methods (OR, CI) in Python
•	Importance of confounding in RWE studies
•	Understanding difference between:
o	Association vs causation
o	Crude vs adjusted analysis
________________________________________
Tools & Technologies
•	Python
•	Pandas
•	NumPy
•	Seaborn / Matplotlib
•	Jupyter Notebook
________________________________________
📁 Project Structure
diabetes-rwe-study/
│
├── notebook/
│   └── diabetes_rwe_analysis.ipynb
│
├── data/
│   └── (dataset not included — see Kaggle link)
│
├── outputs/
│   ├── plots/
│   └── results.txt
│
├── src/
│   └── analysis.py
│
├── README.md
├── requirements.txt
└── .gitignore
________________________________________
Author
Name: Bhawesh Kumar Singh
GitHub: https://github.com/bhaweshsingh16004
________________________________________
Disclaimer
This project is for educational and portfolio purposes only.
It does not represent clinical or medical advice.
________________________________________

