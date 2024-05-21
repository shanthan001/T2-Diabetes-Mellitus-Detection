# DiabAnalytica: Predictive Modeling for Type2 Diabetes

## Group Members
- Pallavi Singh – B00955705 (pl414338@dal.ca)
- Priyadharshini Sridharan – B00955679 (pr423614@dal.ca)
- Syanthan Vullingala – B00952624 (sy454227@dal.ca)

## Professor
- Evangelos Milios

## INDEX
1. [INTRODUCTION](#introduction)
2. [BACKGROUND INFORMATION](#background-information)
3. [PROBLEM STATEMENT](#problem-statement)
4. [PROBLEM SIGNIFICANCE](#problem-significance)
5. [PROJECT OBJECTIVES](#project-objectives)
6. [PROJECT SCOPE](#project-scope)
7. [DATA COLLECTION & PREPARATION](#data-collection--preparation)
8. [DATA ANALYSIS](#data-analysis)
9. [MODELING](#modeling)
10. [RESULTS](#results)
11. [INTERPRETATION OF RESULTS](#interpretation-of-results)
12. [IMPLICATIONS](#implications)
13. [LIMITATIONS](#limitations)
14. [CONCLUSIONS](#conclusions)
15. [REFERENCES](#references)
16. [APPENDIX](#appendix)

## INTRODUCTION
Diabetes remains an important health challenge with its widespread presence steadily increasing around the world. It can lead to other serious issues such as cardiovascular diseases, renal failure, and neuropathy, contributing to rising mortality rates in diabetic patients. Accurately predicting mortality risks in diabetic patients is crucial for identifying high-risk individuals, forming proper diabetic treatment options, and mitigating mortality among older patients.

## BACKGROUND INFORMATION
Our project mainly focuses on Type 2 Diabetes Mellitus (T2DM), which generally occurs when insulin is not effectively used by the body due to excess body weight and physical inactivity. According to WHO reports, around 1.5 million people died due to diabetes in 2019, with 48% of these individuals being under 70 years of age. T2DM constitutes more than 95% of diabetic cases, and affected individuals usually live 6 years less than healthy individuals as per the CDC.

## PROBLEM STATEMENT
Diabetes is a serious health condition leading to complications like vision loss, heart strokes, kidney failures, and limb amputations. It increases the risk of mortality and the onset of both microvascular and macrovascular complications. However, these risks can be reduced by following proper diabetic treatment plans and meeting treatment objectives. Accurately predicting remaining life expectancy remains a significant challenge, with existing mortality prediction models offering limited accuracy for wide populations, particularly in multiclass classification.

## PROBLEM SIGNIFICANCE
The significance of addressing this problem lies in the potential health benefits and improved quality of life for older adults with T2DM. Accurate mortality risk prediction can lead to more effective, personalized treatment plans, potentially reducing premature death rates and improving overall patient outcomes. This research could also provide valuable insights into the factors most indicative of mortality risk, guiding future healthcare strategies and policies.

## PROJECT OBJECTIVES
The main objective is to develop a multiclass classification methodology to predict all-cause mortality in elderly individuals with T2DM, considering various individual-level risk factors. The aim is to develop a single mortality prediction model for patients aged 65 years or older, comparing the performance of various machine learning algorithms to identify the most effective method for classifying patients into distinct risk categories, thereby facilitating more precise and effective treatment planning.

## PROJECT SCOPE
This project focuses on older adults aged 65 and above with T2DM, leveraging a structured dataset of U.S. military Veterans. It tracks the mortality status of patients at both 5-year and 10-year intervals. The project excludes patients with Type 1 Diabetes or gestational diabetes and does not use external datasets for model validation.

## DATA COLLECTION & PREPARATION
The data was sourced from the Mendeley Data Repository, consisting of records of U.S. Military Veterans aged 65 years and above diagnosed with T2DM from 2004 to 2016. The dataset includes 275,190 rows and 70 columns with demographics, clinical biomarkers, and comorbidities. A new column 'mortality' was created based on 'DEATH_5' and 'DEATH_10' columns to indicate remaining life expectancy.

Data preparation involved handling missing values, duplicates, outliers, and data imbalance. The data was analyzed using Chi-Square Test, Cramer's Test, and Phi coefficient. Feature selection was performed using Information Value (IV) and Weight of Evidence (WOE), followed by one-hot encoding and Mutual Information (MI) to identify the best 20 features.

## DATA ANALYSIS
### Chi-Square Test
The chi-square test was used to determine the strength of the relationship between the predictor variables and the target variable. Based on the hypothesis testing result, significant relationships were identified for most columns.

### Cramer’s Test
Cramer's V test gauged the strength of association between pairs of categorical predictors, indicating no significant correlations among predictor variables and the mortality target variable.

### Phi Coefficient
The Phi coefficient measured the strength and direction of association between binary variables, providing insights into the relationships between predictors and the target variable.

## MODELING
The dataset was split into training (75%) and testing (25%) sets. Various models were employed: Baseline Model (Majority Classifier), Logistic Regression, Random Forest, XGBoost, and Decision Tree, with some models undergoing hyperparameter tuning.

### Model Evaluation
Models were evaluated using metrics such as accuracy, confusion matrix, AIC, AUC, and Cohen Kappa. Logistic Regression and XGBoost slightly outperformed other models, with Logistic Regression having the highest AUC score and the lowest AIC.

## RESULTS
### Model Performance Analysis
All models showed similar performance with testing accuracy around 67%-69%. Logistic Regression and XGBoost were marginally better in terms of F1 score and overall balance between false positives and false negatives.

### Inference Based on AIC
XGBoost model had the lowest AIC score, indicating it as a better model in terms of goodness of fit.

### Inference Based on AUC
Logistic Regression model had the highest AUC score, performing best at distinguishing between the two classes.

### Inference Based on Cohen’s Kappa
Logistic Regression and XGBoost had the highest agreement, showcasing high consistency in predictions.

## INTERPRETATION OF RESULTS
The study identified significant predictors of mortality in older individuals with T2DM, emphasizing the importance of cardiac evaluation and monitoring serum creatinine levels. Results indicated the 80–84 age group as particularly vulnerable.

## IMPLICATIONS
Despite identifying important factors, the machine learning models did not attain adequate accuracy, necessitating further refinement. Collaboration with domain experts and incorporating additional factors could enhance model accuracy.

## LIMITATIONS
The study's reliance on a dataset of U.S. military veterans limits the applicability of findings to broader populations. Residual biases and inaccuracies in the dataset may affect the validity of the results. Exploring alternative algorithms could enhance the study's robustness.

## CONCLUSIONS
The project developed a predictive model for mortality in elderly T2DM patients, identifying key predictors associated with mortality risk. While the models exhibited moderate performance, further research is needed to improve accuracy. The study underscores the importance of interdisciplinary collaboration in healthcare research.

## REFERENCES
1. World Health Organization. (2023, April 5). Diabetes. [WHO](https://www.who.int/news-room/fact-sheets/detail/diabetes)
2. Kevin Griffith. (2021, December 21). A Novel Dataset of Predictors of Mortality for Older Veterans Living with Type II Diabetes. [Mendeley Data](https://data.mendeley.com/datasets/kn8v3678n9/3)
3. Sage Pub. PEARSON’S R, CHI-SQUARE, T-TEST, AND ANOVA. [Sage](https://www.sagepub.com/sites/default/files/upm-binaries/33663_Chapter4.pdf)
4. Stats Test. Cramer’s V. [Stats Test](https://www.statstest.com/cramers-v-2/)
5. Anik Chakraborty. (2021, September 5). Weight of Evidence (WoE) and Information Value (IV) — how to use it in EDA and Model Building? [Medium](https://anikch.medium.com/weight-of-evidence-woe-and-information-value-iv-how-to-use-it-in-eda-and-model-building)
6. Centers for Disease Control and Prevention. (2021, May 18). High Blood Pressure Symptoms and Causes. [CDC](https://www.cdc.gov/bloodpressure/about.htm)
7. Centers for Disease Control and Prevention. (2022, June 3). Assessing Your Weight. [CDC](https://www.cdc.gov/healthyweight/assessing/index.html)
8. Centers for Disease Control and Prevention. (2022, September 30). All About Your A1C. [CDC](https://www.cdc.gov/diabetes/managing/managing-blood-sugar/a1c.html)
9. University of Rochester Medical Center. Albumin (Blood). [URMC](https://www.urmc.rochester.edu/encyclopedia/content.aspx?contenttypeid=167&contentid=albumin_blood)
10. Mount Sinai. Creatinine blood test. [Mount Sinai](https://www.mountsinai.org/health-library/tests/creatinine-blood-test)
11. Mayo Clinic. (2022, September 3). Triglycerides: Why do they matter? [Mayo Clinic](https://www.mayoclinic.org/diseases-

