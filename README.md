# Customer Transaction Machine Learning
A machine learning project focused on customer transaction analysis through clustering and classification.

## Project Overview
This project applies machine learning techniques to transaction data to identify customer segments using unsupervised learning and subsequently build classification models based on the resulting clusters.
The project was developed as part of the **Membangun Proyek Machine Learning** learning path at Dicoding Indonesia.

## Objectives
- Explore and prepare customer transaction data for machine learning.
- Identify customer segments using clustering.
- Evaluate and interpret the resulting clusters.
- Build classification models based on the clustering results.
- Evaluate and tune the classification models.

## Dataset
The dataset contains customer transaction information, including:

- Transaction amount
- Transaction type
- Location
- Device information
- Transaction channel
- Customer age
- Customer occupation
- Transaction duration
- Login attempts
- Account balance
- Transaction dates
The processed datasets used in the project are available in the `data/` directory.

## Methodology
### 1. Data Preparation
The project includes data preparation steps such as:
- Data loading
- Data inspection
- Missing value handling
- Duplicate handling
- Feature selection
- Categorical encoding
- Feature scaling
- Outlier handling
- Feature engineering

### 2. Customer Segmentation
K-Means clustering was used to identify groups of customers with similar transaction characteristics.
Cluster evaluation was performed using the **Silhouette Score**, while PCA was used to support visualization and interpretation of the clusters.

### 3. Classification
The resulting cluster labels were used as the target for a supervised classification stage.
The classification models include:
- Decision Tree
- Random Forest

### 4. Hyperparameter Tuning
Random Forest hyperparameters were optimized using `GridSearchCV`.
The tuning process explored:

- `n_estimators`: 50, 100, 200
- `max_depth`: 5, 10, 15
- 5-fold cross-validation

## Results
### Clustering
The K-Means clustering stage produced a Silhouette Score of approximately:
**0.5722**
The resulting clusters were subsequently analyzed based on their transaction and customer characteristics.

### Classification
The classification stage achieved the following result on the test set:
**Accuracy: 100%**
The evaluated metrics include:
- Accuracy
- Precision
- Recall
- F1-score

The tuned Random Forest model used:

```text
RandomForestClassifier(
    max_depth=15,
    n_estimators=50,
    random_state=42
)
