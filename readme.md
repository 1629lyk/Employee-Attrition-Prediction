# Employee Attrition Prediction

## Overview

This project aims to predict employee attrition using machine learning techniques. By leveraging a structured pipeline for data preprocessing, model training, and evaluation, the project provides actionable insights into the factors contributing to employee attrition. The integration of interpretability tools like LIME ensures transparency in the predictions.

---

## Introduction

Employee attrition is a significant challenge for organizations. Understanding the factors influencing attrition can help companies improve retention strategies and employee satisfaction. This project utilizes the IBM HR Analytics Employee Attrition Dataset to:
- Identify key predictors of attrition.
- Develop machine learning models to predict attrition likelihood.
- Provide interpretable insights into the contributing factors.

### Features
- **Preprocessing Pipeline**: Handles missing values, standardizes features, and applies dimensionality reduction.
- **Machine Learning Models**: Logistic Regression, Support Vector Machines (SVM), and ensemble methods.
- **Interpretability**: Feature importance analysis and instance-level explanations using LIME.

---

## Installation

### Prerequisites
- Python 3.7 or higher
- Jupyter Notebook (optional for interactive exploration)

### Steps
1. Clone the repository:
   ```bash
   git clone https://github.com/1629lyk/Employee-Attrition-Prediction.git
   cd Employee-Attrition-Prediction
   ```

2. Install the required Python packages:
   ```bash
   pip install -r requirements.txt
   ```

3. Download the dataset and place it in the `Dataset/` directory:
   - [IBM HR Analytics Employee Attrition Dataset](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset).

---

## Insights

1. **Key Predictors**:
   - Age: Lower age followed by other factors correlates with higher attriton rates
   - Distance from Home: Employees with long commutes are more likely to leave.
   - Job Satisfaction: Lower satisfaction correlates with higher attrition rates.
   - Total Working Years: Employees with limited experience are more prone to attrition.

2. **Threshold Adjustment**:
   - Fine-tuning the decision threshold improved the balance between precision and recall.

3. **Interpretability**:
   - LIME provided actionable insights into individual predictions, identifying the most influential factors for each instance.

---

## Machine Learning Models Used

1. **Logistic Regression**:
   - Linear model for predicting attrition.
   - Strength: Provides interpretable coefficients.

2. **Support Vector Machines (SVM)**:
   - Non-linear model for handling complex relationships in data.
   - Strength: Robust to outliers and works well with smaller datasets.

3. **Random Forest**:
   - Used for feature importance analysis.
   - Strength: Identifies the most predictive features effectively.

4. **Ensemble Method**:
   - Weighted combination of Logistic Regression and SVM.
   - Strength: Enhances predictive accuracy by leveraging strengths of individual models.

---

## Contributing

Contributions to improve the pipeline, add more models, or enhance interpretability are welcome! Please feel free to open issues or submit pull requests.

---