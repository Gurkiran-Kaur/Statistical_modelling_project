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
In order to identify and fetch meaningful data, each  API’s documentation page had to be studied in depth.

Based on data built in part 1 from Citybik, an API call was made both to Foursquare and Yelp with a small radius (1000m) for all the bike stations in cork city

Obtained response was parsed to get the POIs (such as restaurants, bars, entertainment) and their details  like ratings, review count, name, location, categories, coordinates,distance from station etc)

Parsed results were put into a DataFrame and also into a csv file

Data obtained was studied and comparison of  information obtained from Yelp vs Foursqaure was done

Top ten restaurants according to rating were found from both Yelp and Foursquare

### Part 3
Data from part 1 and Part 2 was finally merged to create a new dataframe.

Data visualisation was done to explore the data. A bar plot was created to show the number of empty slots at each bike station. 

Scatter plots were plotted to probe if any pattern or corelation exists between the number of empty slots at a particular station (which shows how busy it is) and how close any POI (shortest distance) to this station is. Scatter plot for both Yelp and FSQ were plotted. 

It was evident from scatter plots that there is positive corelation between these variables but it is not strong. 

SQLite database was created and validated to store the combined data.


### Part 4

A linear regression model was built to demonstrate relationship between a relationship between the shortest distance (closest POI) to a bike station  and number of empty slots using   


## Results
After comparing both the comparison
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

