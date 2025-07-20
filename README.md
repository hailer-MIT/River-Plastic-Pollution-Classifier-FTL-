# River Plastic Pollution Classifier – FTL Project

A machine learning project developed as part of the FTL Ethiopia PBL (Project-Based Learning) Labs, aimed at analyzing river plastic pollution levels using both **supervised** and **unsupervised** learning techniques.

## Problem Statement

Plastic pollution in rivers varies across regions, but there is no standardized method to identify or classify high-polluting rivers. Environmental authorities and researchers need automated tools to analyze river pollution data and categorize pollution levels for targeted cleanup efforts.


## Solution Overview

We designed a hybrid machine learning pipeline:
- **Classification**: Label rivers as *high* or *low* plastic contributors using **Logistic Regression**.
- **Clustering**: Group rivers based on pollution patterns using **K-Means Clustering** and visualized via **PCA**.


## Technical Details

- **Data Source**: A cleaned and preprocessed dataset hosted on Google Drive.
- **Supervised Learning**:
  - Defined a binary label based on plastic waste thresholds.
  - Trained a `LogisticRegression` model after feature scaling.
  - Evaluated using Accuracy, Precision, Recall, ROC AUC.
- **Unsupervised Learning**:
  - Applied `KMeans` on scaled features to create pollution clusters.
  - Used PCA for 2D visualization.
  - Validated cluster separation with **Silhouette Score**.

All data preprocessing (cleaning strings, converting percentages, handling missing values) was handled using `pandas`.



## Tools & Libraries Used

- **Python**: `pandas`, `numpy`, `matplotlib`, `seaborn`
- **ML & Evaluation**:
  - `scikit-learn` for modeling, splitting, scaling, evaluation
  - `KMeans`, `LogisticRegression`, `Silhouette Score`, `ROC AUC`
- **Visualization**: `matplotlib`, `seaborn`, `PCA` for cluster plots


## Results

| Task                     | Model/Score                      |
|--------------------------|----------------------------------|
| Logistic Regression      | Accuracy: ~93.9%, Precision: ~92% |
| K-Means Clustering       | Silhouette Score: **0.714**      |
| PCA Visualization        | Distinct cluster separation      |


## How to Run

> No dataset upload required — it auto-downloads from Google Drive.

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/River-Plastic-Pollution-Classifier-FTL.git
   cd River-Plastic-Pollution-Classifier-FTL
