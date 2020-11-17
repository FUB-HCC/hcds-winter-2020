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

Raw data as json files under "data_raw" as well as cleaned dataset as csv under "data_clean".
  
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
