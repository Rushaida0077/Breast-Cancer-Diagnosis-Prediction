# Breast Cancer Diagnosis Prediction Using KNN and K-Means

## Overview
This project predicts whether a breast cancer tumor is **malignant (M)** or **benign (B)** using:

1. **K-Nearest Neighbors (KNN)** – supervised classification  
2. **K-Means Clustering** – unsupervised exploration of natural clusters


## Dataset
- **Features:** 30 numeric variables (radius, texture, perimeter, area, smoothness, compactness, concavity, concave points, symmetry, fractal dimension)  
- **Target:** `diagnosis`  
  - `M` → 1, `B` → 0  
- **Dropped columns:** `id` and `Unnamed: 32`


## Preprocessing
1. **Encoding**
   - Converted `diagnosis` column:  
     `M → 1`, `B → 0`.

2. **Cleaning**
   - Dropped irrelevant columns: `id` and `Unnamed: 32`.

3. **Scaling**
   - Applied **Min-Max Normalization** to scale all feature columns between 0 and 1.

4. **Splitting**
   - Data was split into:
     - Training set: **80%**
     - Testing set: **20%**



## Machine Learning
### K-Means

- **Purpose**: Explore natural grouping of tumors.
- **Parameters**: `k = 2` clusters
- **Outcome**:
  - Cluster 0 and Cluster 1 roughly correspond to benign and malignant tumors.
  - Comparison with true labels helps understand separability of the dataset.

### KNN
- **Purpose**: Predict tumor type using a supervised learning approach.
- **Parameters**:
  - Number of neighbors: `k = 5`
  - Distance metric: Euclidean (default)
- **Training**: Trained on the 80% training data.
- **Prediction**: Tested on 20% test data.



## Evaluation
| Metric     | Result  |
|------------|---------|
| Accuracy   | 0.9649  |
| Precision  | 0.9535  |
| Recall     | 0.9535  |
| F1-Score   | 0.9535  |


## Libraries Used

- `pandas` – data manipulation    
- `scikit-learn` – machine learning algorithms (`KNeighborsClassifier`, `KMeans`, `MinMaxScaler`, `train_test_split`, `accuracy_score, precision_score, recall_score, f1_score` )  




## How to Run
1. Open `CSE_301_Assignment.ipynb` in Google Colab  
2. Upload `data.csv` if not already included  
3. Run all cells in order:
   - Preprocessing  
   - K-Means clustering  
   - KNN training and evaluation


## Files in Repository
- `CSE_301_Assignment.ipynb` – Complete notebook  
- `README.md` – This summary  



