
# Capstone_Final_Group_Project
## Overview

- This project collected a demographic information of customer data as well as store, product, and promotion data. SQL database was used to store and query the data. Raw data was divdided into multiple tables and integrated according to column properties. To discover customer segment distributions, the factors of media cost and store sales, Tableau public was used to analyze and visualize the results. On the other hand, random forest classification, deep learning, random forest regressor and multiple linear regression model were applied to explore the correlation between member card, occupation, cost, store sales and other features, and make predictions. Finally, a webpage library was built to summarize and display our team work.
- Having tested several models, RandomForest Classifier & RandomForest Regression proved  the best performers for our dataset
- We explored grouping & aggregating  variables in our ML models to positive effect
- KMeans was not viable. Our dataset refused to cluster

## Data Source

Why we choose this data source and what we were expecting to get out it?

Cost Prediction sounded interested since we are looking for a data source related to accounting (profit, revenue, overhead, marketing cost, how to attract new customers to increase sales).  The description of this data source “Predict cost on Media campaigns in food Mart of USA” sounded very instated and had the characteristics we were looking for.
After reviewing the contents of the data source, here are some of the questions we wanted to answer by the data source:

-	How many stores there are?
-	In which cities and states these stores are? 
-	Do costumer demographics link to membership card tiers?
-	Is the cost of sales promotions linked to customers demographics?
-	What is media cost, by state, by store type, by food department?
-	Which are top media promotions, the top unit of sales?
-	What are the sales, by department, store, food category?
 

## Tools
- 


## Results 

### Machine Learning



### Webpage Overview
Check out our webpage here: https://foodmart-app.herokuapp.com/

![Screen Shot 2022-10-26 at 8 57 59 PM](https://user-images.githubusercontent.com/105877888/198187933-bb480342-e652-44e2-a57f-c01362aeab78.png)

### Tableau Visualization and results 

#### Customer Demographics




#### Food Mart Media Cost, Promotions and Sales

https://public.tableau.com/app/profile/hilda.vazqez/viz/FoodMartMediaCostPromotionsandSales/Story1
-	Media cost by Store Type:

Supermarkets are the costliest but also where more customers shop and in consequence the highest on sales.

![image](https://user-images.githubusercontent.com/105381777/198899776-652e54a3-f0f6-47f1-be35-2f667e9adfe1.png)


-	Promotions Cost by Store Type

There are 49 different types of promotions but in general the costliest in total for all Store Types is the Weekend Markdown.  However, this varies by store type:

    . Supermarket – Weekend Markdown with a total cost of $160,008    
    . Deluxe Supermarket - Price Savers with a total cost of $101,706    
    . Gourmet Supermarket – Tow Day Sale with a total cost of $62,223    
    . Small Grocery – Sales Galore with a total cost of $7,774
    
![image](https://user-images.githubusercontent.com/105381777/198899802-bed8f70c-cd87-4f7a-b12d-1c3bd2bbafae.png)

-	Top Promotions based on Sales

  The cost or promotion will not determine the sales results; however Weekend Markdown has the highest sales in total for all Stores Types 
  
    . Supermarket – Weekend Markdown with a store total sale of $11,000,000
    . Deluxe Supermarket – Cash Register Lottery with a store total sale of $10,000,000
    . Gourmet Supermarket – Two Day Sale with a store total sale of $3,000,000
    . Small Grocery – Two Day Sale with a store total sale of $510,000

![image](https://user-images.githubusercontent.com/105381777/198900444-13e83742-6387-40f2-8b6d-b3544f2661ee.png)

-	Media Cost and Total Sales by Food Department

  Produce is the one with the highest cost of media but also Produce is the one with the highest sales 
  
    . Produce cost of media $535, 956
    . Produce total sale $36, 516,000

![image](https://user-images.githubusercontent.com/105381777/198901382-266a97a2-edf5-4bcf-adbc-90fbcc936e38.png)

-	Sales by Media Type

“Daily paper, radio” has the highest sales, followed by “Daily Paper". Media type could be more cost efficient combined then buying it individually with still good sales results.

    . "Daily paper,radio" total sales $32,669,000

![image](https://user-images.githubusercontent.com/105381777/198901686-afa97a1e-e265-4f02-ac8a-a09715a1de44.png)

- Sales by City and State

This data set is presenting Food Mart metrics in the stat of Washington, Oregon, and California.  Here are the total sales for each city and state:

      . WA 



