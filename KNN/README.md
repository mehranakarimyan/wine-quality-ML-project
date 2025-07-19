🍷 Wine Quality Prediction with K-Nearest Neighbors (KNN)

Project Objective  

The goal of this project is to predict the quality of red wine based on its physicochemical properties using a machine learning model. We use the **K-Nearest Neighbors (KNN)** classification algorithm, tune its hyperparameters, and visualize how model accuracy changes with different values of `k` (number of neighbors).

---
Dataset

We used the **Wine Quality dataset** from the **UCI Machine Learning Repository**:  
https://archive.ics.uci.edu/ml/datasets/Wine+Quality  

Specifically, the **red wine quality** dataset (`winequality-red.csv`) which contains 1599 samples and 12 columns:
- 11 numerical input features (like acidity, sugar, pH, alcohol)
- 1 target feature: wine quality score (integer from 3 to 8)

In this project, a pre-sorted version named `winequality-red-sorted.csv` is used.

---

Model Overview and Hyperparameter Tuning

We applied **K-Nearest Neighbors (KNN)**, a distance-based classifier.  
Since KNN performance depends heavily on the choice of `k` and weighting strategy, we performed a **GridSearchCV** with 5-fold cross-validation to find the best combination:

- **k values tested:** 3, 5, 7, 9, 11  
- **weighting strategies:** `uniform`, `distance`  

The data was scaled using **MinMaxScaler** before training, as KNN relies on distance metrics.

---

 Results  

After hyperparameter tuning:
- **Best Parameters:** `n_neighbors = 9`, `weights = 'distance'`
- **Test Set Accuracy:** **~72%**

The results of different k values and their corresponding accuracies were recorded and plotted for comparison.

---

Accuracy vs. Number of Neighbors

To better understand the effect of `k` on model performance, we plotted the model's cross-validated accuracy versus different `k` values.

![Accuracy vs k](plots/accuracy_vs_k.png)

*This plot clearly shows how accuracy changes as the number of neighbors increases, helping us choose the optimal `k`.*


How to Run  

1. Install the required packages:
```
pip install -r requirements.txt
```

2. Open the notebook:
```
jupyter notebook knn_wine_quality_final.ipynb
```

3. Run all cells sequentially.

---
Author  

m.k 
https://github.com/mehranakarimyan