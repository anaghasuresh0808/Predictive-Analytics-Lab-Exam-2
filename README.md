# Predictive Analytics Lab Exam-2

## Objective

To perform binary classification using machine learning techniques and evaluate model performance on a given dataset.

## Dataset

* Total entries: 1020
* Features:

  * Feature1 (Numerical)
  * Feature2 (Numerical)
* Target:

  * Binary classification (Yes / No)

## Exploratory Data Analysis (EDA)

* Checked dataset structure and data types using `.info()`
* Identified missing values in the target column (20 entries)
* Removed missing values using `dropna()`
* Detected extreme outliers in **Feature1** (value around 10000)
* Removed outliers to improve model performance
* Visualized data using:

  * Scatter plots (class distribution)
  * Histograms (feature distribution)
  * Correlation heatmap
* Observed a **non-linear (circular) pattern** in the dataset

## Data Preprocessing

* Converted target variable (Yes/No) into numeric form using **LabelEncoder**
* Split dataset into training and testing sets (80:20 ratio)
* Applied **StandardScaler** for feature scaling

## Model Building

* Initial Model:

  * Logistic Regression (linear)
  * Result: Poor performance due to non-linear data

* Final Model:

  * Polynomial Features (degree = 2) + Logistic Regression
  * Implemented using **Pipeline**
  * Successfully captured non-linear relationships

## Decision Boundary

* Linear Logistic Regression → Straight line (underfitting)
* Polynomial Logistic Regression → Curved boundary (better fit)
* Decision boundary plotted using meshgrid and contour plots

## Model Evaluation

* Accuracy: **96%**

### Confusion Matrix

```
[[151   8]
 [  0  41]]
```

### Classification Report

* High precision and recall
* F1-score indicates strong overall performance
* Achieved **100% recall for minority class**, indicating no false negatives

## Conclusion

The dataset exhibited a non-linear pattern which could not be captured by a simple linear model.
By applying polynomial feature transformation, the model was able to learn complex decision boundaries, resulting in a significant improvement in classification accuracy and overall performance.

## Tools & Libraries Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn

## Repository Contents

* Dataset file (`.csv`)
* Python code (`.ipynb` / `.py`)
* README.md

---
