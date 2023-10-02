
# GPU Configuration and Kernal Runtime Analysis

## Overview
This project aims to understand the relationship between various GPU configurations and their impact on kernal runtime. Different models were evaluated to predict the GPU runtime based on its configurations, with a focus on both interpretability and prediction accuracy.

## Dataset Insights
- The dataset contains information about different GPU configurations and their associated runtimes.
- Features in the dataset provide insights into the GPU's architectural and operational settings.
- Preprocessing steps applied to the data include:
  - **Outlier Removal**: Outliers were removed from the `Runtime` column based on the Interquartile Range (IQR) method.
  - **Log Transformation**: The `Runtime` distribution was log-transformed to address its skewness.
  - **Feature Scaling**: Features were scaled using `MinMaxScaler` to bring them to a similar scale.

## Models Evaluated
Several regression models were trained and evaluated to predict GPU runtime. The models include:
- Linear Regression
- Ridge Regression
- Lasso Regression
- Random Forest Regressor
- Simple Neural Network
- Gradient Boosting Regressor
- K-Neighbors Regressor
- Decision Tree Regressor

## Performance Metrics
The models were evaluated based on two primary metrics:
- **Mean Squared Error (MSE)**: Measures the average squared difference between the estimated values and the actual value.
- **R-squared (R²) Score**: Indicates the proportion of the variance in the dependent variable that is predictable from the independent variables.

## Key Findings
- The Random Forest Regressor and DecisionTreeRegressor were top performers based on MSE and R² Score.
- Linear, Ridge, and Lasso Regressions, while providing a basic understanding, might not be the most suitable models for this dataset.

## Future Work
Considerations for future improvements include:
- Hyperparameter tuning for better model performance.
- Feature engineering to derive new insights.
- Exploring more complex neural network architectures.
