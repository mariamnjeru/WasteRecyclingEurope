# Waste generation and recycling: An overview in Europe.

This project clusters European Countries according to their waste generation and recycling trends from 2010-2020 ( Check out the Tableau+ workbook 🙂) in order to to understand the waste generation and recycling scene in European countires and their evolution overtime.


## Research questions:


1.   What are the geographical and time trends for waste generation and recycling in Europe? What is behind them? (Using Tableau, workbook included)

2.   What groups do the different countries cluster form based on waste generation and recycling? What are the similarities/differences in their trends?

## Content of the files:
1.   A tableau workbook where the spatial and time trends analysis are visualized. The result of it is an interactive map of european countries represent the number of recycling facilities there with time trends for waste gerneration and recycling.

2.  A jupyter notebook where the report and other steps are provided in Python.
   
3.  The final presentation of the project as a pdf.

## Datasets:
The datasets used for the analysis are the following:

* Waste generation dataset: Waste generation for all types of waste excluding major mineral waste. Information available for 38 countries. In kilogram per capita .For periods of two years from 2004 to 2020. Source: Eurostats
* Watse recycling dataset: Waste recycling for all types of waste excluding major mineral waste. Information available for 32 countries. In kilogram per capita .For periods of two years from 2004 to 2020. Source: Eurostats,
* Recycling facilities dataset: Number of recycling facilities in european countries. Information available for 28 countries for periods of two years from 2010 to 2020. Source: Eurostats

## Analysis and results:
1. Data Cleaning and preprocessing:
   * The three datasets covered different number of countries based on the definition of the european countries and the information available.
   * Only the countries that had information in the three datasets were kept (28). The information for the whole european union was excluded as well as we found irrelevant to our goals.
   * Handling outliers: values that are more than 2 standard deviation away from the mean.
     ![image](https://github.com/RandFa/WasteGenerationandRecycling/assets/62840736/f0a74c5d-8ca0-4c98-a0b1-8a1802b449a8)
   * 26 overall missing values + outliers
   * Missing values: Predicted using imputing 
   * Multivariate feature imputation:  models each feature with missing values as a function of other features, and uses that estimate for imputation.
   * It takes into account similar rows (neighbors = 2)
3. Studying geographical and Time trends using Tableau:
   - Germany came first in the number of recycling facilities between 2020 and 2022 followed by Italy, UK, and Spain.
   ![image](https://github.com/RandFa/WasteGenerationandRecycling/assets/62840736/cf8a8285-e2e7-4c8a-aba9-78d3d8288999)
   ### Germany:
   * Steady rate for generation and recycling over the year although several policies to reduce waste were implemented throughout the year.
   * Export a lot of waste, especially to China before the ban in 2019.
     ![image](https://github.com/RandFa/WasteGenerationandRecycling/assets/62840736/54fbb3a5-3184-4196-8388-0f5d6303abf3)
   ### Italy:
   * The first waste prevention program (WPP) in Italy came into force in 2013, and waste generation dropped in the following year but increased in the years that followed.
  
     ![image](https://github.com/RandFa/WasteGenerationandRecycling/assets/62840736/26116baa-74eb-4b7f-ad35-25caa29cbf9a)
   ### Spain:
   * Waste generation was decreasing and reached its lowest point at 2014, which is linked to the global financial crisis. 
   * There was a decrease in GDP in the last few years, it reached in 2020 the same level as 2012.
     ![image](https://github.com/RandFa/WasteGenerationandRecycling/assets/62840736/eafa9634-b9f5-4080-ba17-532432001a0a)
3. Clustering:
   ###  Based on correlation using clustered  heatmaps:
      * Based on waste generation we got these three clusters: Cluster 1: alternating periods of increase and decrease in waste generation.Cluster 2: A steady high increase in waste generation over the years. Cluster 3:  increase in waste generation from 2010-2018 and then slight decrease.
  
        ![image](https://github.com/RandFa/WasteGenerationandRecycling/assets/62840736/c0fbb4ba-bf61-4ef9-a6eb-08873d73992b)
      * Based on waste recyling, we got these 4 clusters: Cluster 1: steady recycling rate with a small drop at 2014. Cluster 2: steady recycling rate. Cluster 3:  increase in waste recycling over the time period. Cluster 4: steady recycling with a slight drop at 2016.
           ![image](https://github.com/RandFa/WasteGenerationandRecycling/assets/62840736/37d0b2a7-4d2e-486e-94e2-8edbca0a374e)

   ###  Unsupervised using knn algorithm:
      * The best unsupervised clustering for small data sets.
      * K = 3 for both waste generation and recycling based on the elbow methond.
      * The three clusters based on waste generation:
        ![image](https://github.com/RandFa/WasteGenerationandRecycling/assets/62840736/833bb15c-5a02-4973-89d6-c8684e416828)
      * The three clusters basedd on waste recycling:
        ![image](https://github.com/RandFa/WasteGenerationandRecycling/assets/62840736/8016b3ca-e1c5-4b3f-acf1-35baabf04aa5)
## Limitations:
* No clear characteristics for the KNN clusters.
* Not enough data to asses the KNN model
* Few data points
* Missing data and errors.
* Due to the freedom of the countries to choose their methods, sampling methods were used by some countries in some parts of the reporting tables. Sampling errors were not included in the report
* Due to the freedom of the countries to choose their methods the non-sampling errors are difficult to summarize at the European level
* The factors influencing the trends are not very clear, based on Eurostats reports, it is not correlated with GDP and population size.
## Perspectives:
* Analyse the waste data by categories eg Plastic packaging
* Combine the analysis with additional data like GDP.
## Help

Any advise for common problems or issues.
```
command to run if program contains helper info
```

## Authors

Contributors names and contact info

1. Rand Fatouh 
2. Mariam njeru


