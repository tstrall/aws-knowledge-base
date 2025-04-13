# Classification Metrics in Machine Learning

> Relevant for:  
> ✅ Developer – Associate (DVA)  
> ✅ Machine Learning – Specialty (MLS)  
> ✅ Solutions Architect – Associate (SAA)

---

## What is it?

Classification metrics are quantitative measures used to evaluate the performance of machine learning models in classification tasks. They provide insights into how well a model is predicting categorical outcomes by comparing the predicted labels to the actual labels. These metrics are essential for understanding model accuracy, precision, recall, and other aspects of performance, especially in scenarios with imbalanced datasets or varying costs of misclassification.

---

## Why should I care?

- **Model Evaluation**: Helps in assessing how well your classification model is performing.
- **Performance Comparison**: Enables comparison between different models or algorithms.
- **Decision Making**: Informs decisions on model selection, tuning, and deployment.
- **Handling Imbalanced Data**: Provides appropriate metrics that account for class imbalance.

---

## Key Metrics

### 1. Accuracy

- **Definition**: The ratio of correctly predicted instances to the total instances.
- **Formula**: (TP + TN) / (TP + TN + FP + FN)
- **Use Case**: Suitable when classes are balanced.
- **Limitation**: Can be misleading with imbalanced datasets.

### 2. Precision

- **Definition**: The ratio of true positive predictions to the total predicted positives.
- **Formula**: TP / (TP + FP)
- **Use Case**: Important when the cost of false positives is high.

### 3. Recall (Sensitivity)

- **Definition**: The ratio of true positive predictions to the actual positives.
- **Formula**: TP / (TP + FN)
- **Use Case**: Crucial when the cost of false negatives is high.

### 4. F1 Score

- **Definition**: The harmonic mean of precision and recall.
- **Formula**: 2 * (Precision * Recall) / (Precision + Recall)
- **Use Case**: Balances precision and recall, especially useful with imbalanced classes.

### 5. Confusion Matrix

- **Definition**: A table layout that visualizes the performance of a classification model.
- **Components**:
  - **TP**: True Positives
  - **TN**: True Negatives
  - **FP**: False Positives
  - **FN**: False Negatives
- **Use Case**: Provides a comprehensive view of model performance.

### 6. ROC Curve and AUC

- **ROC Curve**: Plots the true positive rate against the false positive rate at various threshold settings.
- **AUC (Area Under Curve)**: Measures the entire two-dimensional area underneath the entire ROC curve.
- **Use Case**: Evaluates the ability of the model to distinguish between classes.

### 7. Matthews Correlation Coefficient (MCC)

- **Definition**: A measure of the quality of binary classifications, considering all four confusion matrix categories.
- **Formula**: (TP * TN - FP * FN) / sqrt((TP + FP)(TP + FN)(TN + FP)(TN + FN))
- **Use Case**: Provides a balanced measure even if the classes are of very different sizes.

---

## When to use which metric?

- **Balanced Classes**: Accuracy, F1 Score
- **Imbalanced Classes**: Precision, Recall, F1 Score, MCC
- **High Cost of False Positives**: Precision
- **High Cost of False Negatives**: Recall
- **Overall Performance**: AUC, MCC

---

## Learn More

- [Classification: Accuracy, Precision, Recall](https://developers.google.com/machine-learning/crash-course/classification/accuracy-precision-recall)
- [Evaluation Metrics for Classification Models](https://medium.com/analytics-vidhya/evaluation-metrics-for-classification-models-e2f0d8009d69)
- [Confusion Matrix](https://en.wikipedia.org/wiki/Confusion_matrix)
