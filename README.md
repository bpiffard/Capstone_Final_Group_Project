
# Capstone_Final_Group_Project
## Overview

- This project collected a demographic information of customer data as well as store, product, and promotion data. SQL database was used to store and query the data. Raw data was divdided into multiple tables and integrated according to column properties. To discover customer segment distributions, the factors of media cost and store sales, Tableau public was used to analyze and visualize the results. On the other hand, random forest classification, deep learning, random forest regressor and multiple linear regression model were applied to explore the correlation between member card, occupation, cost, store sales and other features, and make predictions. Finally, a webpage library was built to summarize and display our team work.
- Having tested several models, RandomForest Classifier & RandomForest Regression proved  the best performers for our dataset
- We explored grouping & aggregating  variables in our ML models to positive effect
- KMeans was not viable. Our dataset refused to cluster

## Data Source
- 

## Tools
- 


## Results 
### Webpage Overview
Check out our webpage here: https://foodmart-app.herokuapp.com/

![Screen Shot 2022-10-26 at 8 57 59 PM](https://user-images.githubusercontent.com/105877888/198187933-bb480342-e652-44e2-a57f-c01362aeab78.png)

### 


# Segment 2

# :star:Google Sildes for presentation in attched in main branch.                                                       
Food Mart Week 2 Slides .pptx [link](https://docs.google.com/presentation/d/1UI_9pxgMfpl1RURKctoKzbRbYXUVpgZSbE6YeuhFWNs/edit#slide=id.g16f1dbc7249_5_0)

# Segment 1


![foodmart icon](https://user-images.githubusercontent.com/105877888/194212188-13bd50bd-f078-464c-8bbe-8e88598a0667.jpeg)

## Team communication protocols
- Green Group Channel in Slack
- Zoom meetings – time will be scheduled as needed
- Class time
-  Shared phone numbers for emergencies

## Branches
-	celine
-	Stella-Branch
-	gm_branch
-	calos_branch
-	berns_branch
-	Hilda_branch

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


## Schema

### Data Preprocessing
  - Filter country with USA
  - Change column names
  - One-Hot Encoding and Label Encoding

###  Feature Extraction / Demension reduction
  - Heatmap:
    - customer feature correlation
    - store feature correlation 
    
  - PCA(principal component analysis)
    - Sample Clusters 
    - Scree Plot 
    - Feature Vector 
    - Recast the data along PCs. 

  - Possible group factors 
    - customer segment based on member card status
    - product segments:'gross_weight','net_weight', 'recyclable_package', 'low_fat', 'units_per_case',
    - store segments:'store_sqft', 'grocery_sqft','frozen_sqft', 'meat_sqft', 'store_city', 'store_state', 'store_sales(in millions)', 'store_cost(in millions)','unit_sales(in millions)'
  
### Machine Learning
- **Random Forest Regressor Model** 
  - target variable: `cost`
  - feature variables: customer demographic data
- **Multiple Linear Regression Model** 
  - target variable: `cost`, `store sales`
  - feature variables: customer demographic data, store data
- **Random Forest Classification Model**
  - target variable: `member card`
  - feature variables: customer demographic data
- **Deep Learning** 
  - target variable: `member card`
  - feature variables: customer demographic data
- **Random Forest Multi-Label Classifier**  
  - target variable: `promotion_name`, `food_category`, and `gender`
  - feature variables: several attempts of customer demographic data
- **KMeans Clustering**
  - feature variables: customer demographic data


### Database: SQL 
  - create multiple tables and build ERD.
  - do queries and visualize in Tableau
  
### Visualization: 
  - Tableau: bar chart, line chart, pie chart, 
  - Javascript and flask: add table to HTML and add filters. ---refer to UFOs
  - Dashboard: 
    - add drop down menu and bar chart to display media campaign result for each food category. --- refer to Belly button biodiversity
    - add pie chart for food category, food department, food family; store-type, gender, total-children, education, yearly income, member card....
    - add bubble chart for food category vs promotion, bubble size-unit sales. 


# Results and Insights:
1.  The Cost of a Sales Promotion’s is strongly linked to customer demographics
2.  Membership card Tiers are strongly linked with customer demographics as well
3.  There’s no relationship between different promotions (ie: Bag Stuffers, You Save Days, etc) and the type of product sold. 
4.  Store characteristics such  (square feet, store cost, coffee bar, etc.) were strong predictors of store sales
5.  A promotion’s media type could not be predicted using customer demographics
6.  Data was used to predict Media Cost; the dashboard represents the cost of media for a Food Marts in 3 states.  Also, the cost of media on its different categories.  Visualizations will be updated as per our findings and to answer all our questions.

