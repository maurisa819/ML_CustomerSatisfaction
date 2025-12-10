This folder contains two Jupyter notebooks that show the full modeling work I did before writing the final report. They include my early experiments, baseline model results, and the full tuning process.

1. preliminaryResults.ipynb (Milestone 3)

This notebook contains the first full round of modeling I completed using the cleaned training dataset. It includes:

- Initial data splits (train/validation)

- Early Random Forest and XGBoost models before any tuning

- Baseline performance using accuracy, F1, confusion matrices, and ROC curves

- First observations about class imbalance (showing the minority class was under-detected)

- Initial feature importance comparisons

- Early interpretation of model behavior and errors

Why it matters:
These results guided all the improvements made. This notebook documents the foundation of the project what the models looked like before tuning, what problems appeared (like imbalance), and why later steps were necessary. It shows the full preliminary modeling process that eventually led to the refined pipeline.



2. ModelTuning.ipynb (Milestone 4 — Tuning & Improved Pipeline)

What’s inside:
This notebook contains the upgraded modeling pipeline and tuning experiments, including:

- Oversampling with RandomOverSampler inside an imblearn.Pipeline

- Class imbalance handling using:

	- Oversampling

	- class_weight options for Random Forest

	- XGBoost’s scale_pos_weight

- Full RandomizedSearchCV hyperparameter tuning for both models

- Final tuned Random Forest and XGBoost models

- Updated validation metrics focused on F1 for the positive class

- Feature importance visualizations

- Misclassification analysis for both models

- Threshold adjustment experiments, showing how lowering the threshold changes precision, recall, and F1

Why it matters:
This notebook shows the complete modeling work that produced the improved models. It demonstrates how imbalance was handled, how parameters were optimized, and how threshold adjustments were evaluated to improve recall for the minority class. Much of this detailed analysis does not appear in full in the final milestone report, so this file gives credit for the technical steps taken.
