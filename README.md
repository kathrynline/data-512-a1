# data-512-a1
## Description
This repository contains data and code for assignment 1 of DATA 512, Autumn 2021.
It was created by Emily Linebarger (elineb@uw.edu) in October 2021. 

## Setup
This work was done using a jupyter notebook, and packages were managed using a conda environment. Exact package versions have been saved in the file 'requirements.txt' in the root of the repository. 

## Data access
All data used in this project are accessed through the Wikimedia REST API. Terms and conditions can be found here: https://www.mediawiki.org/wiki/Wikimedia_REST_API#Terms_and_conditions

The Wikipedia Pageviews API is documented here: https://wikitech.wikimedia.org/wiki/Analytics/AQS/Pageviews
The Wikipedia Pagecounts API is documented here: https://wikitech.wikimedia.org/wiki/Analytics/AQS/Legacy_Pagecounts

## Codebook
The final data prepared for visualization has the following columns:
* 'year': Year of website traffic.
* 'month': Month of website traffic. 
* 'pagecount_all_views': Total views recorded through the Pagecounts API during this time period. This is a sum of mobile site and desktop views.
* 'pagecount_desktop_views': Total views recorded on the desktop site through the Pagecounts API during this time period.
* 'pagecount_mobile_views': Total views recorded on the mobile site through the Pagecounts API during this time period. 
* 'pageview_all_views': Total views recorded through the Pageviews API during this time period. This is a sum of desktop, mobile site, and mobile app views.
* 'pageview_desktop_views': Total views recorded on the desktop site through the Pageviews API during this time period. 
* 'pageview_mobile_views': Total views recorded on the mobile site or mobile app through the Pageviews API during this time period.   

## Notes/Special considerations
These data are filtered to organic user traffic (agent=user) in the Pageviews data. This option was not available in the Pagecounts API. 
NAs are removed from raw data and replaced with zeroes for analysis. A NA value in a row indicates that that data collection method was not available during that time period. 
