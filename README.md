# Loan-Repayment-Classification
Comparative classification of loan repayment outcomes using KNN, Decision Tree, SVM and Logistic Regression.

![Python](https://img.shields.io/badge/Python-3.x-3776AB?logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-Classification-F7931E?logo=scikitlearn&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-2E7D32)

A reproducible comparison of four supervised-learning algorithms for classifying historical loan outcomes as **paid off** or **in collection**.

This project was completed as part of IBM's *Machine Learning with Python* coursework and subsequently revised into a leakage-safe, professionally documented model-comparison workflow.

## Project objective

Evaluate how effectively standard classification algorithms can distinguish between paid-off and collection outcomes using basic loan and borrower attributes.

Models evaluated:

- K-Nearest Neighbours
- Decision Tree
- Support Vector Machine
- Logistic Regression

## Methodology

- Leakage-safe preprocessing with scikit-learn pipelines
- Numeric scaling and categorical one-hot encoding
- Five-fold stratified cross-validation
- Hyperparameter tuning using macro F1
- Final assessment on a separate external test set
- Comparison across accuracy, balanced accuracy, F1, Jaccard, ROC-AUC and log loss

## Results

The **Decision Tree** produced the strongest cross-validation macro F1 and was therefore selected as the recommended model.

| Evaluation measure | Result |
|---|---:|
| Cross-validation macro F1 | 0.655 |
| External-test macro F1 | 0.692 |
| External-test balanced accuracy | 0.743 |
| External-test accuracy | 0.722 |

The results are educational rather than production-grade because the dataset is small and contains a limited set of explanatory variables.

## Repository contents

| File | Description |
|---|---|
| [`Loan_Repayment_Classification.ipynb`](Loan_Repayment_Classification.ipynb) | Complete analysis, model tuning, evaluation and interpretation |
| [`README.md`](README.md) | Project overview and usage guidance |

## Run the notebook

Clone the repository and install the principal dependencies:

```bash
git clone https://github.com/anupamctg/loan-repayment-classification.git
cd loan-repayment-classification
pip install pandas numpy matplotlib scikit-learn jupyter
jupyter notebook Loan_Repayment_Classification.ipynb
```

The notebook retrieves the original IBM datasets from their published locations. Local fallback paths are also supported under a `data/` directory.

## Responsible use

This is an educational portfolio project, not a credit-scoring or lending-decision system. The sample size, available variables and demographic features are insufficient for responsible production use without comprehensive validation, fairness assessment, governance and regulatory review.

## Attribution

- **Implementation, analysis and portfolio revision:** [Anupam Paul](https://github.com/anupamctg)
- **Original instructional framework and datasets:** IBM Skills Network / Cognitive Class

## Author

**Anupam Paul** — Data, Analytics and AI Transformation Leader  
[LinkedIn](https://www.linkedin.com/in/anupam-paul/) · [Portfolio](https://www.anupampaul.page/)
