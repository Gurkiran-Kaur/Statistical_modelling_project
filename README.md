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

Obtained response was parsed to get the POIs (such as restaurants, bars, entertainment) and their details  like ratings, review count, name, location, categories, coordinates,distance from station etc.

Parsed results were put into a DataFrame and also into a csv file

Data obtained was studied and comparison of  information obtained from Yelp vs Foursqaure was done

Top ten restaurants according to rating were found from both Yelp and Foursquare

### Part 3
Data from part 1 and Part 2 was finally merged to create a new dataframe.

Data visualisation was done to explore the data. A bar plot was created to show the number of empty slots at each bike station. 

Scatter plots were plotted to probe if any pattern or corelation exists between the number of empty slots at a particular station (which shows how busy it is) and how close any POI (shortest distance) to this station is. Scatter plots for both Yelp and FSQ were plotted. 

It was evident from scatter plots that there is positive corelation between these variables but it is not strong. 

SQLite database was created and validated to store the combined data.


### Part 4

A linear regression model was built to demonstrate relationship between the shortest distance (closest POI) to a bike station  and number of empty slots.   


## Results
After comparing  the quality of the Yelp and Foursquare API, it can be concluded that Yelp API gives the more complete information and better coverage.
For example, apart from giving the POI it is also  telling whether that POI is closed or not which is very important information one would look for.
Review count is another additional key present in Yelp compared to FSQ.

The regression model output gives R-squared value of 0.309 which suggests that model explains a moderate amount of the variability in the data.
The adjusted R-squared (Adj. R²) is 0.287, which is slightly lower than R-squared. This might be due to overfitting or there might be other variables which can be explored to improve the fitting.

Also  with a p-value of 0.001, it can be deduced that the model is statistically significant and there is strong evidence to suggest that changes in the "Shortest Yelp Distance from Station" variable are associated with changes in the number of empty slots. We can say the distance from the station is likely a significant predictor of the number of empty slots.

The collated code for this project with all outputs is present in notebook named original_code_with_outputs which can be found in data directory.

## Challenges 
Reading and understanding API was time consuming.
Picking the relevant keys out of the API data for each one of data sources was tricky
Since the city has less number of bike stations, sometimes number of bikes value were all zero.So instead of number of bikes, number of empty slots was chosen as a variable to get insights. 
Limited calls to yelp API was also an issue 

## Future Goals
I could have studied API in more detail and come up with more innovative ideas specially around picking up keys to filter data.

Can go for multivariate regression for checking the effect of value of shortest distance or distance of nearest POI on empty slots for both the API calls i.e foursquare as well as yelp and explore further.

Explore the data for bigger and busier city

Collect data for more number of POIs and characterstics



