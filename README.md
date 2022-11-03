# Capstone_Final_Group_Project

# Final Segment

### data preprocessing 
- In preprocessing we elected to Use LabelEncoder for the majority of our models to limit expansion of our dataset. Alternate encoders, such as get_dummies and OneHotEncoder, would have resulted in a combined dataset of over 300 potential features. Additionally we experimented with grouping and aggregating the data to positive effect. For example- grouping by physical store characteristic columns such as store square footage to identify distinct stores and then aggregating certain metrics of those stores to find average promotion costs and average store sales.

### Feature engineering & selection 
- features were categorized by Product, Store, Promotion, Customer & Location. Several of these categories were analyzed individually as well as in combination to investigate feature importance by different categories. Questions such as:
  - Can customer demographics predict Membership Card Tier?
  - What Store features are most important for predicting store sales?
  - Do different stores prefer certain Promotions (promotion_name)?
  - Can the cost of a saLes promotion be predicted by customer demographic features?

### Description of how data was split into training and testing sets 
  - using sklearn's train_test_split function, the data was split at 75% training data and 25% test data.

### Explanation of model choice, including limitations and benefits 
- Final ML models were RandomForestClassifier, RandomForestRegressor, & LinearRegression. When RandomForestClassifier & LinearRegression were not viable,  RandomForestRegression was very useful for evaluation of continuous variables. 

### Explanation of changes in model choice (if changes occurred between the Segment 2 and Segment 3 deliverables) 
- Our Deep learning Nearal Network was dropped in favor of RandomForestClassifier which outperformed the Neural network in terms of accuracy and was quicker to execute.

### How was the model was trained or retrained
- RandomForestClassifier models were retrained by increasing the quantity of decision trees which had a positive effect on accuracy & RMSE scores.

### Description and explanation of model’s confusion matrix, including final accuracy score 
- RandomForestClassifier modeling across all membership card types (Gold, Silver, Bronze, and Normal) was 94%. As displayed by the following Confusion Matrix, recall was lowest for the Silver Card category. This may be explained by the relatively small size of the Silver Card cohort, compared to the other Membership Card categories.
![Screen Shot 2022-11-02 at 10 12 33 PM](https://user-images.githubusercontent.com/105818879/199651833-e4d2e7f1-8456-4fd2-b6bc-2d6938bf3cc7.png)

![Screen Shot 2022-11-02 at 10 14 42 PM](https://user-images.githubusercontent.com/105818879/199652021-b79716a8-26b5-4aa7-96c9-db755076c8d3.png)

- Using RandomForestRegressor to analyze Agrocery store's profits based on the stores physical attributes retured a Root Means Square Error of 0.223 indicating that store features have strong predective value when analysing revenue.
![Screen Shot 2022-11-02 at 10 21 04 PM](https://user-images.githubusercontent.com/105818879/199652576-52f2a888-fd9e-4918-b703-9eca6caedfbc.png)

- It was also observed that the geographical location of these stores was an important feature for predicting the Cost of a sales promotion.
  - *With* City & State
  ![Screen Shot 2022-11-02 at 10 26 17 PM](https://user-images.githubusercontent.com/105818879/199653013-90208135-94d1-40e2-8aa7-c9979a5c329d.png)

  - *Without* City & State
  ![Screen Shot 2022-11-02 at 10 27 19 PM](https://user-images.githubusercontent.com/105818879/199653128-f351653c-9262-476c-95fb-a8afc2ee1bea.png)



***
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

