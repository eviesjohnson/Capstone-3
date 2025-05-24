# Capstone-3
Files for Final Capstone project for AI ML course
Capstone Project Summary: Predicting Academic Achievement Using Cognitive and Social-Emotional Data

Author:
Evelyn Johnson

Project Overview
This project investigates the predictive relationship between students’ cognitive reasoning abilities (measured via CogAT subtests) and social-emotional competence (measured via the DESSA) with their academic performance in reading and math. The overarching aim is to determine whether integrating machine learning models can enhance our ability to identify students who may benefit from additional instructional or social-emotional supports.

Problem Statement
Many school districts rely only on a student's academic achievement data to make important instructional decisions. This project explores whether the inclusion of social-emotional and cognitive reasoning data provide a more complete and predictive model of student achievement. The goal is to assess and compare the effectiveness of various machine learning models in predicting academic performance based on these whole-child indicators. 

Data Overview
Sample Size: ~2,300 students
Features:
  CogAT subtests: Verbal, Quantitative, Nonverbal
  DESSA scale scores
  State assessment scores (Reading and Math)
Demographic variables: gender, race, EL status, SPED status, Gifted

Data was cleaned, missing values handled, and encoded appropriately. The dataset was split into 80% training and 20% testing subsets. Standard preprocessing techniques were applied including normalization and encoding of categorical variables.

Methods and Modeling
The dataset included student-level data from approximately 2,300 students, including CogAT subtest scores, DESSA scale scores, and state assessment results in reading and math. Student demographics (e.g., gender, EL, SPED, Gifted, and race) were also included.

I trained and evaluated several supervised learning models:
- Multiple Linear Regression
- LASSO and Ridge Regression
- Random Forest Regressor

Model performance was evaluated using Mean Absolute Error (MAE), Root Mean Squared Error (RMSE), and R² Score. All models were trained on 80% of the dataset and tested on the remaining 20%. Grid Search was used for hyperparameter tuning.

Key Findings
- Linear regression outperformed Random Forest in both reading and math prediction tasks, suggesting that relationships among predictors and outcomes are largely linear.
- CogAT subtests (especially Verbal for reading and Quantitative for math) were among the strongest predictors of achievement.
- DESSA scores played a meaningful role, especially when exploring performance beyond cognitive ability. DESSA scores enhanced predictive power, particularly in identifying over and under performing students.
- Residual analysis revealed that students with higher social-emotional competence often outperformed their cognitive expectations, underscoring the value of whole-child data.
- DESSA scores were significantly higher among overperformers, suggesting that strong social-emotional skills may support achievement even when cognitive ability is lower.

Visualizations
All visualizations were created using matplotlib, seaborn, and plotly. They include:
  Correlation heatmaps of predictors
  Feature importance rankings.
  Boxplots and scatterplots for subgroup comparison
  Residual plots highlighting over and under performers
  All visual elements are labeled with titles, axes, and legends

Summary of Results
Best model: Ridge regression with tuned hyperparameters
Top predictors: CogAT subtests and DESSA scores
R² scores: ~0.60 for Reading, ~0.63 for Math
Actionable Insight: Integrating SEL data can improve how schools identify students needing support and tailor interventions more effectively.

Implications and recommendations
This analysis supports the value of including whole-child data—cognitive and social-emotional measures—when identifying students for intervention. Machine learning can enhance this process by uncovering nuanced patterns and providing interpretable insights (e.g., via feature importance and residual analysis) that inform practice.
Next steps include:
1. Broaden use of whole-child assessments in early academic intervention strategies.
2. Train educators to interpret and apply social-emotional data alongside cognitive assessments.
3. Explore model deployment for real-time school district use.
4. Extend research to include longitudinal data to study growth over time.

Contact:
Author: Evelyn Johnson
email: ejohnson@apertureed.com

Files Submitted
- Jupyter Notebook with full code and results
- Summary report (this document)
