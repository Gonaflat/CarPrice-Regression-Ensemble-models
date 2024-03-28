# CarPrice-Regression-Ensemble-Models-
A Chinese automobile company Geely Auto aspires to enter the US market by setting up their manufacturing unit there and producing cars locally. They have contracted an automobile consulting company to understand the factors on which the pricing of cars depends. Specifically, they want to understand the factors affecting the pricing of cars in the American market, since those may be very different from the Chinese market. The company wants to know:

Which variables are significant in predicting the price of a car
How well those variables describe the price of a car

Goal: Build a regression model that accurately predicts car prices and performs well on new data. Quality data preprocessing for statistical analysis and corresponding data visualization are also required.

What was applied?
1. Initial visualization: Histograms for data distribution visualization, Box Plot for outliers visualization, Count Plot for visualizing the number of data in each feature, and scatter plots for data distribution visualization. 
2. Data in 'Object' format were converted to categorical data. 
3. Missing values were processed, as well as duplicates. 
4. The names of incorrectly entered cars were corrected.
5. A correlation analysis was conducted between features, including visual analysis on a correlation map, and the 'variance_inflation_factor' method was used to identify multicollinearity among features, as regression models are highly dependent on it

What models and evaluation were applied? Various models were developed, including Linear Regression, Ridge Regression, Lasso Regression, and XGBoost. A/B testing was conducted, altering parameters such as the inclusion/exclusion of regularization and the use or non-use of BoxCox transformation for data normalization. All applicable models incorporate hyperparameter tuning (you can review the code for details).
- Linear Regression
   - A pipeline with a Scaler - MinMaxScaler, and model - LinearRegression was created.
   - Subsequently, a cross-validation score evaluation was conducted.
   - The evaluation methods: R2 Score, MSE (Mean Squared Error), and STD Deviation.
- Lasso Regression
   - A pipeline with a Scaler - MinMaxScaler, and model - LassoRegression was created.
   - Param Grid:
     - Lasso_alpha : [0.1, 1.0, 10.0]
   - GridSearch
   - The evaluation methods: R2 Score, MSE (Mean Squared Error), and STD Deviation.
- Ridge Regression
   - A pipeline with a Scaler - MinMaxScaler, and model - RidgeRegression was created.
   - Param Grid:
     - ridge__alpha : [0.1, 1.0, 10.0],
     - ridge__solver : ['auto', 'svd', 'cholesky', 'lsqr', 'sparse_cg', 'sag', 'saga']
   - GridSearch
   - The evaluation methods: R2 Score, MSE (Mean Squared Error), and STD Deviation.
- XGBoost
   - A pipeline with a Scaler - MinMaxScaler, and model - XGBoost was created.
   - Param Grid:
    - xgbreg__n_estimators: [100, 200],
    - xgbreg__max_depth: [3, 4, 5],
    - xgbreg__learning_rate: [0.01, 0.1],
    - xgbreg__subsample: [0.8, 1.0]
   - GridSearch
   - The evaluation methods: R2 Score, MSE (Mean Squared Error), and STD Deviation.

A numerical evaluation of the model's statistical indicators was conducted, along with a visual assessment using a Q-Q plot (to analyze the residuals of a regression model — the differences between observed and predicted values).
