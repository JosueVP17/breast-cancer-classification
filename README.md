# Breast Cancer Classification

This repository implements and compares two classification approaches for breast cancer diagnosis using morphological features extracted from fine needle aspirate (FNA) images:

1. **Rule-Based Classifier**
2. **Logistic Regression Classifier**

The project focuses on analyzing the trade-off between model interpretability and predictive performance. Rule-Based is fully interpretable, but it has limited flexibility. Logistic Regression is a balanced trade-off.

## Dataset

The experiments use the **Wisconsin Diagnostic Breast Cancer (WDBC)** dataset.

Source:
UCI Machine Learning Repository  
Wisconsin Diagnostic Breast Cancer Dataset  
https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+(Diagnostic)

The dataset contains digitized image features of fine needle aspirate (FNA) breast mass samples. Each instance represents a patient and includes:

- A diagnosis label (malignant or benign)
- 30 numerical features derived from 10 morphological characteristics:
  - radius
  - texture
  - perimeter
  - area
  - smoothness
  - compactness
  - concavity
  - concave points
  - symmetry
  - fractal dimension

Each characteristic is provided as:
- Mean value "_0"
- Standard deviation "_1"
- Worst (maximum) value "_2"

## Models

### 1. Rule-Based Classifier

A medically motivated model that classifies a tumor as malignant if any of the following are statistically abnormal relative to benign tissue:

- Cell size
- Cell shape
- Cell texture
- Homogeneity

---

### 2. Logistic Regression

A regularized logistic regression model trained on standardized features that maintains partial interpretability via coefficients
