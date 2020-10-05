# README

## Goal
The goal of this project is to gather, process and analyze the pageviews information for english wikipedia from 2008 to current.

In order to measure Wikipedia traffic from 2008-2020, we will need to collect data from two different API endpoints, the Legacy Pagecounts API and the Pageviews API.

1. The Legacy Pagecounts API ([documentation](https://wikitech.wikimedia.org/wiki/Analytics/AQS/Legacy_Pagecounts), [endpoint](https://wikimedia.org/api/rest_v1/#!/Pagecounts_data_(legacy)/get_metrics_legacy_pagecounts_aggregate_project_access_site_granularity_start_end )) provides access to desktop and mobile traffic data from December 2007 through July 2016.
2. The Pageviews API ([documentation](https://wikitech.wikimedia.org/wiki/Analytics/AQS/Pageviews), [endpoint](https://wikimedia.org/api/rest_v1/#!/Pageviews_data/get_metrics_pageviews_aggregate_project_access_agent_granularity_start_end)) provides access to desktop, mobile web, and mobile app traffic data from July 2015 through last month.


To use the data, we need to agree to Wikimedia's [Terms of Use](https://wikimediafoundation.org/wiki/Terms_of_Use) and [Privacy Policy](https://wikimediafoundation.org/wiki/Privacy_policy). 
Content accessed via this code is licensed under the [CC-BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/) and [GFDL](https://www.gnu.org/copyleft/fdl.html) licenses, and you irrevocably agree to release modifications or additions made through this API under these licenses. See https://www.mediawiki.org/wiki/REST_API for background and details.

### Wikimedia endpoint terms of service and license

[Terms of service](https://wikimediafoundation.org/wiki/Terms_of_Use)

[the Wikimedia Services team - Website](http://mediawiki.org/wiki/REST_API)

[Software available under the Apache 2 license](http://www.apache.org/licenses/LICENSE-2.0)

## Data description

The main dataset is `en-wikipedia_traffic_200712-202008.csv`
It contains page view information for wikipedia from January 2008 to September 2020
Below are the columns in the csv

| **Column**                  | **Value**     | **Data type** | **Description**                                                  |
| ----------------------- | --------- | --------- | ---------------------------------------------------------------- |
| year                    | YYYY      | int       | This contains the year of the page views                         |
| month                   | MM        | int       | This contains the month for the page views                       |
| pagecount_all_views     | num_views | double    | total pageviews for all access types using legacy pagecounts api |
| pagecount_desktop_views | num_views | double    | total pageviews for desktop using legacy pagecounts api          |
| pagecount_mobile_views  | num_views | double    | total pageviews for mobile using legacy pagecounts api           |
| pageview_all_views      | num_views | double    | total pageviews for all access types using new pageviews api     |
| pageview_desktop_views  | num_views | double    | total pageviews for desktop using new pageviews api              |
| pageview_mobile_views   | num_views | double    | total pageviews for mobile using new pageviews api               |


## Known Issues/Special Considerations

- The data from the Pageview API excludes spiders/crawlers, while data from the Pagecounts API does not.
- There is 1 year of overlapping data between the 2 APIs
- The data from mobile web and mobile app for the pageviews api is combined into a single mobile views count
