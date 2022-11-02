# Capstone_Final_Group_Project

# Segment 3
## ✓ Description of data preprocessing 
- For segment 2 I'm using aggregate functions to preprocess the data, exploring what variables can be grouped together to reduce the number of rows in the dataset. I will see if this has any effect on my machine learning models

## ✓ Description of feature engineering and the feature selection, including the team's decision-making process 
- Features have been categorized by Product, Store, Promotion, Customer & Location. We've analyzed these seperately as well as in various combination to see what variables best predict media promotion cost as well as other Target Variables- such as customer demographic data (ex occupation, income level, & education level).

## ✓ Description of how data was split into training and testing sets 
- Data has been split using sklearn's train_test_split function.

## ✓  Explanation of model choice, including limitations and benefits
- I am using RandomRorestRegression to investigate promotion cost and store sales. This has the benefit of being able to produce predictions based on continuois (non-categorical) data. RandomForestClassifier, Deep Learning Nearal Networks, and LinearRegression have also been evaluated for accuracy. Initial attempts were unsuccessful at producing clusters

## Explanation of changes in model choice (if changes occurred between the Segment 2 and Segment 3 deliverables)
- Some LinearRegrssion models did not fit certain features in our dataset, displaying an accuracy of 0.00. These have been dropped.

##  Description of how model was trained (or retrained, if they are using an existing model)
- Data was split at 75% training data and 25% test data.
- 

## ✓ Description and explanation of model’s confusion matrix, including final accuracy score



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

