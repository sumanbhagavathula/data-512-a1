# Introduction
This repository contains code and documentation to retrieve and plot monthly page views for the English wikipedia from July 1 2008 through September 30 2017. The goal is to have the steps in a reproducible research format so any reader can be able to follow along and reproduce the results of this analysis, which is similar to the following graph: https://wiki.communitydata.cc/File:PlotPageviewsEN_overlap.png.

# Copyright and Licensing
NOTE: the code, data and text of this repository are governed by the MIT License included in the [LICENSE file](https://github.com/sumanbhagavathula/wikipediapageviews/blob/master/LICENSE) and [CC BY-SA](https://creativecommons.org/licenses/by-sa/4.0/legalcode)

The data and images are also available under the [Creative Commons BY-SA](https://creativecommons.org/licenses/by-sa/4.0/)

# Overview
For this work, Wikipedia traffic data from two different [Wikimedia REST API endpoints](https://www.mediawiki.org/wiki/REST_API) are combined into a single dataset, some simple data processing steps are performed on the data, and then that data is analyzed.

Below are additional details about these Wikimedia endpoints which expose the Wikipedia traffic from 2008-2016:

1. The legacy **Pagecounts API** ([documentation](https://wikitech.wikimedia.org/wiki/Analytics/AQS/Legacy_Pagecounts), [endpoint](https://wikimedia.org/api/rest_v1/#!/Pagecounts_data_(legacy)/get_metrics_legacy_pagecounts_aggregate_project_access_site_granularity_start_end)) provides access to desktop and mobile traffic data from January 2008 through July 2016.

2. The **Pageviews API** ([documentation](https://wikitech.wikimedia.org/wiki/Analytics/AQS/Pageviews), [endpoint](https://wikimedia.org/api/rest_v1/#!/Pageviews_data/get_metrics_pageviews_aggregate_project_access_agent_granularity_start_end)) provides access to desktop, mobile web, and mobile app traffic data from July 2015 through September 2017.

## Description of the process
The end to end process of this analysis work is broken down into three steps:

1. Data Acquisition
2. Data Processing
3. Analysis and Visualization

To facilitate ease of reproducing this work from any of the steps above and ability to skip any previous steps at any stage, each of these steps is performed and included in separate jupyter notebook files, and the results from each of the phases is stored in this repository for offline view and input to subsequent steps if required. This also is helpful if at any time during the reproducing effort the API endpoints become unavailable for any foreseen or unforeseen reasons. 

## File structure
The source code, data (raw and processed) and the final visualization can be found in the following structure:

### Source
1. [Data Acquisition](https://github.com/sumanbhagavathula/wikipediapageviews/blob/master/src/englishwikipediatrafficanalysis_dataacquisition.ipynb)
2. [Data Processing](https://github.com/sumanbhagavathula/wikipediapageviews/blob/master/src/englishwikipediatrafficanalysis_dataprocessing.ipynb)
3. [Analysis and Visualization](https://github.com/sumanbhagavathula/wikipediapageviews/blob/master/src/englishwikipediatrafficanalysis_visualization.ipynb)

### Data
1. [Raw Data](https://github.com/sumanbhagavathula/wikipediapageviews/tree/master/src/data/raw) contains five JSON files and has the monthly traffic data for each of the different access-type types.
2. [Processed Data](https://github.com/sumanbhagavathula/wikipediapageviews/tree/master/src/data/processed) is a csv formatted processed data that has the combined monthly traffic data from all the different raw files.
3. [Visualization](https://github.com/sumanbhagavathula/wikipediapageviews/tree/master/src/data/visualization) contains a copy of the final visualization produced as part of this analysis which looks like below:

![alt text](https://github.com/sumanbhagavathula/wikipediapageviews/blob/master/src/data/visualization/en-wikipedia_traffic_200801-201709.jpg)






