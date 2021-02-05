## Introduction

Real estate development, or property development, is a business process, encompassing activities that range from the renovation and re-lease of existing buildings to the purchase of raw land and the sale of developed land or parcels to others. Real estate developers are the people and companies who coordinate all of these activities, converting ideas from paper to real property.[1] 

This project is designed to help starting companies, or small investors, identify properties of interest in order to maximize their potential gains and kick start their portfolio with great trajectory.

## Methodology

Using zillows dataset to perform an analysis of the housing market across the united states and target specific zone for time series analysis - ARIMA modeling.
  

## Exploring the Data

Through rigorous data exploration, the objective was to identify key areas to which yeilded the highest percentages of growth. 

#### United States growth map

The graph below shows the percent change for each state from 1996 to 2018

![image.png](pic_1.png)

After inspection on the nations map, the targeted area to focus on is identified as New York City.  A similar analysis was performed on the zillow data set for the 5 boroughs of NYC.  Below is a map showing the overall growth of these boroughs from 1996 to 2018 and their trends:

![image.png](pic2.png)

![image.png](pic8.png)

In order to identify which zip codes to target for the modeling process, the data is split from by borough to by zipcodes within the boroughs.  From the map below one may notice the following:
1.  Manhattan zip codes are limited with data.  Manhattan will be excluded from the analysis as it is typically over developed and very expensive.
2.  Locations around highly upcoming neighborhoods, such as near the Barclay have shown great growth.
3.  The areas of interest are those zipcodes just outside the zone of rapic growth.

![image.png](pic3.png)

Targeted areas to invest in:

![image.png](pic4.png)


## The Model



#### ARIMA Model

The arima Model was used to train the model, the model performed well with the following results:


## Conclusion

The key top features used to determind if a water well is functional are:
* LGA
* Region
* Payment
* Management
* Population
* Age

## Future Work

#### Improving model accuracy

Introducting external data to the dataset

* Incorporating future construction project into the model to predict how large-scale investments into an area can affect housing prices.
* Current dataset does not include how the COVID-19 has impacted the market, extend dataset to more recent timeframes for analysis.
* Adding additional external data to the model, ie number of permits issued by NYC DoB
 
* Natural disaster data - Earthquakes, floors, droughts

#### Multiclassification Model
To provide future finance allocation by predicting timeframes a well may need repair or how to increase the probability of a long lasting water well for future construction projects.


#### References
 1. Frej, Anne B; Peiser, Richard B. (2003). Professional Real Estate Development: The ULI Guide to the Business (2 ed.). Urban Land Institute. 






