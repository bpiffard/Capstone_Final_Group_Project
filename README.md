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

## Schema:
###  Feature Extraction / Demension reduction
- PCA: principal component analysis, variable reduction KMeans
  - Sample Clusters 
  - Scree Plot
- ??Exploratory Factor Analysis: Python or R
    combine the variables that are highly correlated with each other. 
 
    **Possible group factors:** 
    - 1.demographic:'marital_status', 'gender', 'total_children', 'education','occupation', 'houseowner'
    - 2.products:'gross_weight','net_weight', 'recyclable_package', 'low_fat', 'units_per_case',
    - 3.store size:'store_sqft', 'grocery_sqft','frozen_sqft', 'meat_sqft' 
    - 4.location:'store_city', 'store_state'
    - 5.sales:'store_sales(in millions)', 'store_cost(in millions)','unit_sales(in millions)'
  - correlation matrix
  - explained total variance, screeplot
    - % of variance
    - Accumulated %
  - communatlities, component matrix
  - rotated component matrix(varimax)
    to determine which trait be assigned to which factor and name it by researcher.


- Random Forest Model: classification and feature importance
