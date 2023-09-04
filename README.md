# Final-Project-Statistical-Modelling-with-Python

## Project/Goals
The goal of this project is to combine and practice implementing statistical modelling with python.
In this project three APIs namely City_bikes, Four Square places API and Yelp API were queried. A comparison of quality of both Yelp and Four square places API in terms of best coverage and information was done.
Finally regression model that demonstrates a relationship between the shortest distance (closest POI) to a bike station  and number of empty slots  was built and interpreted. 
## Process
### Part 1
Connected  to CityBikes API, queried it and tried exploring it’s structure.
Chose the city named “Cork” and retrieved all available bike stations in that city
For each bike station, the API was used to call the latitude, longitude and number of bikes.
Finally this JSON object was parsed into python and converted into a dataframe. 

### Part 2
Based on data built in part 1 from Citybik, relevant keys were identified as Latitude and Longitude for each Station in the list of stations.

Using values of Latitudes and Longitudes, for each of the bike stations in Part 1, both APIs were queried to retrieve information for the following in that location:
 1. Restaurants or bars
 2. Arts and Entertainment

In order to identify and fetch meaningful data, each  API’s documentation page had to be studied in depth.
Panda data frame was then used to normalize the data for human reading use.
### Part 3
Data from part 1 And Part 2 was finally merged to create a new dataframe.SQLite database was created and validated to store the combined data.
Data visualization 

### Part 4

A regression model was built to demonstrate relationship between ....... 


## Results
comparison
regression
classification

## Challenges 
Reading and understanding API was time consuming.
Picking the relevant keys out of the API data for each one of data sources was tricky
Limited calls to yelp API was also an issue 

## Future Goals
I could have studied API in more detail and come up with more innovative ideas specially around picking up keys to filter data.
multivariate regression
take bigger city
collect more POIs and characterstics

