# [Final Project] - Uyen Phuong
## Car Prices Predicting
![image](https://github.com/user-attachments/assets/b2d97bfc-9b5d-4e70-a0fa-df70e2fac0ff)
Pic credit: Volvo Australia


## About this project
This project seeks to analyze car price datasets to identify the features that influence car prices. Using these insights, we will develop a model to predict car prices based on the selected features.

## Data description
The datasets provide the information about different types of cars across the American market, data on vehicle features and prices of different car models.

## Data Source: Where Our Data Comes from 
Source: Public dataset from Kaggle (Car Price Prediction Multiple LinearRegression: https://www.kaggle.com/datasets/hellbuoy/car-price-prediction/data)

Structures: This datasets includes 26 columns and 205 rows.

**Car ID:** Unique identifier for each car model

**Symboling:** Insurance risk rating for the car

**Car name:** Name or model of the car

**Prices:** Price of the car

**Fuel type:** The type of fuel the car uses

**Aspiration:** Method of air intake for the engine (std or turbo)

**Door number:** Number of doors on the car 

**Car body:** Design or type of car body (sedan, hatchback, etc.)

**Drive wheel:** Type of drivetrain or wheels (FWD, RWD, 4WD)

**Engine location:** Engine location (front or rear)

**Wheel base:** Distance between front and rear axles

**Car length:** Length of the car

**Car width:** Width of the car

**Car height:** Height of the car

**Curb weight:** Weight of the car without passengers or cargo

**Engine type:** Type of engine (ohc, ohcv, etc.)

**Cylinder number:** Number of cylinders in the engine

**Engine size:** Size of the engine (in cc or ci)

**Fuel system:** Type of fuel injection system (mpfi, etc.)

**Bore ratio:** Ratio of cylinder bore diameter to stroke length

**Stroke:** Length of the engine stroke

**Compression ratio:** Engine compression ratio

**Horsepower:** Engine power output (in hp)

**Peak rpm:** Engine's peak RPM for generating power

**City mpg:** Fuel efficiency in city driving (mpg) 

**Highway mpg:** Fuel efficiency on the highway (mpg)

## Tools and Technologies Applied:

Python: Data analysis

Libraries:

•Pandas & Numpy: Data analysis.

•Matplotlib & Seaborn: Visualization, presentation.

•Scikit-learn: Building and evaluating machine learning models, such as Logistic Regression, Random Forest, Decision Tree, CatBoost and Gradient Boosting…

Techniques: Data cleaning, handling missing values, and correlation analysis, RFE, VIF.


## Purpose and Outcome:

Purpose: To determine the features of a car that affect its price and to create predictive models with high accuracy.

Outcome: A precise model for predicting car prices, along with features that affect those prices.


## EDA: 

### Car brand
![image](https://github.com/user-attachments/assets/19ce93f2-fb6c-47f4-8735-650969fbb161)

It can be seen that there is a difference in average price between car brands:
+ Top-notch car group: Jaguar, Buick, Porsche and BMW.
+ High-average car group: Volvo, Audi, Mercury, Alfa-Romero, Peugeot, Saab.
+ Affordable car group: Mazda, Nissan, Volkswagen,...

### Fueltype:
![image](https://github.com/user-attachments/assets/2861325b-05eb-4d3e-beaf-d63ac4816b09)

The chart indicates that there are many more vehicle models using gas as their fueltype compared to those using diesel.

Some gas-powered cars have very high prices, ranging from 30000$ to 45000$.

However, the average price of gas vehicles is lower than that of diesel vehicles.


### Aspiration: 
![image](https://github.com/user-attachments/assets/d4cd368a-9684-4a51-a44f-976d46be99c1)

STD aspiration has a significantly higher count compared to the Turbo type. This may suggest that std cars are more common than turbo cars.

There are also a few outliers in both categories, indicating that some cars have significantly higher.

The average price of "turbo" cars is higher than that of "std" cars.


### Doornumber:
![image](https://github.com/user-attachments/assets/6e85d984-29ed-42ba-a22a-4f55ca8a2620)

The number of four-door vehicle models is greater than that of two-door models, but the difference is not significant.

The two other charts show that there is not much difference in price between two-door and four-door vehicles.


### Carbody:
![image](https://github.com/user-attachments/assets/a23889c7-4765-4171-af52-c9a7c10ea603)

The "sedan" type has the highest count, followed by "hatchback," making these two the most common body types. "wagon," "hardtop," and "convertible" types have significantly lower counts.

"Convertible" and "hardtop" cars have a higher median price, with "hardtop" displaying the widest price range. "Hatchback" cars have the lowest median price, and they are generally cheaper than other body types.

The average price is highest for "hardtop" cars, followed by "convertible" cars. "Hatchback" cars have the lowest average price.

### Drivewheel: 
![image](https://github.com/user-attachments/assets/9138c349-1b5e-4927-96d0-057bdd7e08e9)

"FWD" is the most common drive wheel type, followed by "RWD". "4WD" is the least common.

"RWD" has the highest median price and the widest price range, suggesting that rear-wheel-drive vehicles tend to be more expensive.

The average price is highest for "RWD" vehicles, followed by "FWD," with "4WD" having the lowest average price.

### Enginetype: 
![image](https://github.com/user-attachments/assets/a1c67986-ef63-412c-b670-0a15cd22415e)

The majority of cars have the "ohc" engine type, which significantly outnumbers all other engine types. This shows that "ohc" engines are the most common in this dataset.

Engine type appears to correlate with price, with "dohcv" and "ohcv" engines indicating higher-value cars, while "ohc" engines are more common and generally more affordable.


### Fuelsystem: 
![image](https://github.com/user-attachments/assets/2ab68fd8-3317-4f49-8572-e9e310679565)

The "mpfi" fuel system is the most common, followed by "2bbl".

The box plot reveals that "mpfi" has the highest price range, with a considerable number of high-value outliers, suggesting that it’s often associated with more expensive vehicles. The "idi" and "spdi" fuel systems have relatively lower median prices but exhibit some price variability. The "2bbl" system has a much narrower and lower price range.

The "mpfi" fuel system is both the most common and associated with higher-priced cars, while "2bbl" is common but linked to lower-cost cars.

**Overall Conclusion**

**In the categorical columns, the "doornumber" feature appears to have no impact on price differences among types. It might be worth considering removing this feature when constructing regression models.**

## Correlation: 
![image](https://github.com/user-attachments/assets/1328e306-903d-422a-90d3-d13faa35e48c)

This project primarily analyzes the features that affect car prices, so in this correlation, I will mainly focus on the relationship between price and each individual feature.
From the matrix, it is evident that, except for car height, stroke, compression ratio, and peak RPM, the remaining features all have a correlation with price. Specifically:
+ Negative correlation: city MPG, highway MPG.
+ Positive correlation: wheelbase, car length, car width, curb weight, engine size, bore ratio, horsepower.

**Features that do not show any correlation with price will also be removed when incorporating them into the regression model.**

## Key insights:
### General conclusion:
Here are the results of the features that influence car prices, selected using three different methods: 

1. Features filtered by EDA: wheelbase, carlength, carwidth, curbweight, enginesize, boreratio, horsepower, citympg, highwaympg, fueltype, aspiration, carbody, drivewheel, enginelocation, enginetype, cylindernumber, fuelsystem
   
2. Features filtered by RFE: symboling, wheelbase, carlength, carwidth, carheight, curbweight, enginesize, boreratio, stroke, compressionratio, horsepower, peakrpm, citympg, highwaympg, enginetype_ohc
  
3. Features filtered by RFE+VIF: enginetype_ohc, compressionratio, enginesize, citympg, carwidth, peakrpm, stroke.

From comparison, it can be noted that the features selected for the regression model through Exploratory Data Analysis (EDA) differ from those obtained using the Recursive Feature Elimination (RFE) and Variance Inflation Factor (VIF) methods. Even features that show no correlation in the correlation matrix can still be significant when using RFE and VIF, such as "stroke." 

Next, let's examine the results of the regression models with features selected through various methods.

## Regression Models:
**R2 score and Adjusted R2 score of regression models_result 1:**
![image](https://github.com/user-attachments/assets/222f251b-af13-4600-a38a-07f1043eded2)

The adjusted R² score for the training set is quite good, while the adjusted R² for the testing set is very poor. This discrepancy is due to the number of independent variables being too large compared to the number of samples tested, which results in a negative outcome. The negative result indicates that the model is over-parameterized. Overparameterization is a concept in machine learning (ML) that refers to a model having more parameters than the available training data.

**R2 score and Adjusted R2 score of regression models_result 2:**
![image](https://github.com/user-attachments/assets/7b0c7793-36fd-469c-9e7a-b746faabf97f)

After applying Recursive Feature Elimination (RFE), the number of independent variables was reduced to 15. This adjustment also improved the adjusted R² score for both the training and testing sets.

**R2 score and Adjusted R2 score of regression models_result 3:**
![image](https://github.com/user-attachments/assets/e843a893-c29e-47e7-a209-9cc586ec9af4)

There was a slight change in the adjusted R² score for the training data, and the adjusted R² score for the testing data improved significantly.

**Overall Conclusion**
Linear Regression: Has relatively low Training R2_Score and Testing R2_Score, especially the Testing adjusted_R2_Score, which only reaches 74.90. This indicates that the linear regression model does not fit the data well and struggles to compete with more complex models.

Decision Tree and XGBoost: Show good performance with both Training R2_Score and Testing R2_Score being high and a fairly high Testing adjusted_R2_Score. This demonstrates good generalization capability, meaning they can effectively predict on new data.

Random Forest: Achieves the highest Testing R2_Score and Testing adjusted_R2_Score, indicating the best overall performance among all models. It’s the most suitable choice for this dataset as it predicts well on new data.

LGBM: Has slightly lower Testing R2_Score and Testing adjusted_R2_Score compared to other models, possibly because the data structure does not fit as well with this algorithm compared to Random Forest or XGBoost.

### Recommendations:
Manufacturing companies can focus on examining the features that significantly impact production costs. This will allow them to better control production expenses when introducing vehicles to consumers. Key features to consider include: symboling, wheelbase, car length, car width, car height, curb weight, engine size, bore ratio, stroke, compression ratio, horsepower, peak RPM, city MPG, highway MPG, and engine type (OHC).

**Focus on Key Features:**

Companies should prioritize analyzing and understanding the features that significantly influence vehicle prices. This can help in making informed decisions about production and pricing strategies.

**Cost Control Strategies:**

By understanding how specific features impact production costs, companies can identify areas to reduce expenses without compromising quality. This may involve optimizing materials or manufacturing processes.

**Market Segmentation:**

Tailor marketing strategies based on the features that appeal to different market segments. For example, emphasizing fuel efficiency (city MPG and highway MPG) for eco-conscious consumers or performance features (horsepower and engine size) for performance enthusiasts.

**Continuous Improvement:**

Regularly review and update the features based on consumer feedback and technological advancements to stay competitive in the market. This includes adapting to emerging trends, such as electric vehicles or advanced safety features.



