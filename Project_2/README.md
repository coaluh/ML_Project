Project 2 — Multilayer Perceptron (Adult Income Dataset)

Course: DASC 41103
Team: Group 5
Members: Jaxon Ham, Cody Uhl

Overview

This project applies a Multilayer Perceptron (MLP) neural network to the Adult Income dataset to predict whether an individual earns more than $50 000 per year. The work follows the rubric for Project 2 and demonstrates the full machine-learning pipeline:

Part 1: Data loading and preprocessing (missing values, categorical encoding, scaling).

Part 2: Model development using MLPClassifier in scikit-learn with Pipeline + ColumnTransformer.

Part 3: Hyperparameter tuning via GridSearchCV with 5-fold cross-validation.

Part 4: Model evaluation (accuracy, F1, confusion matrix, ROC/PR curves, learning curves).

Part 5: Reflection & conceptual analysis (architecture choice, overfitting control, ethical concerns, activation functions).

We train, evaluate, and visualize MLP models and save the required validation predictions for grading.

Repository Contents

project_2.ipynb — Main Jupyter Notebook containing code, results, and plots.

artifacts_part1/Group_05_MLP_PredictedOutputs.csv — Validation predictions from the best MLP model (1 = > 50K, –1 = ≤ 50K).

artifacts_part1/best_mlp_pipeline.joblib — Saved pipeline (model + preprocessing).

artifacts_part1/cv_results.csv — GridSearchCV summary of hyperparameter scores.

slides/Project2_MLP.pdf — Team presentation slides (15-minute overview + technical discussion).

requirements.txt — Dependencies for Python environment.

README.md — This file.

How to Run

Clone the repository and open the Project 2 folder:

git clone https://github.com/coaluh/ML_Project.git
cd ML_Project/Project2-MLP


Install dependencies:

pip install -r requirements.txt


(Key packages: numpy, pandas, matplotlib, scikit-learn, joblib, jupyter)

Open and run the notebook:

jupyter notebook project_2.ipynb


Run all cells to reproduce preprocessing, training, evaluation, and plots.
Outputs will be saved in artifacts_part1/.

Results

Best Model Configuration

Hyperparameter	Setting
Hidden Layers	(64, 32)
Activation	ReLU
Alpha (L2)	0.01
Learning Rate	0.001
Solver	Adam

Performance

Metric	CV Accuracy	Test Accuracy	Macro F1	Weighted F1
Score	0.8537	0.8495	0.78	0.84

Confusion Matrix (Test)

[[3666  290]
 [ 494  760]]


Precision/Recall/F1 for ≤ 50K ≈ 0.88 / 0.93 / 0.90

Precision/Recall/F1 for > 50K ≈ 0.72 / 0.61 / 0.66

ROC-AUC ≈ 0.89, PR-AUC ≈ 0.78

Learning curves show minimal overfitting due to early stopping and regularization.

Deliverables

The following files satisfy the Project 2 rubric requirements:

Group_05_MLP_PredictedOutputs.csv — Validation predictions (1 = > 50K, –1 = ≤ 50K).

best_mlp_pipeline.joblib — Serialized best model and transformer.

cv_results.csv — Cross-validation hyperparameter results.

Project2_MLP.pdf — Presentation slides.

Each CSV contains a single column Prediction with signed output values for validation inputs.

Notes

Numeric features: 7  Categorical features: 8  Processed via ColumnTransformer.

All runs use random_state = 42 for reproducibility.

Early stopping (n_iter_no_change = 10) prevents overfitting.

Ethical considerations: model may reflect socio-demographic bias inherent to the Adult dataset; discussion included in Part 2 reflection.

Slides and notebook together provide a complete overview of model design, evaluation, and interpretability.
