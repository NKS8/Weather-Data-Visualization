# python-api-challenge

In this challenge a Python script uesd to visualize the weather of 500+ cities across the world of varying distance from the equator. To accomplish this, it will be utilized a simple Python library, the OpenWeatherMap API to create a representative model of weather across world cities.

The follwing requirements are completed to show relations below:

1. Temperature (F) vs. Latitude  2. Humidity (%) vs. Latitude
<img width="564" alt="Max_temperature" src="https://user-images.githubusercontent.com/67448948/123162886-22fd8400-d43f- 1eb-8e5a-01a15c67ea11.png"> 
In the above graph (City Latitude vs Max Temperature) shows:
When latitude changes from -60 to +20 max temp of cities rise then falls back until Lat of 80 while having some sort of symmetry .
20 is being highest point, then both sides drop equally range of 60 where Latitude spreads. Quadratic function may fit nicely, unless if it is splitted @ latidue 20 and do two separate linear regressions.
2. Humidity (%) vs. Latitude
 <img width="512" alt="Lat_vs_humidity" src="https://user-images.githubusercontent.com/67448948/123162898-25f87480-d43f-11eb-9fd3-f8e5856395f5.png">
3. Cloudiness (%) vs. Latitude
<img width="569" alt="lat_vs_Cloudiness" src="https://user-images.githubusercontent.com/67448948/123162910-285ace80-d43f-11eb-99ad-d5566a59e88a.png">
4. Wind Speed (mph) vs. Latitude
 <img width="566" alt="Lat_vs_windSpeed" src="https://user-images.githubusercontent.com/67448948/123162917-298bfb80-d43f-11eb-9527-c38419761bd3.png">


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

