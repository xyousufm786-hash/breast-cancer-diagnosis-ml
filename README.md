# Breast Cancer Diagnosis: Comparing ML Classifiers

Compares logistic regression, SVM, random forest and k-NN on the **Wisconsin Diagnostic Breast Cancer** dataset (569 patients, 30 features), then tunes the decision threshold for patient safety: missing a malignant tumour is far worse than a false alarm.

## Highlights
| Model | CV ROC-AUC |
|---|---|
| **SVM (RBF)** | **0.994** |
| Logistic regression | 0.991 |
| Random forest | 0.988 |
| k-nearest neighbours | 0.986 |

- At a lowered threshold of 0.35, the SVM catches **98.1% of malignant cases** with **97.9% overall accuracy** on the held-out test set
- Tumour size and shape irregularity (worst radius, perimeter, concave points) carry the most signal

## Data
Bundled with scikit-learn (`load_breast_cancer`), so no download is needed.

> Educational project, not a medical tool.

## Run it
```bash
pip install -r requirements.txt
jupyter notebook breast-cancer-diagnosis-ml.ipynb
```
Then **Run → Run All Cells**. Results are reproducible (fixed random seeds).

**Stack:** Python · scikit-learn · pandas · matplotlib
