

# Capstone_Final_Group_Project

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
- **Random Forest Regression Model** 
  - target variable: `cost`
  - feature variables: customer demographic data
- **Multiple Linear Regression Model** 
  - target variable: `cost`, `store sales`
  - feature variables: customer demographic data, store data
- **Random Forest Classification Model**
  - target variable: `member card`
  - feature variables: customer demographic data
- **Deep Neuron Network** 
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
  - Tableau: bar chart, line chart, pie chart, map
  - Javascript and flask: add table to HTML and add filters. ---refer to UFOs
  - Dashboard: 
    - add drop down menu and bar chart to display media campaign result for each food category. --- refer to Belly button biodiversity
    - add pie chart for food category, food department, food family; store-type, gender, total-children, education, yearly income, member card....
    - add bubble chart for food category vs promotion, bubble size-unit sales. 
   
