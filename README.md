# Capstone_Final_Group_Project
## SQL Status
THe .txt file contains query script to create tables for an SQL database that can house the csv files created by the SQL_Prep.ipynb. Twp separate datasets have been created, the one for mainly data on customers, and one for mainly data on the stores.
## Results of Initial Analysis
I created a Random Forest Classifier capable of multi-label classification with sklearn. There are two notebooks, one for the stopre_data and one for the customer_data. Feel free to download the notebook and test predicting different variables. All you need to do is alter cell 5. Replace the named column with whatever it is you want to test. 

X = X.drop(*variable you want to predict*, axis=1) <br>
y = prepped_df[*variable you want to predict*].values

I created the model to see how well the store data could be used to predict the different promotions used. The model did an abysmally poor job.

*Results for 'promotion_name'* <br>
Label Powerset F1-score: 0.013
Label Powerset Hamming Loss: 0.987

It also did not work well to predict the food category.

*Results for 'food_category'* <br>
Label Powerset F1-score: 0.059 <br>
Label Powerset Hamming Loss: 0.941

As for the customer_data.csv, I had a little more success. Here is average yearly income:

*Results for 'avg_yearly_income'* <br>
Label Powerset F1-score: 0.266 <br>
Label Powerset Hamming Loss: 0.734

I finally had some success when predicting the num,ber of children at home. All this really tells us though, is that demographic data can help predict other demographic data:

*Results for 'num_children_at_home'* <br>
Label Powerset F1-score: 0.775 <br>
Label Powerset Hamming Loss: 0.225

The model also predicted which member card each customer had fairly well.

*Results for 'member_card'* <br>
Label Powerset F1-score: 0.666 <br>
Label Powerset Hamming Loss: 0.334

Knowing how well the model can predict certain variables is really just to help make an educated guess as to which variables are meaningfully impoacted by the others. If it's predicted fairly well, perhaps that means there's an interesting correlation somewhere. The model fails to give us a view as to which of the variables are relevant, that will take more exploration. However, this model can help us determine what variables are worth exploring further.
