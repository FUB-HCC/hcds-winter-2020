# Analysis of Wikipedia Traffic

This project aims to analyze Wikipedia Traffic by retrieving page view data from the English Wikipedia. 

## Index 

This repository contains the following elements:

### Jupyter Notebook for Analysis

A Jupyter Notebook explaining the data retrieval process as well as performing the analysis. 
The data is retrieved via Wikimedia APIs.   
Legacy Pagecounts as well as Pageviews are retrieved as json files.

Find more information here:  
Pagecounts: https://wikitech.wikimedia.org/wiki/Analytics/AQS/Legacy_Pagecounts  
Pageviews: https://wikitech.wikimedia.org/wiki/Analytics/AQS/Pageviews

### Data files

Cleaned dataset as csv file under [data_clean](https://github.com/FUB-HCC/hcds-winter-2020/tree/main/assignments/A2_ReproducibilityWorkflow/masc/data_clean/en-wikipedia_traffic_200712-202010.csv) as well as the raw data in [data_raw](https://github.com/FUB-HCC/hcds-winter-2020/blob/main/assignments/A2_ReproducibilityWorkflow/data_clean/) 

  
#### Description of the data:  
**Variables**
Views: Mobile or desktop views
Year: The year in which the traffic occured
Month: The month in which the traffic occured
Access: The device which accessed the data

### How to reproduce this research

Download the Jupyter Notebook for performing the Analysis.
Retrieve wikipedia traffic data via APIs or import the raw datasets in "data_raw"
Run the analysis
Plot the outcome

### How to use this code for conducting your own wikipedia traffic research

Download the Jupyter Notebook 
Retrieve wikipedia traffice data for the desired time period (change start and end date timestamps)
Run the analysis
Plot the outcome
