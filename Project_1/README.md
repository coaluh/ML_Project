# Project 1 — Machine Learning Classifiers

**Course:** DASC 41103  
**Team:** Group 5  
**Members:** Jaxon Ham, Cody Uhl  

---

## Overview
This project compares multiple classification algorithms on the Adult dataset, following the rubric for Project 1:

- **Part 1:** Data preprocessing (missing values, categorical encoding, scaling).
- **Part 2:** Custom textbook-style implementations of Perceptron and Adaline (GD + SGD).
- **Part 3:** scikit-learn implementations of Perceptron, Logistic Regression, and SVM with GridSearchCV hyperparameter tuning.
- **Part 4:** Conceptual analysis of scaling, gradient descent, regularization, and decision boundaries.

We implement, train, evaluate, and visualize classifiers, and save validation predictions as required CSV files.

---

## Repository Contents
- `Group_5_Project_1_Code.ipynb` — Main Jupyter notebook with code, results, and plots.  
- `Group_5_Project1_Presentation.pptx` — Team presentation slides (15-minute overview + deep dive).  
- `Group_5_Perceptron_PredictedOutputs.csv` — Validation predictions for best Perceptron.  
- `Group_5_Adaline_PredictedOutputs.csv` — Validation predictions for best Adaline.  
- `Group_5_LogisticRegression_PredictedOutputs.csv` — Validation predictions for best Logistic Regression.  
- `Group_5_SVM_PredictedOutputs.csv` — Validation predictions for best SVM.
- `README.md` — This file.

---

## How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/<your-org-or-user>/Project1-ML-Classifiers.git
   cd Project1-ML-Classifiers
   ```

2. Install dependencies:
  ```
  pip install -r requirements.txt
  ```

(Key packages: numpy, pandas, matplotlib, scikit-learn, jupyter)

3. Open the notebook:
  ```
  jupyter notebook Part1_2_3_4Solution.ipynb
  ```

4. Run all cells to reproduce preprocessing, training, evaluation, and plots.

## Results

Custom Perceptron: trained with textbook update rule, convergence monitored via misclassifications.

Custom Adaline (GD + SGD): trained with MSE minimization, convergence monitored via MSE curves.

Logistic Regression (GridSearchCV): best C = 1.0, accuracy ≈ 0.8486.

Linear SVM (GridSearchCV): best C = 1.0, accuracy ≈ 0.8463.

RBF SVM (GridSearchCV + refit): best C = 1.0, gamma = 0.05, accuracy ≈ 0.8488 (top performer).

Decision boundary visualizations included for Logistic Regression vs. SVM.

## Deliverables

The following files meet the rubric’s required outputs:

  Group_5_Perceptron_PredictedOutputs.csv

  Group_5_Adaline_PredictedOutputs.csv

  Group_5_LogisticRegression_PredictedOutputs.csv

  Group_5_SVM_PredictedOutputs.csv

Each CSV contains a single column pred with the predicted class for each validation input.

## Notes

Validation labels were not provided, so reported scores use cross-validation on the training data.

Official validation accuracy will be computed by the graders.

Slides accompany the notebook to summarize findings and conceptual insights.
