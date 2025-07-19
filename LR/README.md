# Logistic Regression for Wine Quality Prediction

This project applies **Logistic Regression** to predict the quality of red wine based on physicochemical tests. It includes hyperparameter tuning using GridSearchCV to find the best-performing model.

##  Dataset
- The dataset used is `winequality-red-sorted.csv`.
- It contains physicochemical properties of red wine samples and their corresponding quality scores.
- Each row represents a sample, and the features include variables like acidity, sugar content, pH, alcohol, etc.

##  Preprocessing
- The features are normalized using **MinMaxScaler**.
- The dataset is split into training (80%) and testing (20%) sets.

##  Model
- **Logistic Regression** is used with hyperparameter tuning via **GridSearchCV**.
- The following hyperparameters were tuned:
  - `C`: [0.1, 1, 10]
  - `penalty`: ['l1', 'l2']
  - `max_iter`: [500, 1000, 2000]
- The best model is selected based on cross-validation accuracy.

##  Evaluation
- The model is evaluated on the test set using:
  - Accuracy
  - Classification report
  - Confusion matrix

##  Visualization
- Accuracy scores for different hyperparameter combinations can be visualized (optional, not included in this version).

##  Prediction
- The best model is used to predict the quality of a new wine sample with the following features:
```python
[7.4, 0.66, 0.00, 1.21, 0.994, 3.51, 0.56, 9.5, 2.75, 1.02, 5.25]
```

##  Files
- `Logistic_Regression_Wine_Quality.ipynb`: Jupyter notebook with all code and explanation.
- `requirements.txt`: Python dependencies for running the project.

##  Requirements
Make sure to install required libraries before running the notebook:

```bash
pip install -r requirements.txt
```
