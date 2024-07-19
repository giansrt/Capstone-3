# California House Prices Prediction

## Business Problem

<p style="text-align: justify;">
A real estate company in California was facing a major challenge in determining accurate prices for the properties they were selling or buying. Improper pricing can have significant negative impacts, both in the form of financial losses and lost business opportunities. Pricing too high can make properties difficult to sell, resulting in inventory build-up and increased operating costs. Conversely, a price that is too low can lead to losses as the property is sold below its true market value, hurting the company in the long run.
</p>

## Problem Statement

<p style="text-align: justify;">
Real estate companies in California face challenges in accurately determining the sale and purchase price of properties, which can have a significant impact on financial returns and business opportunities. Improper pricing can result in properties selling below market value or staying on the market too long, resulting in additional costs and potential losses. Therefore, companies need a solution that can optimize the pricing process by leveraging historical data and predictive analytics.

How can we utilize historical property data in California to develop a predictive model that can accurately forecast the average price of a home? This model should consider various factors that affect property values.
</p>

## Analytic Approach

To address the housing price prediction project in California, the analytical approach involves an in-depth analysis of the housing market data in the region. The steps are as follows:

**Understanding the Dataset**: This stage involves studying the available dataset, including the existing variables and how they may affect housing prices.

**Data Exploration**: Exploratory data analysis is performed to identify patterns or trends that may exist within the dataset. Data visualization is often used to better understand the relationships between variables and housing prices.

**Data Cleaning**: This process involves identifying and rectifying missing values, outliers, or invalid data.

**Feature Engineering**: New features can be created from the existing data to enhance model performance.

**Model Selection**: Based on the characteristics of the housing price prediction task, several commonly used machine learning models include linear regression, KNN, ridge, decision tree, random forest, and XGBoost.

**Model Training and Evaluation**: Machine learning models are trained using the training data and evaluated using appropriate metrics.

**Results Interpretation**: The results from the machine learning models are evaluated to understand the key factors influencing housing prices in California.

## Model Performance

### Before Tuning

| Model            | MAE            | Test MAPE     | Test R2      |
|------------------|----------------|---------------|--------------|
| XGBoost          | 28446.112405   | 0.156304      | 0.789591     |
| Random Forest    | 29501.281434   | 0.159021      | 0.772985     |
| Gradient Boosting| 32804.220262   | 0.177748      | 0.740565     |

### After Tuning

| Model                     | MAE            | MAPE          | R2           |
|---------------------------|----------------|---------------|--------------|
| XGBoost After Tuning      | 26662.975565   | 0.146036      | 0.812424     |
| Gradient Boosting         | 27758.391355   | 0.150729      | 0.798828     |
| Random Forest After Tuning| 29406.739273   | 0.158588      | 0.774732     |

## Conclusion

### Algorithm

Based on the evaluation of the modeling algorithm results, it can be concluded that **XGBoost Regressor** is the best algorithm. XGBoost demonstrated superior performance with the lowest MAE of 28446.112405 before tuning and 26662.975565 after tuning. The Random Forest Regressor also showed good performance but was still below XGBoost. Gradient Boosting showed improvement after tuning but remained below XGBoost.

### Evaluation Metrics

After tuning, XGBoost proved to be the algorithm with the best metrics. The MAE decreased from 28446.112405 to 26662.975565, and the R2 increased from 0.789591 to 0.812424. The decrease in MAPE from 0.156304 to 0.146036 also indicates an improvement in prediction accuracy. Although the improvements were not very significant, they were consistent across all evaluation metrics.

### Feature Importance

Based on the feature importance results, it can be concluded that location has a very significant impact on house prices in California. The feature 'ocean_proximity_INLAND' has the highest importance (0.613336), followed by 'median_income' (0.085319) and other location features such as 'ocean_proximity_NEAR BAY' (0.076327) and 'ocean_proximity_NEAR OCEAN' (0.065615). This shows that the distance from the coast and the median income level of the area greatly influence house prices.

### Conclusion

With these results, the developed model can help real estate companies in California to:
- Determine property prices more accurately
- Reduce the risk of incorrect pricing
- Improve operational efficiency and company profitability

## Recommendation

### Additional Feature Engineering

Create additional features based on domain analysis, such as:
- Distance to public facilities (schools, hospitals, shopping centers)
- Crime rates in the surrounding area
- School ratings

This external data can provide useful additional information.

### Exploration of Other Algorithms

Consider exploring more machine learning algorithms such as:
- **LightGBM**
- **CatBoost**

These algorithms often offer better performance or faster training compared to XGBoost and Random Forest.

### Data Update

- **Use of Recent Data**: The data used comes from the 1990 census. It is highly recommended to update the data with the latest census data or current real estate data. The conditions of the property market, demographics, and economic factors have changed significantly since 1990, so using recent data will yield a more relevant and accurate model.
