# Data Investigation Report
This report provides the outcome of the investigation of analysis of the neighborhoods in downtown Toronto
##  Introduction/Business Problem
The satisfaction of residents is significantly defined by the amount of time they take to reach their places of interest. Further more, the reduction of travel time for residents means reduction of traffic for the city. 
According to [1], 47% of Toronto households are renting, therefore are reasonably mobile. Enabling the residents to choose locations that would optimise their access to their places of interest would not only improve their satisfaction, but would also  reduce the pressure on transport infrastructure
## Available Data
The following data are available for the project:
### Administrative data
Administrative data are sourced from Wikipedia. The data available specify:
1. Postal Code
2. Borough
3. Neighborhood
By using 
### Geo data
Geo data, available via the **geopy** package. The use of the data is available at different levels
1. We can use it to identify the locations defined for the postal codes
2. We can also chase individual venues on the basis of street addresses
For this project, we found "1" sufficient
### Foursquare data
We use Foursquare API to get information allowing us to assess the character of a neighborhood
1. On the most basic level, the project would use the *explore*  interface to find the most recommended venues within given area, and identify their types
2. On the more advanced level, we can hunt details and reviews, to implement more advanced, social-based similarity
The key informaiton we will be looking is the types of venues that are available in the neighborhood.
## Methodology
The following steps were performed
### Exploratory Analysis
To better understand the data, wthe following steps were performed
#### Analysing the number of groups in Roursquare responces
It was found that only one group is ever present
#### Building distance matrix
To understand how close/far the neighborhoods were  
### Choice of approach
It was decided that the solution should be based on K-Means Clustering. 
### Choice of measure
It was decided that a neighborhood shou be represented by a 309-dimentional vector specifying the number of venues per each Category. The default implementation of K-Means uses Eucleadean metrics. However it would be unsuitable for that task, as a neighborhood with 25 Italian Restaurants would be further from a neighborhood with 5 Italian restaurants than a neighborhood with 5 Irish bars.
It was decided that Cosine Similarity would suit the need of the project. Cosine Similarity is equivalent of Euclidean distance once the ventors are normalised  
## Results
The visualisation showed that the most reasonalbe estimation woud be with 5 clusters. 
### Recommendation
Further work would be recommended on describing the Clusters. A finer approach would take advantage of the hierarchy of Categories available from Foursquare
## Conclusion
It is clear that different neighbourhoods have their clear define characters. Also, it is clear that Toronto have several geographically distant areas that however should have quite similar feel. Therefor it would make sense to provide the renting public with such informaiton to enalbe them to live closer to their places of employment while enjoying the urban environment they prefer. 


[1] https://toronto.citynews.ca/2018/02/09/rental-market-toronto/