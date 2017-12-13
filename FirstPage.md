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

# Exploratory Data Analysis

Following graph is showing the ratio between Cancelled and Not-Cancelled flights.
![Image](/flight_datacancel1.png)

We grouped flights according to dates to find out Cancelled and Not-Cancelled flights day-wise. 
Due to computation power issue, we have used small dataset.
![Image](/flight_datacancel2.png)

Now we mapped flights with respect to airline.
![Image](/flight_datacancel3.png)

We plot following graph to show number of flights are getting cancelled for all airlines. 
![Image](/flight_datarating1.png)

We plot following graph to show number of flights are getting delayed for all airlines. 
![Image](/flight_datarating3.png)

Following graph is showing count of all on-time flights, delay between 5 to 45 mins and above 45 mins for all the airlines.
![Image](/flight_datarating2.png)

# Prediction
Most of the time it happens that if a flight experience any delay in its departure, it will not be able to reach timely on the destination. So we picked it up as our objective to predict the delay in arrival if the flight is delayed on departure.

## Model 1
We use **Linear Regression Model** to do the prediction.

## Implementation
In this model we used SCHEDULE_TIME to predict ARRIVAL_DELAY.

## Results
Score on training data is 0.81
Score on test data is 0.81

![Image](/flight_dataLR1.png)

## Model 2
We use **Multiple Linear Regression Model** to do the prediction.

## Implementation
1. We first find out the duration of flight by using two features, SCHEDULE_DEPARTURE and SCHEDULE_ARRIVAL.
2. Other parameters which we already have in our dataset the DEPARTURE_DELAY and SCHEDULE_TIME.
3. We applied the model on dataset then to predict ARRIVAL_DELAY.

## Results
After executing the model, we were able to find the ARRIVAL_DELAY for every flight which we then compared with the ARRIVAL_DELAY already given in our dataset and we came to know that our prediction was nearly equals to the delays already given in the dataset which means our prediction model is fairly good.

![Image](/flight_dataLR2.png)

## Model 3
We use **Logistic Regression Model** to do the prediction. 

## Implementation
We classified our data in this model into two categories DELAYED and NOT-DELAYED using DEPARTURE_DELAY and ARRIVAL_DELAY columns from our dataset.

## Results
Accuracy on training data is 0.96
Accuracy on test data is 0.94

![Image](/flight_dataLR4.png)

We buildup confusion matrix to identify true positive and true negative values for NOT_DELAYED flights.

![Image](/flight_dataLR3.png)

## Model 4
We use **Support Vector Machine** to do the prediction. 

## Implementation
We classified our data in this model into two categories DELAYED and NOT-DELAYED using DEPARTURE_DELAY and ARRIVAL_DELAY columns from our dataset. By implenting this model, we actually want to figure out which model's prediction is more accurate, either SVM or Logistic regression.

## Results
Accuracy on training data is 0.97
Accuracy on test data is 0.94

![Image](/flight_dataLR4.png)

We buildup confusion matrix to identify true positive and true negative values for NOT_DELAYED flights.

![Image](/flight_dataLR5.png)

## Model 5
We use **Logistic Regression Model** and **Multinomial Logistic Regression Model** to predict reason of delay and compared these models results. 

## Implementation
We have 4 different delays given in our dataset which are AIR_SYSTEM_DELAY, LATE_AIRCRAFT_DELAY, WEATHER_DELAY and AIRLINE_DELAY. by using these models, we tried to predict the delay reason for each flight.

## Results
Accuracy of Logistic Regression on training data is 0.92
Accuracy of Logistic Regression on test data is 0.90

Accuracy of Multinomial Logistic Regression on training data is 0.93
Accuracy of Multinomial Logistic Regression on test data is 0.91

![Image](/flight_datadelay.png)

Following graph is showing which airline flight is delayed due to which reason.
![Image](/flight_dataLR7.png)

![Image](/flight_dataLR6.png)







