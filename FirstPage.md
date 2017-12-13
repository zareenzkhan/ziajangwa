

![GitHub Logo](/header.jpg)

# Background and Motivation
Our project is motivated by the following facts: 
- Flight delays are an issue for many business and official travellers. Airlines earn bad reputation for being unreliable due to delays. Based on the data, we want to explore whether these reputations are deserved. 
- There is extensive US official data on the topic of flight delays. For each of these flight, information such as date, weather conditions, airline carrier, departure and arrival airports are freely available.
- Numerous charts can be plotted to understand the statistics of airlines or airports to predict their performance.

# Data
We have used four different data sources
1. The official flight database for every domestic flight in the US 

2. Historical weather data

3. Airport information like names

4. Information about aircraft models
  
Since 1987 the U.S. Department of Transportation (US DOT) collects a huge amount of domestic flight data. This dataset, containing many different features (e.g. timestamp, origin, destination, airline, delays, etc.), is publicly available on their website. The tool on their website allows for downloading a customized dataset based on selected features and a specific time period. Each month there are more than 400,000 recorded flights, so we have to deal with very big datasets. 

For this project, we decided to focus mostly on the 2014 data since otherwise the dataset was just far too large. We were also able to connect this dataset with external weather data. 

Many of us have experienced it before: a flight is delayed because there are some lastminute repairs or other problems with the aircraft. We are curious if the manufacturer or the age of the aircraft influences the probability of delays. Therefore we need more detailed data about the flight. The flight's tail number is comparable to car license plates and helps us to identify the manufacturer and age of the airplane.We can get this information from the Federal Aviation Administration. This institution has a database of tail numbers (so called N-Numbers) for each aircraft in the US and also publishes other datasets with information about the respective aircraft (e.g. manufacturer of turbines, owner, etc.). We downloaded the database from their website. 

In addition, we need the exact geolocations for the airports in the dataset, for example to get good visualizations using Tableau Public or other maps. Furthermore, airport names would be helpful to interpret the data (the original dataset just contains the short IATA abbreviations). This data can be easily found online as csvs (see their website). 

A natural cause for many delays seems to be the weather. We decided to include weather data additionally in our analysis. Therefore, we wanted to get historical weather information of the airports. Unfortunately, when it comes to weather data, we couldn't find any public available sources that provide a suitable (free) dataset. However, Wunderground provides a webinterface allowing to query specific IATA / IAOC codes of airports (see i.e. their website). Writing a script allowed us to get historic data of individual airports. 


![First Image](/flight_data.png)
![Image](/flight_datacancel.png)
![Image](/flight_datacancel1.png)
![Image](/flight_datacancel2.png)
![Image](/flight_datacancel3.png)
![Image](/flight_dataLR1.png)
![Image](/flight_dataLR2.png)
![Image](/flight_dataLR3.png)
![Image](/flight_dataLR4.png)
![Image](/flight_dataLR5.png)
![Image](/flight_dataLR6.png)
![Image](/flight_dataLR7.png)
![Image](/flight_datarating1.png)
![Image](/flight_datarating2.png)
![Image](/flight_datarating3.png)
![Last Image](/Plot_1.png)
