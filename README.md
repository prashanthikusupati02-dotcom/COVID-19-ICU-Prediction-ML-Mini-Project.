# COVID-19-ICU-Prediction-ML-Mini-Project.
Machine learning mini-project to predict COVID-19 ICU admission using baseline patient features.
# COVID-19 ICU Admission Prediction



## 1. Project Overview

This project uses supervised machine learning to predict whether a COVID-19 patient is likely to require ICU admission based on selected baseline patient information.

The project implements a Logistic Regression classifier and evaluates its performance using standard classification metrics and visualizations.

## 2. Problem Statement

Early identification of patients who may require intensive care can support patient triage. The objective is to classify patients into two categories:

- **Non-ICU (0):** ICU admission is not indicated by the dataset label.
- **ICU (1):** ICU admission is indicated by the dataset label.

This is an educational machine learning project, not a clinically validated medical prediction system.

## 3. Dataset

- Number of records: 81
- Original columns: 7
- Target variable: Intensive care unit
- Selected predictors:
  - Baseline clinical score
  - Sex
  - Baseline scanner

The ICU labels are converted from `NO` and `YES` to `0` and `1`. Categorical predictors are converted using one-hot encoding.

## 4. Methodology

1. Load and inspect the dataset.
2. Explore the columns and target distribution.
3. Convert ICU labels to binary values.
4. Encode categorical features using one-hot encoding.
5. Split the data into 80% training and 20% testing sets using stratification.
6. Train a Logistic Regression classifier.
7. Evaluate predictions using accuracy, precision, recall, F1-score, a confusion matrix and ROC-AUC.
8. Visualize the model's evaluation results.

## 5. Results

| Metric | Result |
|---|---:|
| Accuracy | 88.24% |
| ROC-AUC | 0.9929 |
| ICU precision | 1.00 |
| ICU recall | 0.71 |
| ICU F1-score | 0.83 |

These results are based on a test set of 17 records. The model missed two actual ICU cases, and its performance requires further validation.

## 6. Tools and Technologies

- Python
- Google Colab
- Pandas and NumPy
- Scikit-learn
- Matplotlib and Seaborn
- Logistic Regression

## 7. Repository Structure

- `notebooks/` – Jupyter notebook containing the implementation
- `report/` – Final project report in PDF format
- `presentation/` – Project presentation slides
- `requirements.txt` – Python dependencies for local execution

## 8. How to Run

### Option A: Google Colab

1. Open the notebook in `notebooks/`.
2. Open it in Google Colab.
3. Upload the permitted dataset spreadsheet if it is not already available.
4. Confirm that the dataset path matches the notebook.
5. Run the cells from top to bottom.
6. Review the evaluation metrics and plots.

### Option B: Local Python Environment

1. Clone or download this repository.
2. Install the required packages using `pip install -r requirements.txt`.
3. Place the permitted dataset spreadsheet at the path expected by the notebook, or update the path.
4. Open the notebook using Jupyter Notebook or JupyterLab.
5. Run all cells in order.

## 9. Limitations and Future Scope

- The dataset contains only 81 records.
- The test set contains only 17 records.
- The model uses selected baseline features rather than radiomics features extracted directly from CT images.
- The results may vary with different data splits.
- Future work may include cross-validation, comparison with other classifiers, additional permitted features and independent validation.

## 10. Reference

Zhan, Xianghao, and Yiheng Li. *CT-based Patient Triage of COVID-19: Radiomics Prediction of ICU Admission, Mechanical Ventilation, and Death of Patients.*


