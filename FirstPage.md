![GitHub Logo](/header.jpg)

# Background and Motivation
Our project is motivated by the following facts: 
- Flight delays are an issue for many business and official travellers. Airlines earn bad reputation for being unreliable due to delays. Based on the data, we want to explore whether these reputations are deserved. 
- There is extensive US official data on the topic of flight delays. For each of these flight, information such as date, weather conditions, airline carrier, departure and arrival airports are freely available.
- Numerous charts can be plotted to understand the statistics of airlines or airports to predict their performance.

# Data
We have used data from different sources like
- The official flight database for every domestic flight in the US 

- Historical weather data

- Airport information like names
  
We picked the data from kaggle website. This is the data of U.S. Department of Transportation (US DOT) which have a huge amount of domestic flight data. This dataset, containing many different features (e.g. timestamp, origin, destination, airline, delays, etc.). We have customized the data as per our requirement. 

For this project, we decided to focus on the 2015. We were also able to connect this dataset with external weather data.  

A natural cause for many delays seems to be the weather. We decided to include weather data additionally in our analysis. Therefore, we wanted to get historical weather information of the airports. Unfortunately, when it comes to weather data, we couldn't find any public available sources that provide a suitable (free) dataset. We found a dataset which was a single day data, we mold it as per our requirement. 

# Prediction
It most of the time happens that if a flight experience any delay in its departure, it will not be able to reach timely on the destination. So we picked it up as our objective to predict the delay in arrival if the flight is delayed on departure.

## Model
We use **Linear Regression Model** to do this prediction.

## Implementation
1. We first had to find out the duration of flight by using two features, SCHEDULE_DEPARTURE and SCHEDULE_ARRIVAL.
2. Other parameter which we already have the DEPARTURE_DELAY in our dataset.
3. We applied the model on dataset then.

## Results
After executing the model, we were able to find the ARRIVAL_DELAY for every flight which we then compared with the ARRIVAL_DELAY already given in our dataset and we came to know that our prediction was nearly equals to the delays already given in the dataset which means our prediction model is fairly good.

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
