# Alzheimer's Disease Detection with Machine Learning

## Project Components


## Problem Statement
Early and accurate diagnosis of Alzheimer’s Disease (AD) is critical, yet challenging due to limited clinical time, diagnostic complexity, and overlapping symptoms with normal aging. Current diagnosis relies on blood tests, history, and MRI scan interpretation, which is often manual and time-consuming.

## Objective
Develop ML models to:
1. **Classify** brain MRIs between AD and non-AD cases.
2. **Predict** future AD diagnosis from early MRIs.
3. **Classify** AD or Mild Cognitive Impairment (MCI) using patient symptom history.

## Datasets
All data sourced from the **Alzheimer’s Disease Neuroimaging Initiative (ADNI)**:

- **2D MRI Images**: 22–36 slices used (central brain region).
- **3D MRI Images**: Preprocessed NIfTI files; PCA applied for efficiency.
- **Symptom & Medical History Data**: Filtered ADNI1 phase data, joined on patient ID.

## Models & Techniques

### MRI Image Classification
- **2D CNN Model**:
  - Achieved **84.13%** validation accuracy.
  - Optimized via hyperparameters (kernel size, pooling, brightness, contrast).
- **3D CNN Model**:
  - 6-layer CNN trained with and without PCA.
  - Best training accuracy: **48%** after dimensionality reduction.

### Symptom-Based Classification
- Models tested: **KNN, Decision Tree, Random Forest, SVM, Naive Bayes, Logistic Regression**
- Best model: **Random Forest** with tuned depth and estimators.
- Evaluation focused on preventing underfitting/overfitting by comparing train/test accuracy deltas.

## Highlights
- Extensive preprocessing of MRI and tabular data.
- Multiple CNN architectures tested with augmentation and regularization.
- Comparative analysis across several classical ML models on non-imaging data.
- Carefully handled missing diagnoses through label imputation based on longitudinal data.

## Acknowledgments
Data from the [Alzheimer’s Disease Neuroimaging Initiative (ADNI)](http://adni.loni.usc.edu/).

## Contributors
1. Theresa Sumarta
2. Adeline Chin
