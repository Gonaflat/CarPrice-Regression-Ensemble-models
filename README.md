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
