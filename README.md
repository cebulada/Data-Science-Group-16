# Data Science 2:  Statistics for Data Science

## Group 16 Members

- 1. Su Wang - [Email](mailto:s399wang@uwaterloo.ca)
- 2. Mabi Mabbayad - [Email](mailto:mmabbaya@uwaterloo.ca)
- 3. Kira Xue - [Email](mailto:w27xue@uwaterloo.ca)
- 4. Igor Jajcanin - [Email](mailto:ijajcani@uwaterloo.ca)
- 5. Daniel Adam Cebula - [Email](mailto:dacebula@uwaterloo.ca)
- 6. Wenwen Shi - [Email](mailto:w65shi@uwaterloo.ca)

## Group Topic

- Our group would like to study the Citibike New York City data set from Oct. 2015 - Oct. 2020.
    - [Link](https://www.citibikenyc.com/system-data) to System Data
    - [Link](https://s3.amazonaws.com/tripdata/index.html) to s3 bucket of all datasets

## DataFrame and Columns

- We will explore a 5 year data set that has the following dataframe structure.

 |    |   tripduration | starttime         | stoptime          |   start station id | start station name      |   start station latitude |   start station longitude |   end station id | end station name      |   end station latitude |   end station longitude |   bikeid | usertype   |   birth year |   gender |
|---:|---------------:|:------------------|:------------------|-------------------:|:------------------------|-------------------------:|--------------------------:|-----------------:|:----------------------|-----------------------:|------------------------:|---------:|:-----------|-------------:|---------:|
|  0 |           1202 | 8/1/2015 00:00:04 | 8/1/2015 00:20:07 |                168 | W 18 St & 6 Ave         |                  40.7397 |                  -73.9946 |              385 | E 55 St & 2 Ave       |                40.758  |                -73.966  |    23253 | Subscriber |         1987 |        1 |
|  1 |            301 | 8/1/2015 00:00:05 | 8/1/2015 00:05:06 |                450 | W 49 St & 8 Ave         |                  40.7623 |                  -73.9879 |              479 | 9 Ave & W 45 St       |                40.7602 |                -73.9913 |    22675 | Subscriber |         1951 |        2 |
|  2 |            431 | 8/1/2015 00:00:06 | 8/1/2015 00:07:18 |                312 | Allen St & E Houston St |                  40.7221 |                  -73.9891 |              296 | Division St & Bowery  |                40.7141 |                -73.997  |    19831 | Subscriber |         1985 |        1 |
|  3 |            273 | 8/1/2015 00:00:09 | 8/1/2015 00:04:43 |                382 | University Pl & E 14 St |                  40.7349 |                  -73.992  |              229 | Great Jones St        |                40.7274 |                -73.9938 |    22765 | Subscriber |         1975 |        1 |
|  4 |           1256 | 8/1/2015 00:00:17 | 8/1/2015 00:21:13 |                352 | W 56 St & 6 Ave         |                  40.7634 |                  -73.9772 |              432 | E 7 St & Avenue A     |                40.7262 |                -73.9838 |    22127 | Subscriber |         1978 |        1 |
|  5 |            739 | 8/1/2015 00:00:24 | 8/1/2015 00:12:44 |                212 | W 16 St & The High Line |                  40.7433 |                  -74.0068 |              498 | Broadway & W 32 St    |                40.7485 |                -73.9881 |    19293 | Subscriber |         1988 |        1 |
|  6 |            433 | 8/1/2015 00:00:30 | 8/1/2015 00:07:43 |                388 | W 26 St & 10 Ave        |                  40.7497 |                  -74.003  |              284 | Greenwich Ave & 8 Ave |                40.739  |                -74.0026 |    19115 | Subscriber |         1976 |        1 |
|  7 |           1575 | 8/1/2015 00:00:33 | 8/1/2015 00:26:49 |                492 | W 33 St & 7 Ave         |                  40.7502 |                  -73.9909 |              492 | W 33 St & 7 Ave       |                40.7502 |                -73.9909 |    20532 | Customer   |          nan |        0 |
|  8 |            843 | 8/1/2015 00:00:39 | 8/1/2015 00:14:43 |                387 | Centre St & Chambers St |                  40.7127 |                  -74.0046 |              391 | Clark St & Henry St   |                40.6976 |                -73.9934 |    24273 | Customer   |          nan |        0 |
|  9 |            467 | 8/1/2015 00:00:49 | 8/1/2015 00:08:37 |                285 | Broadway & E 14 St      |                  40.7345 |                  -73.9907 |              284 | Greenwich Ave & 8 Ave |                40.739  |                -74.0026 |    17688 | Subscriber |         1976 |        1 | 

- The following columns are present
    - Trip Duration
        - in seconds
    - Start Time and Date of Trip
        - Date and Time in Eastern Standard Time Zone (GMT - 5)
    - End Time and Date of Trip
        - Date and Time in Eastern Standard Time Zone (GMT - 5)
    - Start / End Station Name
        - Name of Station that trip started and ended in
    - Start / End Station ID
        - ID of Station that trip started and ended in
    - Start / End Station Latitude and Longitude
        - Latitude and Longitude of Station that trip started and ended in
    - Bike ID
        - unique ID of bike used during trip
    - User Type
        - Customer
            - 24 hour or 72 hour member
        - Subscriber
            - Annual member
    - Gender of rider (self-reported)
        - 0
            - Unknown
        - 1
            - Male
        - 2
            - Female
    - Year of Birth of rider (self-reported)
        - ex. 1900

## Type of Analysis

- Our group would like to do several types of analysis with the dataset

- 1. Time Series Analysis of all Bicycle Trips summarized by hour / day / week / month aggregation with the following dependant attributes:
    - trip duration
    - trip distance (calculated by Haversine formula using Latitude and Longitude values)
    - count of each user types (pivot column)
    - count of each start station (pivot column)
    - count of each end station (pivot column)
    - count of each gender (pivot column)
    - count of each birth year (pivot column)

- 2. Perform Bayesian Analysis of Bike Trip Data (Naive Bayes)
    - modify several parameters and observe the changes in simulated Bike Trip data

## Project Requirements

- 1. Make a hypothesis about a correlation in a dataset and test the hypothesis using a statistical inference technique (such as the t-test).
- 2. Build a predictive model using one of the techniques covered in the course, i.e., ordinary least squares regression or Naïve Bayes.

## Group Project Requirements

- 1. Collaborate with peers to solve a Data Science Problem
- 2. Work in a group setting to complete a challenge within an agreed-upon time frame
- 3. Engage with peers to discover their problem-solving process and lessons learned
- 4. Carry out a statistical analysis using real data
- 5. Hone Skills in explaining technical details to a non-technical audience
