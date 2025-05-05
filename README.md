# Alzheimer's Disease Detection with Machine Learning

## Project Components
### Research Paper
- [`Alzheimer_Disease_Detection_Report.pdf`](Alzheimer_Disease_Detection_Report.pdf)  
  *Comprehensive report detailing data, methodology, experiments, and findings.*

### Slide Deck
- [`AlzheimerDetection_Slides.pdf`](AlzheimerDetection_Slides.pdf)  
  *Concise summary of problem, approach, and results for presentation.*

### Notebooks 

| Notebook | File Name | Description |
|----------|-----------|-------------|
| 🔄 Conversion Patient Selection | [`Identify_Conversion_Patients.ipynb`](notebooks/Identify_Conversion_Patients.ipynb) | Filters longitudinal patient data for MCI-to-AD progression analysis. |
| 📋 Symptom-Based Classification | [`Symptoms_Classifier_ML.ipynb`](notebooks/Symptoms_Classifier_ML.ipynb) | Uses classical ML models on patient history and symptoms to classify AD/MCI. |
| 🧠 3D MRI Classification | [`3D_MRI_AD_Classifier.ipynb`](notebooks/3D_MRI_AD_Classifier.ipynb) | Builds and trains a 3D CNN model using NIfTI volumes. |

## Summary

This project explores multiple modalities for Alzheimer's detection:
- **Image-based deep learning**: Using 2D slices and full 3D MRI volumes.
- **Clinical data modeling**: Using symptom-based structured data.
- **Early diagnosis modeling**: Predicting future AD conversion from MCI.

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
- Best model: **Random Forest** with tuned depth and estimators with an F1 Score of 0.7957.
- Evaluation focused on preventing underfitting/overfitting by comparing train/test accuracy deltas.

## Tools & Libraries

- PyTorch, Keras, Scikit-learn, NiBabel, NumPy, Pandas
- OpenCV, Matplotlib, Seaborn
- MRI data from ADNI (Alzheimer's Disease Neuroimaging Initiative)

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
