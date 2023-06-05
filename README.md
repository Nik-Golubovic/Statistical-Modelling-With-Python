# Final-Project-Statistical-Modelling-with-Python

## Project/Goals
The goal of the project is to query the API for citybikes and pull relevant information for the city of Hamilton, ON. We will use the location of the hubs as a starting point for two additional API's. We will also query Foursquare and Yelp, using the information gathered from CityBikes to find the closest restaurants and bars. Our goal is to create a visualization of which hubs have the closest POI and in the case of the Yelp API, we will also check which hubs have the highest rated POIs.

## Process
### Step 1
The first step in the process will be to gather the relevant information from the respective APIs. We will query CityBikes and get Hub location information, which we will use as a referenece point to query FOursquare and Yelp to find nearby POIs. Once we have gathered this info, we will convert all of the tables into a usbale format and create an SQL database for further analysis. 
### Step 2
We will be using the Haversine formualtion to determine the distance between the POIs and the location of the Hub. This information will help us gather further insights into which Hubs have the closest POIs and which Hubs have the highest rated, on average, POIs nearby.
## Results
Multiple maps were successfully created that showcase the availablilty of restaurants in the city. The Foursquare database was used to show the average distance of the top ten closest restaurants to each bike hub. The Yelp Database was used to create a map showcasing the average rating of the ten closest restaurants near each bike hub. 

The results of the map showed fairly accurate results, if you are aware of the city's layout. The Hubs with the closest restaurants tended to be close to downtown and city hall, whee there is the most urban build up, whereas the hubs with the furtheres POIs tended to be in the east end of the city (where the infastructure is less dense) and in the far west of the city, where the village of Dundas borders on rural land. 

THe results of the ratings were also in line. THe highest rated POIs tended to be in the Locke street neighbourhood (well known for having very good restaurants and being a hip, urban center) and Westdale village, which is close by to the University and has a wide variety of diffrent POIs. The worst rated POIs tended to be in the core of the city, where there is an abundance of places, as well as some really small hole-in-wall places, and the indutrial areas. The surprising thing to note was that the less urbanised East end happened to have on average higher rated POIs, and this may be due to the scarcity of available places.

## Challenges 
Below is a list of some of the challenges that were faced in this project.
-Formatting the API results to properly enter into the dataframes.
-Hitting the limit of calls in the Yelp API which led to having to create multiple accounts. Running the APIs mutiple times was not a good way of trouble shooting. 
-Accuracy of the Yelp API in its ability to properly classify what each of the POIs was, categorically.
-Accidentaly overwriting an entire dataframe by using the same variable name as previously used and having to hope that there was still avaiable calls on my account, to regenerate the data. (This is why you commit often!)

## Future Goals
If we had more time, I would have liked to sort through the results of both queries a little better. I would have liked to try and add additional restrictions to the API calls to limit things like: POIs classified incorrectly, or POIs with a small sample size of reviews.

In the future I will be using this database and checking the accuracy of the generated results by physically going to these bike locations and testing out thew nearby restaurants. Seems to me like I've managed to create a good "date-night" application.


## WARNING
Remove the CSV files from the folder and add them to the main directory before attempting to run any of the code. 