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

![image.png](pic_2.png)

![image.png](pic_8.png)

In order to identify which zip codes to target for the modeling process, the data is split from by borough to by zipcodes within the boroughs.  From the map below one may notice the following:
1.  Manhattan zip codes are limited with data.  Manhattan will be excluded from the analysis as it is typically over developed and very expensive.
2.  Locations around highly upcoming neighborhoods, such as near the Barclay have shown great growth.
3.  The areas of interest are those zipcodes just outside the zone of rapic growth.

![image.png](pic_3.png)

Targeted areas to invest in:
![image.png](pic_4.png)


## The Model

There are additional features used for the model. These features and the grouping of them are outlines below:

    * age: [5, 10, 15, 20, 30, 40, 60]
    * lga: [0.5,0.65]
    * ward: [0.4, 0.6]
    * payment: [0.6]
    * quantity: [0.6]
    * management: [0.6]
    * source: [0.65]
    * waterpoint: [0.6]
    * region: [0.5, 0.65]
    * district: [0.3, 0.4, 0.6]
    * extraction_type_class:[0.3]
    * population:[1]
    * installer': [0.45]
    * funder: [0.45]
    * water_quality: [0.65]
    
This method of binning these features is to group features of high percentages of functioning water wells into a class that will be used to increase the importance of that feature for predicting functioning wells.

#### XGBOOST Model

The XGBoost Model was used to train the model, the model performed well with the following resoluts:

* Training set score for SVM: 0.838361
* TestinG set score for SVM: 0.825926

#### Confusion Matrix

![image.png](https://github.com/NickCatalano14/dsc-mod-3-project-v2-1-onl01-dtsc-pt-052620/blob/926ba615ca7cfbad739699199600fa70c57b950e/conf_matrix.png?raw=true)


The part to highlight from the confusion matrixs is the recall of the functioning water wells.  A 92% recall for functioning wells indicates that of the functioning wells predicted, 92% of those are functioning.  This is critically important for a life support system such as providing clean water to those needing it.

#### Feature Importance

![image.png](https://github.com/NickCatalano14/dsc-mod-3-project-v2-1-onl01-dtsc-pt-052620/blob/926ba615ca7cfbad739699199600fa70c57b950e/feature_importance.png?raw=true)


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

* City data - Location, population
* Region poverty data
* Natural disaster data - Earthquakes, floors, droughts

#### Multiclassification Model
To provide future finance allocation by predicting timeframes a well may need repair or how to increase the probability of a long lasting water well for future construction projects.


#### References
 1. Frej, Anne B; Peiser, Richard B. (2003). Professional Real Estate Development: The ULI Guide to the Business (2 ed.). Urban Land Institute. 






