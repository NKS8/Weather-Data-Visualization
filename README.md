# python-api-challenge 
## Part I-Section 1.

In this challenge a Python script used to visualize the weather of 500+ cities across the world of varying distance from the equator. To accomplish this, it will be utilized a simple Python library, the OpenWeatherMap API to create a representative model of weather across world cities.

The follwing requirements are completed to show relations below:

1. Temperature (F) vs. Latitude  2. Humidity (%) vs. Latitude
<img width="564" alt="Max_temp" src="https://user-images.githubusercontent.com/67448948/123169254-0a916780-d447-11eb-8de3-af7bca7f0855.png">

In the above graph (City Latitude vs Max Temperature) shows:
When latitude changes from -60 to +20 max temp of cities rise then falls back until Lat of 80 while having some sort of symmetry .
20 is being highest point, then both sides drop equally range of 60 as the Latitude spreads. Quadratic function may fit nicely, unless if it is splitted @ latidue 20 and do two separate linear regressions.

2. Humidity (%) vs. Latitude
 <img width="512" alt="Lat_vs_humidity" src="https://user-images.githubusercontent.com/67448948/123162898-25f87480-d43f-11eb-9fd3-f8e5856395f5.png">
 In the above graph, City Latitude vs Humidity scatter plot shows that:
Regardless of lattiude change, more cities are scattered where humidity is between 60% & 100%. But, when latidude is >= 0, there are more cities where humdity is below 40% compare to opposite same latitude. It may show different pattern as season changes since plot are made on current weather data.

3. Cloudiness (%) vs. Latitude
<img width="569" alt="lat_vs_Cloudiness" src="https://user-images.githubusercontent.com/67448948/123162910-285ace80-d43f-11eb-99ad-d5566a59e88a.png"> 

In the above plot (From City Latitude vs Cloudiness) shows :
When latitude between (-40 and -20, cities are clustered @ 0 cloudiness.
Also, when latitude between +20 and +50 cities are clustered @ 0 cloudiness.
When latitude between 0 and 20, more cities clustered close to 100% cloudiness.
It looks like, if the step functions used, it may fit properly.

4. Wind Speed (mph) vs. Latitude
 <img width="566" alt="Lat_vs_windSpeed" src="https://user-images.githubusercontent.com/67448948/123162917-298bfb80-d43f-11eb-9527-c38419761bd3.png">
In the above plot (City Latitude vs Wind Speed shows):
Density of cities scattered is between where Wind speed is between 0-10 mph, or rather shows that it has less dependcy on the latitude.

## Part I -Section 2.

Then linear regression is performed on each relationship. This time, separate the plots into Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude):

5. Northern Hemisphere - Temperature (F) vs. Latitude 
 <img width="455" alt="northern_temp_lat" src="https://user-images.githubusercontent.com/67448948/123163298-90111980-d43f-11eb-9e8f-2ff778952b97.png">
6. Southern Hemisphere - Temperature (F) vs. Latitude 
 <img width="437" alt="Southern_temp_lat" src="https://user-images.githubusercontent.com/67448948/123163325-9a331800-d43f-11eb-8769-1354b7fde9fd.png">
7. Northern Hemisphere - Humidity (%) vs. Latitude 

<img width="488" alt="Northern_Hhumidity_lat" src="https://user-images.githubusercontent.com/67448948/123163470-bdf65e00-d43f-11eb-96c1-25a652d4698b.png">
8. Southern Hemisphere - Humidity (%) vs. Latitude
<img width="469" alt="Southern_Humidity" src="https://user-images.githubusercontent.com/67448948/123163495-c484d580-d43f-11eb-9771-0b720ac5fbf8.png">
9. Northern Hemisphere - Cloudiness (%) vs. Latitude
 <img width="444" alt="northern_cloudiness" src="https://user-images.githubusercontent.com/67448948/123163524-cf3f6a80-d43f-11eb-9c74-c429d27fa3f5.png">
10. Southern Hemisphere - Cloudiness (%) vs. Latitude
<img width="494" alt="Southern_cloudiness" src="https://user-images.githubusercontent.com/67448948/123163560-d9f9ff80-d43f-11eb-92ce-d4accae1d2ed.png">
11. Northern Hemisphere - Wind Speed (mph) vs. Latitude 
 <img width="518" alt="northern_wind" src="https://user-images.githubusercontent.com/67448948/123163592-e2523a80-d43f-11eb-90ab-f806a6151160.png">
12. Southern Hemisphere - Wind Speed (mph) vs. Latitude
<img width="502" alt="Southern_wind" src="https://user-images.githubusercontent.com/67448948/123163612-e8481b80-d43f-11eb-95f7-8dc511dbc86c.png">

## Observation for Part I- Section 2.  

Max Temperature: Temperature in south hemisphere increases as latitude decrease/getting closer to the equator, the opposite happens in northern hemisphere. Note: The Highest Max temperature occurs cities are located around latitude of 20.
Humidity: In both Northern and Southern hemisphere where cities are located latitude wise does not have a strong correlations between Latidue and Humidity.
Northern and Southern hemisphere both higher density cloudiness close to zero versus close to hundred in depends on ranges of latitudes shows on the graph.
Regardless of latitude, in both most cities in regions of southern and northern hemisphere the wind speed ranges between 0-10 mph. So wind does not heavily effected by where city location is laitude wise, it is rather other affected by other factors.

## Part II 
1. Created a heat map that displays the humidity for every city from Part I. 
The heat map for cities weather data obtained from Part I. 
<img width="742" alt="Heat map for over 500 cities  2021-06-23 154724" src="https://user-images.githubusercontent.com/67448948/123168381-e5502980-d445-11eb-9de6-5cb3e6b50341.png">

2. Narrowed down the DataFrame to find your ideal weather condition. 
For example:
A max temperature lower than 85 degrees but higher than 82.
Wind speed less than 4 mph.
Zero cloudiness.
Dropped any rows that don't contain all three conditions to be sure the weather is ideal. Note: Felt free to adjust to my specifications but be sure to limit the number of rows returned by my API requests to a reasonable number.
Used Google Places API to find the first hotel for each city located within 5000 meters of your coordinates.
Plotted the hotels on top of the humidity heatmap with each pin containing the Hotel Name, City, and Country. 

<img width="737" alt="Ideal Vacation spot map  2021-06-23 154845" src="https://user-images.githubusercontent.com/67448948/123168393-ea14dd80-d445-11eb-8d75-1483b59fcdd9.png">

Above cities are narrowed down and shown on the google map with Hotel Name, City, and Country.
