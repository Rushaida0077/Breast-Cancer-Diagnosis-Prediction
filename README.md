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
1. Encoded `diagnosis` column (`M → 1`, `B → 0`)  
2. Applied **Min-Max Normalization** to all features  
3. Split dataset: **80% train / 20% test**



## Machine Learning
### K-Means
- **Clusters:** k = 2  
- Purpose: Explore natural separation of benign and malignant tumors  
- Comparison with true labels showed high correspondence with actual diagnoses

### KNN
- **Neighbors:** k = 5  
- Trained on 80% training data  
- Tested on 20% test data



## Evaluation
| Metric     | Result              |
|------------|---------------------|
| Accuracy   | 0.9649122807017544  |
| Precision  | 0.9534883720930233  |
| Recall     | 0.9534883720930233  |
| F1-Score   | 0.9534883720930233  |



## How to Run
1. Open `CSE_301_Assignment` in Google Colab  
2. Upload `data.csv` if not already included  
3. Run all cells in order:
   - Preprocessing  
   - K-Means clustering  
   - KNN training and evaluation


## Files in Repository
- `CSE_301_Assignment` – Complete notebook  
- `README.md` – This summary  



