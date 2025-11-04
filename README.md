# DASC 41103 — Machine Learning & Data Science Projects

Course: DASC 41103
Team: Group 5
Members: Jaxon Ham, Cody Uhl

## Overview

This repository contains our team’s projects for DASC 41103.
Each project folder includes its own code, notebook(s), deliverables, and a detailed README.md describing requirements, implementation, and results.

## Repository Structure
```
├── Project1-ML-Classifiers/
│   ├── Group_5_Project_1_Code.ipynb
│   ├── Group_5_Project1_Presentation.pptx
│   ├── Group_5_Perceptron_PredictedOutputs.csv
│   ├── Group_5_Adaline_PredictedOutputs.csv
│   ├── Group_5_LogisticRegression_PredictedOutputs.csv
│   ├── Group_5_SVM_PredictedOutputs.csv
│   ├── README.md
│   └── requirements.txt
├── Project2-MLP/
|   ├── Group5_Project2.ipynb
|   ├── artifacts_part1/
│      └── Group_05_MLP_PredictedOutputs.csv
|   ├── Group5_Project2_Presentation.pptx
│   └── README.md
├── Project3-<Name>/
│   ├── ...
│   └── README.md
└── README.md   ← (this file)
```

## Projects
Project 1 — Machine Learning Classifiers

Preprocessing, custom Perceptron/Adaline, sklearn Logistic Regression & SVM.

Validation predictions exported as required CSVs.

Includes Jupyter notebook, presentation, and results.

See Project1-ML-Classifiers/README.md
 for full details.

## 🚀 Project 2 — Multilayer Perceptron (Adult Income Dataset)

Predict whether an individual earns > \$50K per year using demographic and employment data.

This project demonstrates a full end-to-end **machine-learning pipeline** in Python using `scikit-learn`:

- Loads and cleans the UCI Adult Income dataset  
- Preprocesses data with a **ColumnTransformer** (numeric → impute + scale | categorical → impute + one-hot)  
- Trains and tunes an **MLP Classifier** via `GridSearchCV`  
- Evaluates performance and fairness implications  
- Generates validation predictions in the required CSV format

Project 3 — Placeholder Title

Will include description, scope, and deliverables once assigned.

Folder: Project3-<Name>/

## How to Use

Clone the repository:
```
git clone https://github.com/<your-org-or-user>/DASC41103-Projects.git
cd DASC41103-Projects
```

Navigate into the project folder you want to run:
```
cd Project1-ML-Classifiers
```

Follow the instructions in that project’s README.md.

## Notes

Each project is self-contained: all notebooks, data inputs (if allowed), outputs, and presentation slides are inside its folder.

Environment setup for each project is listed in that project’s requirements.txt.

Top-level repo serves as the portfolio hub for all projects.
