# Craigslist Vehicles TSA

Given data on from [craigslist vehicles](https://www.kaggle.com/datasets/mbaabuharun/craigslist-vehicles) for the period April to May 2021, perfrom a Time series analysis task on the data and possibly build a time series model. More details on the data and its information can be found on the [notebook](https://github.com/Nickimani/craigslist_used_vehicles_TSA/blob/main/Code.ipynb).

Here are the key steps:

1. Start by addressing missing values in the dataset. You can handle this by filling in missing values with the median for numerical columns and the mode for categorical columns. 
2. Ensure that the data types of the columns are appropriate. Specifically, make sure to convert the 'posting_date' column to a datetime data type.
3. Utilize the 'posting_date' column to create a datetime index for the dataset. This will facilitate the analysis of temporal patterns.
4. With clean data, explore it using various visualizations and statistical analysis techniques. This step is crucial for understanding temporal patterns, identifying seasonal trends, and analyzing demand-supply dynamics by region and vehicle type.
5. Build the time-series chart.
6. Finally, create a GitHub Repository and push your work there, also document your process through each of the steps and demonstrate your understanding by implementing them on the dataset.

We start by cleaning the data where some things come to light: 

- The features in the dataset have a high percentage of missing values with some features like 'county' having no non-null records.
- There are a lot of outliers in the numeric features, some of these seem to be errors during recording for example failing to record data with decimal points.
- There are a lot of typos in the object columns with car 'model' and 'description' being the features that stand out on this.

After cleaning we perform analysis on the data to get insights on client behavior and other characteristics of the data. Below are the findings extracted from the data: 

1. Ford is the most popular car manufacturer, leaving chevrolet, the runner up by a large margin. Considering that this is the American market and Ford is a locally manufactured vehicle, it is not shocking to see it as so.
2. The Ford F-150 model is posted a lot on craigslist, this would mean that it is a very popular car model in demand by consumers followed by Chevrolet Silverado 1500.
3. The craigslist postings are especially frequent in the state of california with over 500 posts being done per day, this leads us to think that the market in california is very good. Looking at information on California, it is one of the richest states in USA that had a GDP per capita of $72,569 as of 2021 meaning that people there should have quite the disposable income.
4. There are two classes of cars when you consider them in terms of year of manufacture, Vintage and modern cars. The threshold used to separate the two classes is the yar 1998. These two classes have completely different relationships to price. For vintage cars, the older the car, the more pricey it is. Whereas for modern cars, the older a car is, the lower the price that it can fetch.
5. The milage of a car is an important factor to consider when buying it. The general trend is, the more a cars milage, the cheaper it should be. While this applies to both classes of car, it seems to matter less when dealing with vintage cars since they have a lower negative correlation to price when compared to modern cars.

We hoped to come up with a time series model for this problem, however the data is too small for such a task. Therefore, no modelling is done using this data. 
