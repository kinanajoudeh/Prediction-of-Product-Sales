# Prediction of Product Sales

## Sales prediction for food items at various stores
Kenana Jouda

## Introduction
This project aims to predict product sales using a dataset containing information about products, outlets, and sales.

## Data Source
Big Mart Sales Prediction Data
https://datahack.analyticsvidhya.com/contest/practice-problem-big-mart-sales-iii/

## Data Dictionary
<img width="674" alt="Data Dictionary" src="https://github.com/user-attachments/assets/565e05a7-9c10-4920-8e2a-993da5aa4dff">

## Data cleaning
  Some data inconsistencies were found and handled in the Item_Fat_Content column.

## Data Analysis

### Exploratory Data Analysis
  - Dataset Overview: The dataset contains 8,523 rows and 12 features, combining numerical and categorical variables.
  - Each row represents the data of a specific item in a specific outlet.
  - The target variable is the Sale Price of an item in an outlet.

#### Some highlighted insights explored from the data:
  1. The distribution of Item Outlet Sale Prices shows clear segmentation, indicating the presence of four distinct price ranges for the sold goods.
    - Low Priced Items:
      With prices less than 70.
    - Medium Priced Items:
      With prices between 70 and 135.
    - High Priced Items:
      With prices between 135 and 205.
    - Very High Priced Items:
      With prices greater than 205.

  - Most of the items have medium or high prices:
    2751 medium-priced items
    3003 high-priced items
  - Fewer items have low and very high prices:
    1341 low-priced items
    1428 high-priced items

  The maximum retail price for items strongly affects the total items outlet sales. When the price increases,
  the total item outlet sales are expected to increase.
    
  Very high-priced items, even though they are a smaller set than other groups like the medium and
  high price items, and have achieved the maximum average of sales across all  groups. 
  
  That could be due to multiple possible reasons, maybe some expensive items are heavily marketed or backed by
  strong a brand, making them more desirable. Or maybe the fact that higher prices often imply better quality.

  High-priced items achieved the highest total sales among all groups. However, very high-priced items may not
  have performed as well, possibly due to their extreme prices reaching up to 13,000, which could make them
  less accessible to a broader customer base.
 
  <img width="586" alt="Screenshot 2024-09-19 at 11 56 14 AM" src="https://github.com/user-attachments/assets/00ac6129-07d4-4b99-b758-c9a39a368098">

  <img width="586" alt="Screenshot 2024-09-19 at 11 56 14 AM" src="https://github.com/user-attachments/assets/23f2caf1-ddce-489f-9331-8404e762ca29">
 

  2. The top 4 item types that have achieved the most total sales were:
      - Fruits and vegetables
      - Snack Foods
      - House Hold
      - Frozen Foods
   
<img width="614" alt="Screenshot 2024-09-19 at 11 48 05 AM" src="https://github.com/user-attachments/assets/359f70db-c78f-489e-9ebd-4842cdce51d7">


### Explanatory Data Analysis
Features were separated into 3 categories:
  - Categorical
  - Ordinal
  - Numeric

For each feature:
  - A univariate plot was explained.
  - A multivariate plot with the target was explored

## Model
  2 types of models were tested. A Linear Regression model and a Random Forest model(2 default and tuned versions).
  Here are the model metrics on training and testing data
  - For training data:
    - According to the MAE the model is off by average 692.4 dollars.
    - According to the RMSE the model is off by average 984.2 dollars.
    - The model covers 67.3% of the data variation.
  - For testing data:
    - According to the MAE the model is off by average 729.0 dollars.
    - According to the RMSE the model is off by average 1,046.9 dollars.
    - The model covers 60.3% of the data variation.
   
  Let us compare the performance of the models against the testing data:

  - Tuned Random Forest vs. Default Random Forest:
  
    The tuned Random Forest model shows improvements in the test R^2 and reduced overfitting compared to the
    default Random Forest. This indicates that the tuning process helped improve the model performance and it
    generalizes better on unseen data.
  
  - Tuned Random Forest vs. Linear Regression:
  
    The tuned Random Forest model performs better on both training and test data, as evidenced by lower errors
    (MAE, RMSE) and higher R2


  - In conclusion: 
    - **Good Predictive Power:** The model is fairly accurate, explaining around 60-67% of the price differences.
    This means it can reliably predict item outlet prices with an average error of around $700-$1,000 per
    item. This level of prediction is valuable for making pricing decisions, helping the business stay
    competitive while ensuring that prices are aligned with market expectations.
    
    - **Real-World Application:** In real-world terms, the model provides a useful guide for setting prices across
    different outlets. However, it’s important to understand that it doesn’t predict prices perfectly and could
    still make some errors, which should be kept in mind when using the model’s predictions for critical
    business decisions.
    
    - **Room for Improvement:** While the model is performing well, there's still potential to improve its
    accuracy, particularly in how it handles new, unseen data. Further refinements or adjustments to the model
    could reduce the errors in price predictions and improve its performance.



## Recommendations

- Use as a Tool for Price Strategy: The model can serve as a strong tool for understanding pricing trends and making informed decisions. It can assist in setting competitive outlet prices, balancing between maximizing revenue and remaining attractive to customers.

- Monitor and Refine: Although the model is effective, it’s important to continuously monitor its performance and make improvements over time. Further adjustments to the model could help reduce prediction errors, especially when dealing with new data or market conditions.

## Stakeholder Recommendations

1. **Focus on High-Value Products for Maximum Revenue Potential**
   Higher-priced items contribute significantly to total sales despite being fewer in quantity.
   Invest in promoting high-value products, especially those with strong brand recognition or perceived high quality.
   Ensure the availability of premium items in key locations where demand is higher.
   Highlight quality and brand advantages through targeted marketing campaigns.
   
2. **Address Accessibility of Very High-Priced Items**
  Very high-priced items achieve high average sales but may struggle with total sales due to limited accessibility.
  Introduce financing options or promotional discounts to make these items more accessible to a broader audience.
  Identify niche markets or premium segments where such products can be marketed effectively.
  Use customer feedback to refine the pricing or value proposition of these items.


## Limitations and Next Steps

  - The model’s accuracy could be improved by making adjustments to reduce prediction errors. For example, by incorporating more features or data points related to pricing trends.
  
  - In future iterations, we could explore additional data sources or advanced techniques to increase the model's predictive power and reduce errors.




  
