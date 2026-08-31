# my-diabetes-prediction-project
This repository contains the complete code implementation for an MSc research project on early Type 2 Diabetes Mellitus (T2DM) prediction. The project addresses critical literature gaps including data leakage, class imbalance, accuracy over-reliance, and black-box uninterpretability through a consolidated machine learning framework.

Improving Early Type 2 Diabetes Prediction Using Machine Learning and Explainable AI with Methodological Class Imbalance Handling

Author: Ahmed Talal Sherani
Student ID: 20082993
Institution: Ulster University
Module: COM748 Masters Research Project


PROJECT OVERVIEW

This project presents a methodologically rigorous, highly sensitive, and clinically interpretable machine learning framework for early prediction of Type 2 Diabetes Mellitus (T2DM). The framework addresses critical literature gaps including data leakage, class imbalance, accuracy over-reliance, and black-box uninterpretability.

Five supervised machine learning models were evaluated:

- Logistic Regression
- Support Vector Machine (SVM)
- Decision Tree
- Random Forest
- XGBoost

The framework includes data preprocessing, leakage-free pipeline (median imputation + post-split StandardScaler), dataset consolidation (1,233 records) for natural class balancing, GridSearchCV with 5-fold cross-validation optimized for Recall, comprehensive model evaluation (Accuracy, Precision, Recall, F1-Score, ROC-AUC), and dual-level Explainable AI using Gini importance and SHAP.


PROJECT FILES

Notebooks:

Diabetes_Prediction (PIMA dataset).ipynb
Baseline evaluation on imbalanced PIMA dataset (768 records). Demonstrates poor Recall due to class imbalance.

Diabetes_Prediction (merged dataset).ipynb
Core implementation on consolidated dataset (1,233 records). Leakage-free pipeline with 8-15 percent improvement over baseline.

Diabetes_Prediction (Graph).ipynb
Performance visualization: Bar charts, ROC-AUC curves, and Confusion Matrices.

Diabetes_Prediction (XAI Graphs).ipynb
Explainable AI implementation: Feature importance, SHAP summary, and Waterfall plots.

Data:

ddiabetes.csv
PIMA Indians Diabetes Dataset (768 records)

diabetes.csv
Additional registry dataset for merging

Results:

bar_chart.png
Grouped bar chart comparing Accuracy and Recall

roc_auc_curves.png
ROC-AUC curves for all five classifiers

confusion_matrix_rf.png
Confusion matrix of top-performing Random Forest model

XAI Outputs:

feature_importance.png
Global Gini feature importance bar chart

shap_summary.png
SHAP summary beeswarm plot

waterfall_plots/
Individual patient risk breakdowns

Other Files:

requirements.txt
Python libraries required to run the notebooks

README.md
Project description and instructions


REQUIREMENTS

Python 3.14.7 or later
Jupyter Notebook / Anaconda
Required Python libraries listed in requirements.txt


INSTALLATION

Install the required libraries using:

pip install -r requirements.txt


HOW TO RUN

1. Open Jupyter Notebook through Anaconda Navigator or by running:

jupyter notebook

2. Recommended order to run notebooks:

First, run Diabetes_Prediction (PIMA dataset).ipynb to see baseline performance.
Then, run Diabetes_Prediction (merged dataset).ipynb to see improved results.
Run Diabetes_Prediction (Graph).ipynb to generate visualizations.
Finally, run Diabetes_Prediction (XAI Graphs).ipynb for explainability analysis.

3. Make sure all CSV files are in the same directory or update file paths accordingly.

4. Run each notebook sequentially or select Cell then Run All.


KEY RESULTS

Dataset merging improved all models by 8 to 15 percentage points.

Random Forest achieved the best overall performance on the merged dataset:
Accuracy: 84.21 percent
Precision: 85.04 percent
Recall: 84.38 percent
F1-Score: 0.8471

Plasma Glucose was identified as the dominant global predictor with 38 percent Gini feature importance.


EXPLAINABLE AI (XAI) INTEGRATION

Global Level:
Gini feature importance identifies overall clinical risk drivers across population.
SHAP summary beeswarm plot shows direction and magnitude of feature impacts.

Local Level:
SHAP waterfall plots explain individual patient risk breakdowns.

Clinical Significance:
Transparent reasoning helps clinicians trust AI predictions.
Satisfies GDPR Article 22 (Right to Explanation).
Enables informed diagnostic decisions based on interpretable outputs.


ETHICAL NOTE

The study uses publicly available anonymised data from the PIMA Indians Diabetes Dataset (Kaggle) and a complementary registry (Mendeley Data).

The framework is intended for experimental diabetes risk screening and is not a substitute for formal clinical diagnosis. All models are designed as Clinical Decision Support Systems (CDSS) to assist, not replace, qualified medical professionals.


AUTHOR

Ahmed Talal Sherani
Student ID: 20082993
COM748 Masters Research Project
Ulster University, London Campus
Email: Sherani-AT@ulster.ac.uk


SUPERVISOR

Amrutha Vishnupriya 
Head of the Year (Ulster Y2), HETL
Email: Amrutha.Vishnupriya@qa.com


ACKNOWLEDGMENT

This research was conducted as part of the MSc programme at Ulster University. The author expresses gratitude to the supervisor for their invaluable guidance and to the Department of Computer Science for providing the necessary resources and computational support.
