# Car-Insurance-Claim-Prediction
Predict whether the policyholder will file a claim in the next 6 months or not.

Training exercise on the dataset:https://www.kaggle.com/datasets/ifteshanajnin/carinsuranceclaimprediction-classification

## 🎯 Notebook Detailed Analysis

### 1️⃣ Importing Libraries and Data
- **Objective**: Prepare the work environment.
- **Libraries Used**:
- `h2o`: Distributed Machine Learning Library.
- `pandas`: Data manipulation and analysis.
- `datetime`: To track execution times.
- **Custom Function**: `from utils import _ds_common_pandas_dataframe_split_main` for data splitting.

👉 **Key**: Prepare the data and configure the visualizations.

---

### 2️⃣ Data Exploration
- **Objective**: Understand the structure and quality of the data.
- **Main operations**:
- `df.head()`, `df.info()`, `df.describe()` to inspect rows, columns, data types.
- Identify missing values ​​and distributions.

👉 **Key**: This step is crucial to decide on any cleaning or transformation.

---

### 3️⃣ Splitting the dataset
- **Objective**: Prepare training, validation and test sets.
- **Structure**:
- **Training set** for training.
- **Validation set** for tuning the algorithm.
- **Test set** for final evaluation.

👉 **Key**: Ensure fair splitting to avoid overfitting.

---

### 4️⃣ Training the model
- **Objective**: Build and train the machine learning model.
- **Process**:
- Initialize H2O.
- Convert dataset to `H2OFrame()`.
- Select model (e.g. `H2OGradientBoostingEstimator`).
- Define evaluation metrics (AUC, F1, AUCPR).

👉 **Key**: choosing the metrics is crucial for unbalanced datasets.

---

### 5️⃣ Experiments and variations
**Objective**: test different configurations to improve performance.

- **Baseline**: few variables, optimized for AUCPR.
- **Top AUCPR**: all original features, optimized for AUCPR.
- **Top F1**: optimize F1-score.
- **Top AUC**: optimize AUC.
- **Top AUCPR with balanced classes**: rebalance classes.
- **Top AUCPR with feature engineering**: adding new features.
- **Top AUCPR with exploitation_ratio = 0.1**: further advanced tuning.

👉 **Key**: each experiment has a specific goal, optimizing different metrics.

---

### 6️⃣ Leaderboard: model comparison
- **Goal**: identify the best performing model.
- **Methodology**: comparison based on metrics such as AUC, F1, logloss, AUCPR.

👉 **Key**: identify the best trade-off between accuracy and complexity.

---

### 7️⃣ Final analysis of the best model
- **Goal**: understand why the winning model performed better.
- **Analysis**:
- **Feature importance**: which variables influence the most.
- **Confusion matrix**: to examine classification errors.
- **SHAP values** (if applicable): interpretability of predictions.

👉 **Key**: explain the behavior of the model to make it interpretable.

---

## ✨ Overall conclusion

- **Main goal**: obtain a performing model for predicting reimbursement requests.
- **Most effective experiment**: (indicate which experiment had the best balance between metrics and interpretability).
- **Possible future improvements**:
- Optimize parameters.
- Test with other models.
- Add more features.

👉 **Final result**: the notebook has fully explored the problem, testing different configurations to find the best solution.


