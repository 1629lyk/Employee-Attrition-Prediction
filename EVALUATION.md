# Project Evaluation

## Strengths
- **Structured workflow:** The notebook walks through preprocessing, data splitting, model training, and ensemble evaluation in clearly delineated stages, which makes the experimentation path easy to follow. 【F:Employee-Attrition-Prediction.ipynb†L267-L273】【F:Employee-Attrition-Prediction.ipynb†L457-L464】【F:Employee-Attrition-Prediction.ipynb†L1263-L1270】
- **Imbalanced-data handling:** You explicitly address class imbalance via oversampling prior to dimensionality reduction, helping the minority class remain visible to the models. 【F:Employee-Attrition-Prediction.ipynb†L457-L464】
- **Model breadth and interpretability:** The work combines linear, kernel-based, and ensemble models and emphasizes interpretability via feature importance and LIME, aligning with the goals documented in the README. 【F:readme.md†L16-L20】【F:readme.md†L62-L78】

## Opportunities for improvement
- **Use stratified splits:** Because attrition is only ~16%, using stratified train/test (or stratified cross-validation) would preserve the class distribution and reduce variance across folds. You noted avoiding stratification due to small-class concerns; using stratified splits with appropriate random seeds typically mitigates that risk. 【F:Employee-Attrition-Prediction.ipynb†L267-L273】
- **Prevent preprocessing leakage:** Oversampling and PCA appear to happen before model evaluation rather than inside a pipeline. Wrapping scaling, oversampling, PCA, and the estimator into an `imblearn.Pipeline` evaluated via cross-validation would ensure resampling and dimensionality reduction are confined to training data within each fold. 【F:Employee-Attrition-Prediction.ipynb†L457-L464】
- **Deepen evaluation:** The ensemble section reports ROC-AUC and classification reports; adding precision-recall curves or cost-sensitive metrics would better reflect performance on the minority class and support the threshold-tuning discussion in the README. 【F:Employee-Attrition-Prediction.ipynb†L1263-L1270】【F:readme.md†L48-L58】
