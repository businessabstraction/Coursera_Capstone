# Data Investigation Report
This report provides the outcome of the investigation of analysis of the neighborhoods in downtown Toronto
##  Introduction/Business Problem
The satisfaction of residents is significantly defined by the amount of time they take to reach their places of interest. Further more, the reduction of travel time for residents means reduction of traffic for the city. 
According to [1], 47% of Toronto households are renting, therefore are reasonably mobile. Enabling the residents to choose locations that would optimise their access to their places of interest would not only improve their satisfaction, but would also  reduce the pressure on transport infrastructure
## Available Data
The following data are available for the project:
### Administrative data
Administrative data are souced from Wikipedia. The data available specify:
1. Postal Code
2. Borough
3. Neighborhood
By using 
### Geo data
Geo data, available via the **geopy** package. The use of the data is available at different levels
1. We can use it to identify the locations defined for the postal codes
2. We can also chase individual venues on the basis of street addresses
For this project, we found "1" sufficient
## Foursquare data
We use Foursquare API to get information alowing us to assess the character of a neighborhood
1. On the most basic level, the project would use the *explore*  interface to find the most recommended venues within given area, and identify their types
2. On the more advanced level, we can hunt details and reviews, to implement more advanced, social-based similarity
The key informaiton we will be looking is the types of venues that are available in the neighborhood.

[1] https://toronto.citynews.ca/2018/02/09/rental-market-toronto/