# Customer Loyalty & Churn Risk Modeling

## Project Overview
Understanding why customers leave is a critical component of effective growth and retention strategy. This project develops a **machine learning–based churn risk model** for a telecommunications company, designed to support more informed marketing and customer communication decisions.

Rather than replacing human judgment, the model serves as a **decision-support tool** that estimates churn probability and segments customers into actionable risk groups. The analysis balances predictive performance with interpretability to ensure insights can be translated into business strategy.

---

## Business Context
The organization seeks to better understand customer churn patterns and identify high-risk customers early enough to enable targeted retention efforts. The model is **not intended for automated decision-making**, but instead to:

- Highlight customers at varying levels of churn risk  
- Support segmentation-based marketing strategies  
- Provide insights into factors associated with customer attrition  

---

## Dataset
The dataset contains approximately **7,000 customer records**, including demographic, account, service usage, and billing attributes.

### Target Variable
- **Churn** (binary):  
  - `1` → Customer churned  
  - `0` → Customer retained  

The dataset exhibits **class imbalance**, making accuracy alone insufficient for evaluation.

---

## Exploratory Data Analysis (EDA)
Exploratory analysis was conducted to:

- Understand churn prevalence and class imbalance  
- Examine relationships between churn, tenure, contract type, and billing  
- Identify variables useful for segmentation and modeling  

Insights from EDA informed feature selection, modeling choices, and evaluation strategy.

---

## Modeling Approach

### Pipeline Design
A reproducible machine learning pipeline was built using:

- Categorical encoding  
- Feature scaling  
- Logistic Regression classifier  

### Hyperparameter Tuning
Hyperparameters were optimized using **RandomizedSearchCV**, with:

- **5-fold cross-validation**
- **F1 score** as the optimization metric  

This approach ensures balanced performance between precision and recall in the presence of class imbalance.

---

## Evaluation Metrics
The model was evaluated using:

- **F1 Score** (primary metric)  
- **ROC Curve and AUC**  
- **Confusion Matrix**  

These metrics provide a more meaningful assessment of churn prediction performance than accuracy alone.

---

## Key Results
- **Test F1 Score:** ~0.67  
- **ROC AUC:** ~0.88  

The ROC curve demonstrates strong class separability, allowing flexibility in selecting decision thresholds depending on business priorities.

---

## Churn Risk Segmentation
Predicted churn probabilities were converted into four interpretable risk segments:

| Risk Segment     | Description                          |
|------------------|--------------------------------------|
| Low Risk         | Very unlikely to churn               |
| Medium Risk      | Moderate churn likelihood            |
| High Risk        | Elevated churn risk                  |
| Very High Risk   | Immediate retention concern          |

Segment-level analysis revealed clear differences in tenure and monthly charges, enabling targeted retention strategies.

---

## Repository Contents
- **`Project 2 - Customer Loyalty.ipynb`**  
  Full analysis including EDA, modeling pipeline, hyperparameter tuning, evaluation, and segmentation.

- **`Customer_Churn_Pipeline.pkl`**  
  Serialized trained pipeline for reuse or deployment.

---

## How to Reproduce Results
1. Clone the repository  
2. Install required Python libraries:
   - `pandas`
   - `scikit-learn`
   - `matplotlib`
   - `seaborn`
3. Open and run the Jupyter notebook end-to-end  

---

## Key Takeaways
This project demonstrates how machine learning can support business decision-making by:

- Quantifying churn risk  
- Enabling customer segmentation  
- Balancing predictive performance with interpretability  

The framework is extensible and can support future enhancements such as cost-sensitive thresholds or expanded feature sets.

---

## Author
**Julio**  
BrainStation Data Science Bootcamp  
**Project 2 – Machine Learning**
