# California Housing Price Prediction

## Project Overview

This project explores housing price prediction using the California Housing dataset. Three regression models—Ordinary Least Squares (OLS), Ridge, and Lasso—are trained and evaluated to compare their predictive performance.

The project covers exploratory data analysis, feature engineering, preprocessing, hyperparameter tuning, and residual error analysis.

## Dataset

The California Housing dataset contains 20,640 observations describing housing districts in California.

Features include geographical coordinates, housing age, room and bedroom counts, population, household information, median income, and ocean proximity.

The target variable is `median_house_value`.

## Technologies Used

- Python
- Pandas and NumPy
- Matplotlib and Seaborn
- Scikit-learn
- Jupyter Notebook

## Methodology

1. **Exploratory Data Analysis:** Examined feature distributions, missing values, and correlations.
2. **Feature Engineering:** Created three ratio features and an interaction feature combining median income and housing age.
3. **Data Splitting:** Divided the dataset into 80% training and 20% testing data.
4. **Preprocessing:** Applied median imputation, standardization, and one-hot encoding through Scikit-learn pipelines.
5. **Model Training:** Trained OLS, Ridge, and Lasso regression models.
6. **Hyperparameter Tuning:** Used GridSearchCV with five-fold cross-validation to tune Ridge and Lasso regularization.
7. **Evaluation:** Compared models using MAE, RMSE, and R², supported by actual-versus-predicted plots and residual distributions.

## Results

| Model | MAE | RMSE | R² |
|---|---:|---:|---:|
| OLS | $49,376.49 | $69,048.19 | ~0.64 |
| Ridge | $49,382.63 | $69,056.22 | ~0.64 |
| Lasso | $49,377.34 | $69,049.25 | ~0.64 |

OLS achieved the lowest prediction errors, although all three models performed similarly.

Adding an interaction feature between median income and housing age slightly improved predictive accuracy across all three models.

Residual analysis identified larger errors for some housing districts, particularly among higher-valued observations.

## Running the Project

1. Clone or download the repository.
2. Install the required dependencies using the root `requirements.txt` file:

   ```bash
   pip install -r requirements.txt
   ```

3. Open `Task-2-Housing-Price-Prediction/housing_price_prediction.ipynb` in Jupyter Notebook or VS Code.
4. Run the notebook cells in order.

Ensure that the housing dataset is available in the location expected by the notebook.

## Conclusion

The results demonstrate that linear regression provides a useful baseline for housing price prediction. Ridge and Lasso regularization did not substantially improve performance in this experiment, while interaction feature engineering produced a small improvement.

Further work could investigate nonlinear models and additional feature engineering techniques.