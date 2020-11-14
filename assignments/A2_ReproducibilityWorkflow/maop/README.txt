The goal of this project is to visualize the total amount of page views on Wikipedia. The needed data is being collected using the following APIs:

- Legacy Pagecounts API (for documentation see: https://wikitech.wikimedia.org/wiki/Analytics/AQS/Legacy_Pagecounts)

- Pageviews API (for documentation see: https://wikitech.wikimedia.org/wiki/Analytics/AQS/Pageviews

- For terms and condition of REST API see: https://www.mediawiki.org/wiki/Wikimedia_REST_API#Terms_and_conditions

- License of source data is available under the Creative Commons Attribution-ShareAlike License

All raw data drawn through this project is located in the following directory: "maop/raw_data/"

All clean data is saved to "maop/clean_data/" after processing

The result after executing the given code can be found under "maop/result"
The result directory includes an output graph which is a PNG export of the prior computation. The data used in this graph is also exported to: "maop/result/result_data.csv"


== Description of values in final data ==

result_data.csv consist of a five column table.

year -> The year extracted from timestamp in raw data

month -> The month extracted from timestamp in raw data

desktop_traffic -> The values in this column is the sum of total desktop traffic gained through Legacy and Pageviews for each month and each year starting from 2017/12. While Pageview provides an option to filter for 'user-access' only, it is to be expected, that the queried data includes bot traffic collected through the other API. NOTE: For time periods where the data is overlapping, the average is being computed.

mobile_traffic -> Represents the total mobile accesses including mobile-site and accesses through the mobile app. NOTE: For time periods where the data is overlapping, the average is being computed.

all_traffic -> Is simply the sum of desktop+mobile traffic.


== Miscellaneous ==

Pageview API excludes spiders/crawlers, while data from the Pagecounts API does not. When it comes to mobile_traffic, traffic generated via mobile-app access and mobile-site access has been taken into consideration.


== Made with love mvrc@github ==
