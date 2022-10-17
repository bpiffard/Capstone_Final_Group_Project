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


- Database : SQL
  - create multiple tables and build ERD.
  - do queries and visualize in Tableau
  
- Visualization: Tableau


- Library: html webpage
  - about food mart: Visit Wikipedia
  - Data Source: Kaggle Dataset: media prediction and its cost.csv, 500 Dataset Sample
  - Database: SQL
  - Visualization: Tableau
  - Model: Machine Learning
  - About Us: Team Members
