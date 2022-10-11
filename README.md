# World_Weather_Analysis

## Overview of Analysis

The purpose of this repository is to create new additions to the PlanMyTrip app. Beta testers have tested out the application and have recommended a few changes to take the app to the next level.They recommended adding the weather description to the weather data. Beta testers will then use input statements to filter the data for their weather preferences, which will be used to identify potential travel destinations and nearby hotels. From the list of potential travel destinations, the beta tester will choose four cities to create a travel itinerary. Finally, using the Google Maps Directions API, users will see a travel route between the four cities as well as a marker layer map. This update will consist of three new technical features: 
- Retrieve Weather Data
- Create a Customer Travel Destinations Map
- Create a Travel Itinerary Map

## Retrieve Weather Data

A weather database is created by running an API on Open Weather Map and retrieving a 2,000 sets of random latitudes and longitudes. The set is stored in a list of cities, then parsed using JSON format, then converted into a pandas dataframe. 
#### Weather Database
![Weather Database](https://user-images.githubusercontent.com/73972332/104137939-6fec1300-5355-11eb-9b6f-48158e33ba50.png)
## Create a Customer Travel Destinations Map
A travel destinations map is created by reading the weather database file into a dataframe, prompting the user to enter minimum and maximum temperature criteria, and filtering the dataframe based on the user weather preferences while creating a new dataframe out of the filtered information. Then a new dataframe is created by adding a column for nearby hotels. Nearby hotels are found by using a Google Maps & Places API Key to search for hotels within 5,000 meters of the random coordinates in the weather database. A marker layer is added for the hotel names and the information is displayed as a destination map. 

#### Weather Vacation Map

![WeatherPy_vacation_map](https://user-images.githubusercontent.com/73972332/104138061-6adb9380-5356-11eb-9593-891ce62cd7a2.png)
## Create a Travel Itinerary Map
A travel itinerary that shows the route between four cities chosen from the customer’s possible travel destinations is created from using the Google Directions API. Then finally and as the last part of the application updates, a marker layer map with a pop-up marker for each city on the itinerary is created. A user now has a full blown temperature preferenced based maps itinerary provided for them! 

#### Travel Map

![WeatherPy_travel_map](https://user-images.githubusercontent.com/73972332/104138373-8e074280-5358-11eb-9d68-d4479c599845.png)

#### Travel Map with Markers for each hotel showing Current Weather Descriptions

![WeatherPy_travel_map_markers](https://user-images.githubusercontent.com/73972332/104138391-a0817c00-5358-11eb-9dc1-ac38933b15dc.png)
