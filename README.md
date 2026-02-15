# Reduce Customer Churn for TruSource

My MSBA Project on Predictive Ananlytics
# Business Problem:
Customer churn threatens TruSource’s revenue stability because acquiring new customers costs far more than retaining existing ones. The goal of this project is to predict which customers are at risk of leaving and identify actionable intervention points early in the lifecycle. Beyond prediction, the focus is translating model insight into operational retention strategies.

# Key Results:
- CatBoost delivered the strongest detection power, outperforming Logistic Regression and Random Forest in ROC-AUC and PR-AUC on unseen data.
- Early-life, month-to-month customers represent the largest risk and opportunity, accounting for ~38% of the base with high revenue potential but low stability.
- Payment friction and engagement depth matter — auto-pay adoption, bundled services, and add-on usage strongly correlate with improved retention.

# How to Run the Project:
1. Clone the repository.
2. Install required libraries (catboost, scikit-learn, pandas, numpy, shap, matplotlib).
3. Place the dataset in the /data folder.
4. Start with Exploratory EDA
5. Run the preprocessing and feature engineering notebook/script.
6. Execute the modeling pipeline to reproduce cross-validation and final metrics.
7. Open the segmentation and interpretation notebooks to view SHAP results and strategy outputs.
8. Optional: Run K-mean segmentation to devise churn management recommendations based on groups
9. Use scoring code to predict churn probablity on unseen data
   

# Limitation / Risk
Customer behavior and competitive offers change over time. Without regular retraining and performance monitoring, model accuracy and segment definitions may degrade, reducing the effectiveness of retention interventions.
