# Ticket Price Prediction
Ticket Price Prediction
Project Overview

This project aims to predict flight ticket prices based on various features such as airline, departure time, arrival time, flight duration, and stops. The dataset used for this project contains flight information from India in 2019. The primary goal is to build a machine learning model capable of accurately estimating ticket prices by using several preprocessing techniques and various machine learning algorithms, including decision trees, random forests, gradient boosting, and K-nearest neighbors (KNN).

The project was developed as part of the Data Mining on the Web course and participated in the MachineHack Flight Ticket Price Prediction Hackathon.
Features

    Data Preprocessing:
        Merged Date_of_Journey and Dep_Time to create a dep_date_time column.
        Split flight Duration into duration_hours and duration_minutes, also calculated total flight duration in minutes.
        One Hot Encoding for categorical columns such as Airline and Additional_Info.
        Transformed Total_Stops into an integer representing the number of stops.
        Added additional features such as city population and calculated total distance covered using geographic coordinates of airports.

    Visualization:
        Box plots and count plots were used to understand the distribution and impact of various categorical features (e.g., airline, source, destination) on ticket prices.

    Machine Learning Algorithms:
        Explored various regression models including KNN, Decision Trees, Random Forests, AdaBoost, and Gradient Boosting.
        Sequential Forward Selection was used to select the best features for the models.
        Hyperparameter tuning was performed using GridSearchCV to optimize model performance.

Dataset Description

The dataset contains the following columns:

    Airline: Name of the airline.
    Date_of_Journey: Date of flight.
    Source/Destination: Cities of departure and arrival.
    Dep_Time/Arrival_Time: Time of departure and arrival.
    Duration: Total flight time including layovers.
    Total_Stops: Number of stops between source and destination.
    Additional_Info: Any other additional information about the flight.
    Price: The target variable for prediction.

Preprocessing Steps

    Feature Engineering:
        Converted dates into cyclical day-of-year format.
        Encoded categorical variables using One Hot Encoding.
        Calculated total distance covered using airport coordinates.
        Added population data for source and destination cities.
    Feature Selection:
        Performed feature importance analysis using an ExtraTreesRegressor and explored correlations between features to reduce dimensionality.
        Removed unnecessary features such as Additional_Info due to low correlation with price.

Model Performance

    Gradient Boosting: Achieved the best results with an RMSLE score of 0.923, ranking within the top 300 in the MachineHack competition.
    Other Algorithms:
        KNN, Decision Trees, and Random Forests performed reasonably well, with Random Forest achieving an r2-score of 0.80.
        SVD and AdaBoost were replaced with better-performing algorithms (Extra Trees and Extreme Gradient Boosting) due to poor results.
    Hyperparameter Tuning: Gradient Boosting was further optimized using GridSearchCV, achieving the highest performance with a learning rate of 0.1 and other fine-tuned parameters.
