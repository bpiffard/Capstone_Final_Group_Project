# Capstone_Final_Group_Project
***
# Segment 2
## ✓ Description of preliminary dataprep processing 
- For segment 2 I'm using aggregate functions to preprocess the data, exploring what variables can be grouped together to reduce the number of rows in the dataset. I will see if this has any effect on my machine learning models

## ✓ Description of preliminary feature engineering and preliminary feature selection, including their decision-making process 
- Features have been categorized by Product, Store, Promotion, Customer & Location. These will be analyzed seperately as well as in various combination to see what variables best predict media promotion cost as well as other Target Variables- such as customer demographic data.

## ✓ Description of how data was split into training and testing sets 
- Data has been split using sklearn's train_test_split function

## ✓ Explanation of model choice, including limitations and benefits
- I am using RandomRorestRegression to investigate promotion cost and store sales. this has the benefit of being able to produce predictions based on continuois (non-categorical) data. RandomForestClassifier and LinearRegression Models are used when the data is categorical. 
  - PCA & Kmeans will be further investigated with aggregated date. Initial attempts were unsuccessful at producing clusters



***
# Segment 1
## ML Combined:
### In ML Combined there are 2 datasets:
- Customer data
- Store Data

***
### Customer Attributes
- **Can the cost of a sales promotion be predicted by customer demographic data?**
  - Modeled with Multiple Linear regression
    - Result: Low Accuracy
  - Modeled with Random Rorest Regression 
    - Regression evaluated by Root Means Square Error (RMSE)
    
- **Can total store sales be predicted by customer demographic data?**
  - Modeled with Multiple Linear regression
    - Result: Low Accuracy
    
- **Can a customer's member card category (normal, bronze, golden, etc) be predicted by their demographic data?**
  - Modeled with a deep neural network.
    
- **(Heatmap) What correlations exist between individual features in customer demographical data?**

### Store Attributes
- **Can total store sales be predicted by store attributes (store square feet, salad bar, coffe bar, etc.)?**

- **(Heatmap) What correlations exist between individual features in store demographical data?**

