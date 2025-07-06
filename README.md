# Breast_Cancer_ML
🧠 Breast Cancer Detection Using ML (Logistic Regression, KNN, SVM)
This project uses machine learning algorithms to classify tumors as Malignant (M) or Benign (B) using the Breast Cancer Wisconsin dataset. The steps include data preprocessing, exploratory data analysis (EDA), feature selection, scaling, and model building with evaluation.

📂 Dataset
Source: breast_cancer.csv

Total entries: 569

Diagnosis labels:

M = Malignant (encoded as 1)

B = Benign (encoded as 0)

🔍 Workflow Overview
1. Data Preprocessing
Removed unnecessary id column.

Encoded target variable: M → 1, B → 0.

Checked for missing values using missingno.

Normalized features using StandardScaler.

2. Exploratory Data Analysis
Visualized class distribution.

Plotted distribution of all features.

Used a heatmap to observe correlation among features.

3. Feature Selection
Removed features having correlation > 0.92 to prevent multicollinearity.

Reduced feature count from 32 → 23.

4. Modeling & Evaluation

| Model                   | Train Accuracy | Test Accuracy | Precision | Recall    | F1-score |
| ----------------------- | -------------- | ------------- | --------- | --------- | -------- |
| **Logistic Regression** | 98.9%          | 96.5%         | 0.96–0.98 | 0.94–0.99 | 0.96     |
| **KNN (default)**       | 96.7%          | 95.6%         | 0.94–0.98 | 0.91–0.99 | 0.95     |
| **SVC (GridSearchCV)**  | \~100%         | 97.4%         | 0.96–1.00 | 0.96–0.99 | 0.97     |

.

🔧 Libraries Used
python
Copy
Edit
pandas, numpy, matplotlib, seaborn, sklearn, missingno
📈 Key Visualizations
Class Distribution Plot

Feature Histograms

Heatmap for Feature Correlation

Missing Data Matrix using missingno

🧪 Model Evaluation Metrics
Confusion Matrix

Accuracy Score

Classification Report

Precision

Recall

F1-score

✅ Conclusion
All three models perform well, with SVC giving the highest accuracy and balance between precision/recall.

Feature selection based on correlation significantly improved generalization by reducing redundancy.

The project can be extended using:

Cross-validation

Ensemble models (e.g., Random Forest, XGBoost)

Feature engineering

SHAP/LIME for explainability

