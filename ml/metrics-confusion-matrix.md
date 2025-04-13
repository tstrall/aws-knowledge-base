# Confusion Matrix in Machine Learning

> Relevant for:  
> ✅ Developer – Associate (DVA)  
> ✅ Machine Learning – Specialty (MLS)  
> ✅ Solutions Architect – Associate (SAA)

---

## What is it?

A **confusion matrix** is a performance evaluation tool in machine learning, representing the accuracy of a classification model. It displays the number of true positives, true negatives, false positives, and false negatives. This matrix aids in analyzing model performance, identifying misclassifications, and improving predictive accuracy. citeturn0search0

---

## Why should I care?

- **Comprehensive Evaluation**: Provides detailed insight into the performance of a classification model beyond simple accuracy.
- **Error Analysis**: Helps identify specific types of errors (false positives and false negatives) the model is making.
- **Metric Computation**: Enables calculation of other performance metrics like precision, recall, and F1-score.
- **Model Comparison**: Facilitates comparison between different models or algorithms.

---

## Key Components

In a binary classification problem, the confusion matrix is a 2x2 table:

|                | Predicted Positive | Predicted Negative |
|----------------|--------------------|--------------------|
| **Actual Positive** | True Positive (TP)    | False Negative (FN)   |
| **Actual Negative** | False Positive (FP)   | True Negative (TN)    |

- **True Positive (TP)**: Correctly predicted positive cases.
- **True Negative (TN)**: Correctly predicted negative cases.
- **False Positive (FP)**: Incorrectly predicted positive cases (Type I error).
- **False Negative (FN)**: Incorrectly predicted negative cases (Type II error).

---

## Derived Metrics

From the confusion matrix, several important metrics can be derived:

- **Accuracy**: (TP + TN) / (TP + TN + FP + FN)
- **Precision**: TP / (TP + FP)
- **Recall (Sensitivity)**: TP / (TP + FN)
- **F1 Score**: 2 * (Precision * Recall) / (Precision + Recall)
- **Specificity**: TN / (TN + FP)

---

## When to use it

- Evaluating the performance of classification models, especially when dealing with imbalanced datasets.
- Analyzing the types of errors made by a model to inform improvements.
- Comparing the performance of multiple classification models.
- Calculating other performance metrics for a more nuanced evaluation.

---

## Example: Creating a Confusion Matrix with Scikit-learn





```python
from sklearn.metrics import confusion_matrix
import numpy as np

# Example true labels and predicted labels
y_true = np.array([1, 0, 1, 1, 0, 1, 0, 0, 1, 0])
y_pred = np.array([1, 0, 1, 0, 0, 1, 1, 0, 1, 0])

# Generate confusion matrix
cm = confusion_matrix(y_true, y_pred)

print("Confusion Matrix:")
print(cm)
```





---

## Learn More

- [Confusion Matrix in Machine Learning - Analytics Vidhya](https://www.analyticsvidhya.com/blog/2020/04/confusion-matrix-machine-learning/)
- [Confusion Matrix - Wikipedia](https://en.wikipedia.org/wiki/Confusion_matrix)
- [Confusion Matrix - IBM](https://www.ibm.com/think/topics/confusion-matrix)
