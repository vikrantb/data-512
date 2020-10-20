# Bias in Data
1 README file in .txt or .md format that contains a brief summary of the assignment goals, and links to the Figshare datasets, the Detox wiki page, and the Perspective API repository on GitHub.

## Goal
The goal of this project is to identify what, if any, sources of bias may exist in various Wikipedia talk corpus datasets, and to develop testable hypotheses about how these biases might impact the behavior of machine learning models trained on the data, when those models are used for research purposes or to power data-driven applications. 

Google data scientists used these [annotated datasets](https://figshare.com/projects/Wikipedia_Talk/16731) to train machine learning models as part of a project called Conversation AI. The models have been used in a variety of software products and made freely accessible to anyone through the Perspective API. 

As part of this assignment project, we want to study these datasets and try to identify potential biases or potential unintended negative consequences.

## Data Citations

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

| **Column**              | **Value** | **Data type** | **Description**                                                  |
| ----------------------- | --------- | ---------     | ---------------------------------------------------------------- |
| year                    | YYYY      | int           | This contains the year of the page views                         |
| month                   | MM        | int           | This contains the month for the page views                       |
| pagecount_all_views     | num_views | double        | total pageviews for all access types using legacy pagecounts api |
| pagecount_desktop_views | num_views | double        | total pageviews for desktop using legacy pagecounts api          |
| pagecount_mobile_views  | num_views | double        | total pageviews for mobile using legacy pagecounts api           |
| pageview_all_views      | num_views | double        | total pageviews for all access types using new pageviews api     |
| pageview_desktop_views  | num_views | double        | total pageviews for desktop using new pageviews api              |
| pageview_mobile_views   | num_views | double        | total pageviews for mobile using new pageviews api               |


## Known Issues/Special Considerations

- The data from the Pageview API excludes spiders/crawlers, while data from the Pagecounts API does not.
- There is 1 year of overlapping data between the 2 APIs
- The data from mobile web and mobile app for the pageviews api is combined into a single mobile views count
