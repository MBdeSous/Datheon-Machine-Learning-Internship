# Iris Flower Classification

Machine Learning & Data Science Internship — Task 1

## Project Overview

This project focuses on classifying Iris flower species using two machine learning algorithms: Logistic Regression and Decision Tree.

The models are trained and evaluated using the Iris dataset to compare their classification performance. The project covers data exploration, preprocessing, model training, evaluation, and visualization.

## Dataset

The Iris dataset contains 150 samples belonging to three species:

- Setosa
- Versicolor
- Virginica

Each sample contains four numerical features: sepal length, sepal width, petal length, and petal width.

These measurements are used to predict the flower species.

## Technologies Used

- Python
- Pandas and NumPy
- Scikit-learn
- Matplotlib and Seaborn
- Jupyter Notebook

## Methodology

### 1. Exploratory Data Analysis

The dataset was examined for missing values and explored using scatter plots and a correlation heatmap to identify relationships between the flower measurements.

### 2. Data Preprocessing

The dataset was divided into 80% training data and 20% testing data. StandardScaler was applied to standardize the features used for Logistic Regression.

### 3. Model Training

Two classification algorithms were implemented:

- **Logistic Regression:** Estimates the probability of each flower belonging to a particular species.
- **Decision Tree:** Uses feature-based decision rules to classify the flowers.

### 4. Model Evaluation

Both models were evaluated using accuracy, precision, recall, and F1-score.

Additional evaluation methods included:

- Confusion matrices to identify classification errors.
- ROC curves and AUC scores to assess class separation.
- Feature importance analysis to identify influential measurements.
- Decision boundary visualizations to compare how the models separate the species.

## Results

Both models achieved an accuracy of **93.3%**, correctly classifying 28 out of 30 test samples.

The ROC curve analysis produced the following AUC scores:

| Species | Logistic Regression | Decision Tree |
|---|---|---|
| Setosa | 1.00 | 1.00 |
| Versicolor | 0.99 | 0.92 |
| Virginica | 0.99 | 0.92 |

Although both models achieved the same accuracy, Logistic Regression produced slightly higher AUC scores for Versicolor and Virginica.

Feature importance analysis showed that petal length and petal width contributed the most to the Decision Tree's predictions.

## Running the Project

1. Ensure Python and Jupyter Notebook are installed.
2. Install the required dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. Open `iris_classification.ipynb`.
4. Run all notebook cells in order.

Ensure `iris.csv` is available in the same directory as the notebook.

## Conclusion

Both Logistic Regression and Decision Tree performed well on the Iris classification task, achieving identical accuracy on the selected test dataset.

The additional visualizations highlighted differences in how the models classify the three species, while the feature importance analysis identified the measurements most relevant to the Decision Tree.

The project demonstrates a complete supervised machine learning workflow, from preparing and exploring the dataset to training, evaluating, and comparing classification models.