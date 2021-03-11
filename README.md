# Fire_Houses
A Spatial Analysis of New York City Fire Houses


## Background
Fire stations are important facilities in urban areas that can guarantee residents' life and safety. According to the United
State Fire Administration, there are 1194 home fire fatalities reported in 2018. About 49% (figure 1) of the incident reported is related to Emergency Medical Service (EMS). Obviously, with the increasing population in the city, there more demand for fire stations. The delivery of an EMS is time-critical. As shown in the figure, the victims who have a heart attack will have a higher survival rate if CPR started within four minutes. Thus, fire stations' location selection is essential so that firefighters can reach the incident site in the golden five minutes (Sen et al., 2011).\
GIS is a powerful tool for a firefighter in planning and predicting risk. Using network analysis, a service area map can be created to see if there any unserved areas. With the use of density analysis, the risk of incidents can be determined. Besides, point pattern analysis allows us to see the current fire station's spatial pattern to plan for future facilities.

## Objectives
This paper aims to analyze the spatial pattern of current fire stations in New York City. Also, looking at the service area map for current facilities and finding potential places for building a new station.

## Method and Data
Information about the fire stations and the hospital will be acquired from the New York Open Data website. Census, borough boundary, and other geography information of New York City can be accessed through the New York City data dropbox. This paper uses the 2010 census data to calculate population density and household density. General data workflow includes data clean-up will be done through Microsoft Excel.\
A geographic information system (GIS) is a powerful tool to analyze spatial patterns and relationships. "XY table to point" and "geocode table" are tools that allow importing original CSV data into ArcGIS pro. Using the "Selecting features" tool allows us to exclude data points that are not within the study area. With dasymetric mapping, population and household density are visualized.\
The New York City (NYC, in short) refers to the five boroughs, which is The Bronx, Brooklyn, Manhattan, Queens, and Staten Island. This paper will examine the spatial pattern of charging stations in the whole NYC area. This will be done by applying Ripley’s K function and standard deviation ellipse to the point data set. Comparing the observed k value with the confidence envelope, we can identify its spatial pattern. Generally, a spatial clustering pattern occurs because of the observed k value greater than the two confidence envelopes or vice versa. When observed k lie between the confidence envelops, it tells a random pattern.\
Proximity analysis (Euclidean Distance) applies to see the standard distance from an existing fire station or hospital. The result of  Euclidean distance will then be reclassified into ten different classes. For both facilities, the greater distance between stations, the assigned weight will be higher. Areal interpolation (weighted overlay) will allow us to overlay the land use raster with the Euclidean distance result. This paper restricted all residential and commercial related land. Only consider public accessible land as a suitable location. Places closer to the hospital and further from the existing fire station will be assigned more significant value. Figure 2 shows the detailed setting of this weighted overlay. Overall, the location with weighted overlay results greater than (or equal to) 7 will be considered suitable.\
Network analysis is another method used in this paper. This analysis used a walking network as the transportation network due to limited traffic and road conditions. This study assumes a five-minute driving distance needs thirty minutes to walk so that the cut-off value set in the service area is 30, 60, 80, and 100 minutes.


## Results
As a result of density analysis, from Figures 3 and 4, the population and household density is higher in the Manhattan and Bronx borough. With a higher population and household density, the risk is considered higher. Observation from figure 5 suggests the fire stations are clustered in the Manhattan and Brooklyn area. By applying Ripley’s k function in figure 6, the results prove that the fire stations are significantly clustering in a small distance in NYC.\
The Euclidean Distance map shows the higher value locates mostly at the edge of the borough boundary. Higher value, in this case, refers to a greater distance from an existing facility. When overlay with a land-use raster layer with 40% weighted, a new fire station's potential location is shown in the following map. As a summarized result (Table 1), the Brooklyn area has the highest number of existing fire stations. The Bronx and Staten Island have the lowest number of facilities but more places to build a new one. Among the five boroughs, the Manhattan area has the least area for building new fire stations. According to Lai, a fire station should ideally have an area greater than four square kilometers. When we apply this condition to our results, only two areas are left (Table 2). One locates in the northern Bronx area, with a size of eight square kilometers. The other one is four square kilometers large and locates in the southern Queen area.\
From observation in the service area map, most of the area can reach four minutes-drive if an incident occurs. The area needs more than four minutes to reach are mainly located at the edge of the borough boundary, and they are also the area with low population and household density.

## Discussion
When doing the density analysis, this paper only considers the residential data. The incident does occur in the residential area and commercial, parks, and other places. Only considering the residential incidents will lead to overestimation of the response time. Comparing the service map with the density maps, service areas that needed more time to reach coincides with low population and household density.\
In this analysis, we assume there are only three factors (proximity to two facilities and land use condition) that impact a fire station's location selection. There are more to be considered. Also, different factors will have different importance to the selection. An example would be the station's distance to the nearest road or highway since time is critical in an emergency medical service. Facilities close to the highway with a higher speed limit would be able to respond to an incident faster./ 
Besides, we cannot determine the service area accurately due to the information missing about traffic congestion. In this paper, we use a walking model to do network analysis. In a real situation, traffic conditions like speed limits or congestion can impact the service area significantly.\
Moreover, the edge effect also impacts our result from network analysis. Other closer fire stations outside the study area cover the unserved areas or low service area. However, because we ignore their impact, these areas that were initially covered become unserved areas. Furthermore, when we using the data points within the study are to create a service map, the area mentioned above will require more time to reach from a different fire station inside the borough boundary.

## Conclusion
The goal of fire service is to prevent loss of life, poverty, and resources from incidents. Time is a critical factor in most cases. GIS is a powerful tool that helps optimize fire services. From our results, we can conclude that the current fire stations are located clustered around the Manhattan and Queen area in New York City. Two locations are suitable for building new facilities. One is 5.5 square kilometers large and locates in the southern Queen area. The other one locates in the Bronx with an area of 8 square kilometers. The network analysis shows a well-covered service map. The current station can reach an incident site within 4 minutes.\
However, this result only considers a small part of the factors that influence a fire station's location selection. The limitation mentioned above in the discussion will require a workable solution. Also, more consumer preference, policy legislation, and real-world implications will require further study in the future.







