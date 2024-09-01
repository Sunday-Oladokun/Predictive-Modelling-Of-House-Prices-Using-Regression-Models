# Predictive Modelling of House Prices

**A Comprehensive Report on a Machine Learning Project**  
*Prepared by: Oladokun Sunday Obasanjo*

## Project Overview

In this capstone project, I applied my data science and machine learning skills to develop a predictive model for house prices. The project involved several critical steps: data cleaning, exploratory data analysis (EDA), feature engineering, model training, and evaluation. Using a real-world dataset, the goal was to build a robust model that accurately predicts house prices based on various features, offering valuable insights into the factors influencing property values.

## Problem Statement

Predicting house prices is challenging due to the multitude of factors influencing property values, including physical attributes like size and location, as well as external variables such as market trends and economic conditions. These variables interact in complex ways, affecting prices to varying degrees. Accurate price predictions can benefit buyers, sellers, real estate agents, financial institutions, and investors by enabling informed decisions and fair valuations.

This project aims to address the challenge of accurate property valuation by developing a machine learning model that leverages features such as physical characteristics, location, and condition of the houses. The objective is to create a model that effectively captures the intricate relationships between these features and the sale price, providing a reliable tool for stakeholders in the real estate market.

## Project Objective

### General Objective:
To accurately predict house prices using machine learning models and identify the most effective approach for achieving this goal.

### Specific Objectives:
1. **Data Cleaning and EDA:** Prepare and understand the dataset through thorough cleaning and analysis.
2. **Feature Engineering and Encoding:** Enhance the model's predictive capabilities by engineering features and encoding variables appropriately.
3. **Model Training, Evaluation, and Optimization:** Train, evaluate, and optimize multiple machine learning models to determine the best-performing one for predicting house prices.

## Methodology

### Data Collection
The dataset used for this project is titled "Housing Sales: Factors Influencing Sale Prices" from Kaggle. It includes 18 features and 2,413 observations, detailing property attributes such as lot size, building type, house style, and sale prices. This data was ideal for analyzing real estate market trends and developing predictive models.

### Data Cleaning
1. **Typographical Error Correction:** Verified and corrected categorical and numerical features to ensure data integrity.
2. **Numerical Feature Validation:** Checked for unusual characters in numerical features, confirming data cleanliness.
3. **Handling "Year Built":** Chose not to convert "Year Built" to datetime, considering it more meaningful as an integer.
4. **Outlier Analysis:** Identified and handled 561 outliers, creating two datasets: one with outliers (`df`) and one without (`df2_without_outliers`) to compare model performance.

### Exploratory Data Analysis (EDA)
1. **Non-Graphical and Graphical Univariate Analysis:** Explored frequency distributions, statistical summaries, histograms, and boxplots.
2. **Non-Graphical and Graphical Multivariate Analysis:** Investigated relationships between features and the target variable, using correlation analysis, groupby, ANOVA, pairplots, and heatmaps.
3. **Key Outcome:** Gained insights into feature distributions and their impact on the target variable, informing feature selection for modeling.

### Feature Engineering and Selection
New features, such as house age and decade built, were created to enhance model performance. Features were selected based on their effect on the target variable, resulting in three datasets for machine learning:
1. `training_ml_df`: Training set with outliers.
2. `test_ml_df`: Test set with outliers.
3. `df2_without_outliers_ml`: Dataset without outliers.

### Machine Learning
Three models were trained and tested on the datasets, both with and without outliers:
1. **Linear Regression:** Chosen for its simplicity, interpretability, and efficiency.
2. **Random Forest Regressor:** Selected for handling non-linearity, providing feature importance, and robustness.
3. **XGBoost Regressor:** Preferred for its high performance, ability to handle large datasets, and feature engineering capabilities.

All models were evaluated using Root Mean Square Error (RMSE), Mean Squared Error (MSE), and R² scores. Visual evaluations included scatter plots and bar charts to assess model performance.


## Conclusion
The project successfully developed and evaluated multiple machine learning models for predicting house prices, offering a robust tool for stakeholders in the real estate market. The final model, selected based on evaluation metrics, provides accurate and reliable price predictions, helping to better understand the factors influencing property values.

The XGBoost Regressor emerged as the best performer in our analysis, particularly when trained on the dataset without outliers. This model demonstrated significantly lower errors, as indicated by the Mean Squared Error (MSE) and Root Mean Squared Error (RMSE), and exhibited superior explanatory power with a higher R-squared (R²) value.

The impact of outliers on model performance was substantial. Generally, removing outliers led to improved performance across all models. However, the most notable enhancement was observed in the XGBoost model, highlighting its sensitivity to outliers and its ability to benefit greatly from their removal.
In terms of model robustness, both the Random Forest and XGBoost models showed greater resilience to outliers compared to Linear Regression. Despite this, all models experienced performance gains when outliers were removed, underscoring the importance of outlier management in achieving accurate predictions.


## Future Work
Future enhancements could include exploring additional features, incorporating more complex models, and deploying the final model for real-world applications.

## Acknowledgments
Thank you to Kaggle for providing the dataset and to all those who contributed to the successful completion of this project.
 
