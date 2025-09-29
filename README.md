# Bangalore-Housing-Price-ML
In order to predict the cost of houses in Bangalore, I created a machine learning model that predicts the prices with an accuracy of 93%.

#### Background:
Buying or renting a house in the silicon valley of India is like a dream come true. But what should be my budget? What should be the price range I can expect in order to get the house of my dreams these are the kind of questions people usually tend to ask. This ML model helps answer all of the questions based on a few input criteria. Whether a person wants to rent a house or buy one, whether you want to stay at a PG or a hostel, this model helps you to get an idea of the price of all of these residence options.

This helps a person create a budget or get the loan accordingly. People can also use it to have a general idea of the existing market rates and invest in real estate accordingly. This model is helpful espically for students as a large number of them come from different parts of the country to study at some of the best institutions here. Such students are generally looking for a PG or hostel and having an idea of how much they would be required to spend on allocation helps budget their expenses. This model helps people have an estimate owing to which they make a financially sound decisions on how much to save or what amount of loan to take.

Buying a home, especially in a city like Bengaluru, is a tricky choice. While the major factors are usually the same for all metros, there are others to be considered for the Silicon Valley of India. With its help millennial crowd, vibrant culture, great climate and a slew of job opportunities, it is difficult to ascertain the price of a house in Bengaluru.

#### Problem Statement:
Most people do not have an idea of the price that they have to pay in order to buy or rent the house as a result of which they are unable to save or invest enough to get themselves or their family a house of their own.

#### Objective: 
To have an estimate of the house price whether for renting or buying.

#### Assumptions:
1. The buyer already has an idea about the location they are willing to buy the house.
2. They know the BHK, bath and balcony	they want in their house.
3. The buyer only want to know the estimated price of the house.

#### Short comings:
1. People only get to know the estimated price based on the location and not the actual value.
2. A buyer should have an idea about the area/location they want to buy/rent the house in.

#### About the model:

The buyer (a person who wants to know the estimate of the price of the house in Bangalore) just needs to provide the following given inputs:<br>
location	<br>
size_BHK	<br>
total_sqft	<br>
bath	<br>
balcony	<br>
and the model can predict with 93% accuracy the price of houses based on the buyer input. This also provides them with a pre-existing idea of the price range they can expect in order to get there dream house in their dream location. 

#### Approach:

1. The datset is downloaded from kaggle in the csv format and imported it in the jupter file along with all the other necessary libraries.

2. Tackling null values:
   The next obivious was to look for null values. Since all of the columns in the dataset consisted of columns with less than 5% null values, the most obvious and useful step was to remove those null values.

3. An overview of the outliers:
   There was a lot of outliers in the dataset. This is very obvious owing to the fact that the dataset consisted of both renting and buying prices of the property. The price of renting is a lot less then the         price of buying a property. Additionally, a number of factors namely location, BHK, balcony, neighbourhood affect the prices of the property. Thus, we need to work with outliers. Outliers cannot be eliminated     during the creation of this model.

4. Feature Engineering:
   Feature Engineering is the most important step in model making as it accelerates or deaccelerates the accuracy of the model. In this step new columns are           created while existing columns can be removed. <br>
&nbsp;&nbsp;&nbsp;&nbsp;i. Feature Removal:<br>
&nbsp;&nbsp;&nbsp;&nbsp;In this step, addition features were created and unnecessay features were removed. A correlation metrics revealed that columns like availabilty and society are     not imparting much to the creation of the model. A person might know the location they want to get the house in but not really the society, they would just want    to explore all of the houses in the area/location. Similarly, questions like avalibilty are not really something potential buyer/renters tend to ask. Therefore,    it was a wise decision to remove these columns from the dataset.<br>
   
&nbsp;&nbsp;&nbsp;&nbsp;ii. Feature Construction:<br>
&nbsp;&nbsp;&nbsp;&nbsp;Additional features were created like total price (price * total_sq_feet_area).<br>

&nbsp;&nbsp;&nbsp;&nbsp;iii. Encoding:<br>
&nbsp;&nbsp;&nbsp;&nbsp;As machine learning models only take numerical values but columns like location are categorial. Hence Label Encodin was performed to change them into numerical column.<br>

&nbsp;&nbsp;&nbsp;&nbsp;iv. Scaling:<br>
&nbsp;&nbsp;&nbsp;&nbsp;Scaling was performed to benefit standarization. This helps bring all the values in the range of 0-1 while keeping the distribution and distance intact.<br>

&nbsp;&nbsp;&nbsp;&nbsp;5. Model creation and cross validation:<br>
&nbsp;&nbsp;&nbsp;&nbsp;Multiple models were trained namely<br>
    Linear Regression<br>
    Ridge Regression<br>
    Lasso Regression<br>
    Elastic Net<br>
    Decision Tree<br>
    Random Forest<br>
    Gradient Boosting<br>
&nbsp;&nbsp;&nbsp;&nbsp;Upon cross validating the GradientBoostingRegressor provided the highest accuracy score of 93% turning out to be the best model among the ones used.<br>

#### Final Verdict:
A house price is determined by a number of factors a few of which are covered in dataset based on which the model is created. The model is able to predict the price with an accuracy of 93%. It is an extremely useful model for any person who is buying/renting the house and wants an estimation of the budget to be allocated.


 
