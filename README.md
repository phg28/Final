# [Final Project] - Uyen Phuong
## Car Prices Predicting

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

## Tools and Technologies:
Python, Pandas, Matplotlib, Seaborn, etc.

## Purpose and Outcome:
Purpose: To determine the features of a car that affect its price and to create predictive models with high accuracy.
Outcome: A precise model for predicting car prices, along with features that affect those prices.


# Key insights: (đưa thêm bảng r2 và adj r2 để thể hiện kết quả)
General conclusion:
Here are the results of the features that influence car prices, selected using three different methods: 

1. Features filtered by EDA: wheelbase, carlength, carwidth, curbweight, enginesize, boreratio, horsepower, citympg, highwaympg, fueltype, aspiration, carbody, drivewheel, enginelocation, enginetype, cylindernumber, fuelsystem
   
2. Features filtered by RFE:
  
3. Features filtered by RFE+VIF:

# Recommendations:
   
