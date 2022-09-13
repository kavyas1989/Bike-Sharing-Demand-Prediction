# Bike-Sharing-Demand-Prediction

# Problem Description 
Public rental bike sharing system has been gaining popularity in the recent times.Currently,this system has been introduced in many major cities for enhancement of mobility comfort.It is also a great step towards environmental sustainability and social welfare.
In order to run this system successfully,it is important to ensure that the rental bikes are available and accessible to the public at the right time,since this reduces the waiting time.Providing the city with a stable supply of rental bikes could become a serious challenge,eventually.Forecasting the number of bikes required at each hour can greatly help in ensuring that there's a stable supply of rental bikes.
Our objective here,is to predict the Count of Rental bikes required on an hourly basis and to also identify the features which influences the hourly demand for Rental bikes

# Data Description 

- Date : year-month-day
- Hour : Hour of the day (24hr fomat)
- Temperature : Temperature in Celsius
- Humidity : Percentage of humidity
- Windspeed : windspeed in m/s
- Visibility : visibility of 10m
- Dew point temperature : In Celsius
- Solar radiation : In units of MJ/m2
- Rainfall : Amount of rainfall for each day in units of mm
- Snowfall : Amount of snowfall for each day in units of cm
- Seasons : Winter, Spring, Summer, Autumn
- Holiday : Holiday/No holiday
- Functional Day : Yes/No
- Rented Bike count : Count of bikes rented at each hour (Dependent variable)

- Total number of rows in data : 8760
- Total number of columns : 14

# Data Cleaning and Feature Engineering
### (1) Removing Duplicate Rows
- No duplicate rows were present in dataset.

### Hanlding Null Values
- No null values present in the Dataset 

### Converting columns to appropriate data types
- Changed datatype of Date to date type.

### Creating New Columns 
- Created new column for month from date column.
- Created new column for day of mweek from date column.

### Feature Encoding 
- did one hot encoding to convert numerical into categorical columns for better analysis

# Extrapolarotary Data Analysis

To gain insights from the data. We plot various charts like bar graph, histogram, heat map, line graph etc. for univariate and bivariate analysis. This process helped us figuring out various aspects and relationships among the dependent and the independent variables.
Observation of our EDA as follows:

- Peak demand of bike sharing was observed during summer and lowest in Winter season
- Our peak commuting hours was 7 A.M. - 9 A.M. in morning and 5 P.M. - 7 P.M. in evening
- Our bike sharing demand was higher during weekend than weekdays.
- On holidays demand of bike sharing was lower than non-holidays
- Dew point temerature and temperature found to be highly correlated.

# Model Building 

As we have to predict the count of rented bikes in our problem, so this is a regression problem. Based on the problem statement which is basically to predict the demand of rented bikes for each hour, so I have decided to develop predictive models using following algorithms and then compared ther performance to use most appropriate model .

- Linear Regression
- Ridge and Lasso regression
- Decision Tree Regressor
- Random Forest Regreesor
- Gradient Boosting
- Elastic Net

# Evaluation Metrics 

To evaluate the models we used MAE(Mean Absolute Error) and Adjusted R2 score 
and we need to use the fact that smaller the value of MSE is and higher the value of Adjusted R2 score better our model is .

calculating MSE and Adjusted R2-score for all regression algorithms :
- Linear regression : MAE = 4.53 , Adjusted R2 score : 0.77
- Ridge : MSE = 4.53 , Adjusted R2 score : 0.79
- Lasso : MSE = 4.69 , Adjusted R2 score : 0.79
- Decision Tree : MSE  = 3.88 , Adjusted R2 score : 0.79 
- Random Forest Regression : MSE = 3.22 , Adjusted R2 score : 0.89 
- Gradient Boosting : MSE = 2.36 , Adjusted R2 score : 0.94

# Conclusion 

As we have observed that we are getting our least value of MAE and highest value of Adjutsed R2 score by using Random Forest and Gradient Boosting.
So we can use either of these 2 algorithms for model building  . 
                      

