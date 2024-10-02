
# Drug Response Prediction Using Multi-Omics Data

## Project Overview

This project aims to predict the drug response of cancer cell lines using multi-omics data. Specifically, the response to the drug **(5Z)-7-OXOZEAENOL** was predicted based on data from genomic, transcriptomic, and proteomic layers. The overall goal was to explore how different biological layers contribute to drug sensitivity and resistance, using machine learning (ML) and deep learning (DL) models. 

## Data Collection

Two main categories of datasets were utilized:
- **Drug Response Data**: From the **Genomics of Drug Sensitivity in Cancer (GDSC)** database, focusing on the IC50 values of (5Z)-7-OXOZEAENOL.
- **Multi-Omics Data**:
  - **Whole Exome Sequencing (WES)** for somatic mutations and copy number variations (CNVs).
  - **RNA-seq** for gene expression levels.
  - **Reverse Phase Protein Array (RPPA)** for protein expression profiles.

## Data Preprocessing

Key steps in data preprocessing included:
- **Handling Missing Values**: Imputation methods such as mean, median, or mode were applied depending on the data type.
- **Normalization**: Z-score normalization and min-max scaling were used to standardize data.
- **Feature Selection**: Techniques such as Principal Component Analysis (PCA) were used to reduce dimensionality and avoid overfitting.

## Data Integration

A **middle integration strategy** was employed to process and integrate the multi-omics data:
1. **Separate Processing**: Each dataset (WES, RNA-seq, RPPA) was processed independently to extract meaningful patterns.
2. **Integration Model**: The processed datasets were combined based on common cell line IDs, creating a unified dataset for model development.

## Machine Learning Models

Various ML models were applied to predict the response to (5Z)-7-OXOZEAENOL:
- **Logistic Regression**: A baseline model for binary classification.
- **Random Forest**: An ensemble method that ranks feature importance and captures complex data interactions.
- **Support Vector Machine (SVM)**: A model suited for high-dimensional datasets using the kernel trick to handle non-linear relationships.
- **Neural Networks**: A simple neural network was implemented to explore deep non-linear patterns.

### Model Performance

| Model               | Accuracy | F1-Score | Precision | Recall | ROC-AUC |
|---------------------|----------|----------|-----------|--------|---------|
| Logistic Regression  | 67.35%   | 0.68     | 0.66      | 0.71   | 0.75    |
| Random Forest        | 64.60%   | 0.64     | 0.65      | 0.63   | 0.72    |
| SVM                  | 65.97%   | 0.66     | 0.66      | 0.66   | 0.74    |
| Neural Network       | 65.64%   | 0.66     | 0.66      | 0.67   | 0.74    |

## Future Directions

- Generalizing the workflow for other drugs.
- Improving model performance using advanced techniques like **SWnet** for deep learning.
- Handling more complex interactions between multi-omics layers for improved prediction accuracy.


