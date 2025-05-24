# Capstone-3
Files for Final Capstone project for AI ML course
Predicting Academic Achievement Using Cognitive and Social-Emotional Data

Author:
Evelyn Johnson

Project Overview
This project investigates the predictive relationship between students’ cognitive reasoning abilities (measured via CogAT subtests) and social-emotional competence (measured via the DESSA) with their academic performance in reading and math. The overarching aim is to determine whether integrating machine learning models can enhance our ability to identify students who may benefit from additional instructional or social-emotional supports.

Problem Statement
Many school districts rely only on a student's academic achievement data to make important instructional decisions. This project explores whether the inclusion of social-emotional and cognitive reasoning data provide a more complete and predictive model of student achievement. The goal is to assess and compare the effectiveness of various machine learning models in predicting academic performance based on these whole-child indicators. 

Data Acquisition - data for this project came from several school districts across one state. Future analyses could be conducted for other states that collect similar data to better inform instructional decision making for their students. 
Sample Size: ~2,300 students
Features:
  CogAT subtests: Verbal, Quantitative, Nonverbal
  DESSA scale scores
  State assessment scores (Reading and Math)
Demographic variables: gender, race, EL status, SPED status, Gifted

Data preprocessing and preparation: Data was cleaned, missing values handled, and encoded appropriately. The dataset was split into 80% training and 20% testing subsets. Standard preprocessing techniques were applied including normalization and encoding of categorical variables.

Modeling, Outcomes and Evaluation: 
This project utilized supervised machine learning techniques to address a regression problem. The primary objective was to predict students' performance on standardized reading and math state assessments, which are continuous numerical outcomes. Therefore, regression models were the appropriate choice, as the target variables (test scores) are continuous rather than categorical.
Three types of regression models were implemented:
  1. Multiple Linear Regression to establish baseline predictive performance using cognitive and social-emotional variables.
  2. Regularized Regression Models (LASSO and Ridge) to address potential multicollinearity and enhance generalization.
  3. Random Forest Regressor as a non-linear, ensemble-based approach to compare against linear models.
The expected outputs from these models are numerical test score predictions for both reading and math subjects. These outputs were compared against actual student scores to assess model accuracy and interpretability. Evaluation metrics included Mean Absolute Error (MAE), Root Mean Squared Error (RMSE), and R² Score, enabling a clear comparison of predictive performance across different modeling techniques.
This approach supports the goal of identifying students who may need targeted academic or social-emotional interventions based on predicted underperformance relative to their cognitive profiles.


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
Best model: LASSO regression for both reading and math.
Top predictors: CogAT subtests and DESSA scores
R² scores: ~0.60 for Reading, ~0.63 for Math
Actionable Insight: Integrating SEL data can improve how schools identify students needing support and tailor interventions more effectively.

Next steps and recommendations
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
