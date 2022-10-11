# Capstone_Final_Group_Project

![foodmart icon](https://user-images.githubusercontent.com/105877888/194212188-13bd50bd-f078-464c-8bbe-8e88598a0667.jpeg)

## Data Source:
- **Cost Prediction on acquiring Customers**
- https://www.kaggle.com/datasets/ramjasmaurya/medias-cost-prediction-in-foodmart

  ```
  PREDICT COST ON MEDIA CAMPAIGNS IN FOOD MART OF USA .

  ON THE BASIS OF 60K CUSTOMERS INCOME ,PRODUCT,PROMOTION AND STORE FEATURES.

  ABOUT FOODMART:

  Food Mart (CFM) is a chain of convenience stores in the United States. The private company's headquarters are located in Mentor, Ohio, and there are currently approximately 325 stores located in the US. Convenient Food Mart operates on the franchise system.

  Food Mart was the nation's third-largest chain of convenience stores as of 1988.

  The NASDAQ exchange dropped Convenient Food Mart the same year when the company failed to meet financial reporting requirements.

  Carden & Cherry advertised Convenient Food Mart with the Ernest character in the 1980s.

  …KNOW MORE FROM WIKI .
  ```

## Terms: 
[media campaign](https://dictionary.cambridge.org/dictionary/english/media-campaign)
```
media campaign: 
noun [ C ]   MARKETING, COMMUNICATIONS
a planned series of newspaper articles, television interviews, etc. that are intended to achieve a particular aim:
eg1: a media campaign against sth---- The government has launched a national media campaign against smoking.
eg2: a media campaign to do sth---- The president won the election despite a concerted media campaign to discredit him.
```

[One-Hot Enconding vs. Label Encoding](https://www.analyticsvidhya.com/blog/2020/03/one-hot-encoding-vs-label-encoding-using-scikit-learn/)
- Label Encoding
  - each label is assigned a unique integer based on **alphabetical ordering**.
  - is a process of converting categories to numbers.
- One-Hot Encoding 
  - simply creates **additional features** based on the number of unique values in the categorical feature. 
  - every unique value in the category will be added as a feature.
  - is the process of creating dummy variables.
  - Drawback: The Dummy Variable Trap leads to the problem known as multicollinearity. Multicollinearity is a serious issue in machine learning models like Linear Regression and Logistic Regression.

- We apply One-Hot Encoding when:
  - The categorical feature is not ordinal (like the countries above)
  - The number of categorical features is less so one-hot encoding can be effectively applied
- We apply Label Encoding when:
  - The categorical feature is ordinal (like Jr. kg, Sr. kg, Primary school, high school)
  - The number of categories is quite large as one-hot encoding can lead to high memory consumption

[oneHotEncoder vs. get_dummies](https://pythonsimplified.com/difference-between-onehotencoder-and-get_dummies/)
- The get_dummies can’t handle the unknown category during the transformation natively. You have to apply some techniques to handle it. But it is not efficient. On the other hand, OneHotEncoder will natively handle unknown categories. All you need to do is set the parameter handle_unknown='ignore' to OneHotEncoder.
- If you want to put your machine learning model into production, Scikit-learn Pipeline will be very useful. But, get_dummies is not compatible with the Scikit-learn pipeline. It requires you to create your own transformer. On the other hand, OneHotEncoder is compatible with the Scikit-learn pipeline.

[StandardScaler, MinMaxScaler and RobustScaler](https://www.geeksforgeeks.org/standardscaler-minmaxscaler-and-robustscaler-techniques-ml/)(https://stackoverflow.com/questions/51237635/difference-between-standard-scaler-and-minmaxscaler)

- MinMaxScaler
  -(feature_range = (0, 1)) will transform each value in the column proportionally within the range [0,1]. Use this as the first scaler choice to transform a feature, as it will preserve the shape of the dataset (no distortion).
- StandardScaler
  - will transform each value in the column to range about the mean 0 and standard deviation 1, ie, each value will be normalised by subtracting the mean and dividing by standard deviation. Use StandardScaler if you know the data distribution is normal.
- RobustScaler
  - If there are outliers, use RobustScaler(). Alternatively you could remove the outliers and use either of the above 2 scalers (choice depends on whether data is normally distributed)
**Note**:  If scaler is used before train_test_split, data leakage will happen. Do use scaler after train_test_split


### Possible questions:
1. Which kinds of people can be classified together? And which is the most effective media type for this clusters with same demographic traits?
2. Which kinds of products can be classified together? And which is the best promotion for this product group?
3. Among all features, What are the top 5 reasons affect the store sales? store size, product type, costumer's property?
4. Which kind of promotion is most cost-effective on different food category?



## Schema:

### Filter country with USA
### Standarlization

###  Feature Extraction / Demension reduction
- PCA: principal component analysis, variable reduction KMeans
  - Sample Clusters 
  - Scree Plot 
  - Feature Vector 
  - Recast the data along PCs. 
 
  **Possible group factors:** 
  - 1.demographic:'marital_status', 'gender', 'total_children', 'education','occupation', 'houseowner'
  - 2.products:'gross_weight','net_weight', 'recyclable_package', 'low_fat', 'units_per_case',
  - 3.store size:'store_sqft', 'grocery_sqft','frozen_sqft', 'meat_sqft' 
  - 4.location:'store_city', 'store_state'
  - 5.sales:'store_sales(in millions)', 'store_cost(in millions)','unit_sales(in millions)'

- Random Forest Model: classification and feature importance
- Neural Network: classification
- Multiple Linear Regression: features-cost or features-store sales ---> predictions


- SQL: 
  - create multiple tables and build ERD.
  - do queries and visualize in Tableau
- Tableau: pivot table visualization

- Javascript: add table to HTML and add filters. ---refer to UFOs
- Dashboard: 
  - add drop down menu and bar chart to display media campaign result for each food category. --- refer to Belly button biodiversity
  - add pie chart for food category, food department, food family; store-type, gender, total-children, education, yearly income, member card....
  - add bubble chart for food category vs promotion, bubble size-unit sales.
