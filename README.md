# Machine-Learning-Project
Car Price Prediction Project - Analysis & Insights

1.Data Preprocessing

 Steps Taken:
  * Loaded the dataset and checked for missing values.
  * Handled missing or incorrect values appropriately.
  * Transformed the data to fix the abnormality in skewness.
  * Encoded categorical variables (e.g., car brands, fuel types) using one-hot encoding.
  * Standardized/normalized numerical features for better model performance.
  
 Insights:
  * Proper data preprocessing ensured that the dataset was clean and ready for machine learning models.
  * Encoding categorical variables allowed the models to interpret non-numeric features effectively.


2️. Outlier Detection & Treatment

 Steps Taken:
  * Used boxplots to visualize and detect outliers in numerical variables.
  * Capped extreme values using IQR-based capping or transformation techniques.
   
 Insights:
  * Outlier detection helped in identifying extreme values that could negatively affect model performance.
  * Capping ensured that the dataset maintained its integrity while avoiding overfitting to extreme values.


3. Feature Selection
   
 Steps Taken:
  * Initially used a correlation heatmap but found it ineffective for feature selection.
  * Applied feature importance using the Gradient Boosting Regressor and Random Forest Regressor  to identify significant variables affecting car prices.
    
 Insights:
  * The correlation heatmap was not a reliable method for feature selection due to multicollinearity among variables.
  * Feature importance scores from Gradient Boosting Regressor and Random Forest Regressor revealed that curb weight,highwaympg, engine size, horsepower,carlength  had a strong impact on car price predictions.

4️.Model Implementation & Evaluation

 Steps Taken:
  *Implemented five regression models:
    - Linear Regression
    - Decision Tree Regressor
    - Random Forest Regressor
    - Gradient Boosting Regressor
    -Support Vector Regressor (SVR)
    
 *Split the dataset into training (80%) and testing (20%) sets.
 *Evaluated models based on:
    1.R-squared (R²) → Measures how well the model explains variance.
    2.Mean Squared Error (MSE) → Measures the average squared difference between predicted and actual prices.
    3.Mean Absolute Error (MAE) → Measures the average absolute difference between predicted and actual prices.

 Insights:
  * Gradient Boosting Regressor performed the best, achieving an R² of 0.958 with the lowest MSE and MAE, making it the most accurate model.
  * Random Forest Regressor was the second-best, performing slightly lower than Gradient Boosting Regressor.
  * Linear Regression & Decision Tree Regressor showed moderate accuracy.
  * Support Vector Regressor performed the worst, failing to learn meaningful patterns from the data.

5️. Hyperparameter Tuning

 Steps Taken:
  *Performed hyperparameter tuning on Gradient Boosting Regressor and Random Forest Regressor using GridSearchCV to optimize parameters like n_estimators, max_depth, and min_samples_split.
  *Evaluated the tuned model's performance.
  
 Insights:
  * The tuned Random Forest model achieved R² = 0.920, with improved MSE and MAE, confirming that tuning enhanced accuracy.
  * The tuned Gradient Boosting model had negative impact because its performance slightly decreased copared to the initial values.
