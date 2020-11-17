# A2-hcds-hcc-xiyu
HCDS Assignment 2

# Goal of project

The project is aimed to acquire user traffic on Wikipedia of english version visualize the user traffic with time series plot.

# Data description
The data is collected from:
1. The Legacy Pagecounts API (documentation, endpoint/get_metrics_legacy_pagecounts_aggregate_project_access_site_granularity_start_end)) provides access to desktop and mobile traffic data from December 2007 through July 2016.
2. The Pageviews API (documentation, endpoint) provides access to desktop, mobile web, and mobile app traffic data from July 2015 through last month.

> The data description is from original discription from Jupyter Assignment

# Project Structure and Main Steps
The detailed data processing and visualization process can be found in Jupyter Notebook named A2_ReproducibilityWorkflow.

The process consists of three main stage:
1. Data Acquisition.
1. Data Processing.
1. Data Analysis.

## Data Acuisition:
The data used in this workflow is acquired through APIs (mentioned in data description) and are written as 5 seperate JSON format. The data source are seperated based on access type (desktop, mobile) and the APIs.

## Data Processing
The data are loaded from json files and need to be converted into a general dataframe with essential parameters.

The main processings are:
1. For data collected from the Pageviews API, combine the monthly values for mobile-app and mobile-web to create a total mobile traffic count for each month.
1. For all data, separate the value of timestamp into four-digit year (YYYY) and two-digit month (MM) and discard values for day and hour (DDHH).

> Description from original description on Jupyter Assignment.

<br/>![image](https://github.com/FUB-HCC/hcds-winter-2020/blob/main/assignments/A2_ReproducibilityWorkflow/xiyu/Page%20Views%20on%20English%20Wikipedia.png)

The processed data is stored in a csv file with 8 attributes:

* year: 
<br/> In which year were the scored user traffics taken place. Extracted from timestamp parameter from original data in JSON file.
* month:
<br/> In which month were the scored user traffics taken place. Extracted from timestamp parameter from original data in JSON file.
* pagecount_all_views: <br/> Pagecount traffics in all, including from desktop as well as from mobile.Accessed through pagecount API.
* pagecount_desktop_views: <br/> Pagecount traffics from desktop as access-type.
* pagecount_mobile_views: <br/> Pagecount traffics from mobile as access-type.
* pageview_all_views: <br/> Pageview traffics in all, including from desktop as well as from mobile.Accessed through pageview API.
* pageview_desktop_views: <br/> Pageview traffics from desktop as access-type.
* pageview_mobile_views: <br/> Pageview traffics from mobile as access-type, including from mobile-web as well as from mobile-app (preprocessed before).

## Data Analysis and Visualization

In this stage, a time series plot of user traffics from different access type are depicted as line chart.

We are interested in three metrics: desktop traffic, mobile traffic and all traffic, regardless of APIs. Therefore, the csv file is loaded as dataframe and data processing for metrics and scaling (Y-axis in billion) are taken place before the visualization.







