## Purpose of Repository

This Jupyter Notebook was created by Peter Meleney on October 2, 2019.  It is meant to satisfy **Assignment A1: Data Curation** for course DATA 512: Human Centered Data Science at the University of Washington Master's of Science in Data Science (MSDS) program.

## Purpose of Assignment

From the DATA-512 Course Wikipedia page:

"The goal of this assignment is to construct, analyze, and publish a dataset of monthly traffic on English Wikipedia from January 1 2008 through August 30 2019. All analysis should be performed in a single Jupyter notebook and all data, documentation, and code should be published in a single GitHub repository.

The purpose of the assignment is to demonstrate that you can follow best practices for open scientific research in designing and implementing your project, and make your project fully reproducible by others: from data collection to data analysis."[1]

## Data Provenance
Raw data were gathered from the Wikimedia REST API, Wikimedia Foundation, 2018. CC-BY-SA 3.0.  See terms and conditions here: https://www.mediawiki.org/wiki/REST_API#Terms_and_conditions.

Data for this project are stored on two different systems within the Wikimedia Foundation.  The first data source is the legacy so-called "pagecounts database" which "makes availabe the pagecounts aggregated per project from January 2008 through January 2016.  The main difference among pagecounts and the current pageview data is lack of filtering of self-reported bots, thus automated and human traffic are reported together [in the pagecount database]."[2] 

## API Documentation
**Pagecounts**: https://wikitech.wikimedia.org/wiki/Analytics/AQS/Legacy_Pagecounts  
**Pageviews**: https://wikitech.wikimedia.org/wiki/Analytics/AQS/Pageviews  

Values of fields in cleaned_data file en-wikipedia_traffic_200712-201809.csv:  
**Year**: the year for which the counts are applicable.  
**Month**: the month for which the counts are applicable.  
**pagecount_all_views**: the number of views of all services from the pagecount API, this includes both self-reported bot and human views.  
**pagecount_desktop_views**: the number of views of the desktop services from the pagecount API, this includes both self-reported bot and human views.  
**pagecount_mobile_views**: the number of views of the mobile services from the magecount API, this includes both self-reported bot and human views.  
**pageview_all_views**: the number of views of all services from the pageview API, this includes only human views and does not include self-reported bots.  
**pageview_desktop_views**: the number of views of desktop services from the pageview API, this includes only human views and does not include self-reported bots.  
**pageview_mobile_views**: the sum of the views from the mobile-app and mobile-web services from the pageview API, this includes only human views and does not include self-reported bots.  

## Special Considerations
On occasion the APIs will malfunction and return 0 or null values for counts or views that should have values greater than zero.  If you see such values and the figure constructed by your notebook conflicts with the plot that is available through this repository, consider running the data gathering part of the jupyter notebook again to see if this resolves the issue.

## References:
[1] Morgan, Johnathan T. (2019, October 1)  Human Centered Data Science (Fall 2019)/Assignments.  Retrieved from: https://wiki.communitydata.science/Human_Centered_Data_Science_(Fall_2019)/Assignments, accessed on October 2, 2019.

[2] (27 June 2018) Analytics/AQS Legacy Pagecounts. Retrieved from: https://wikitech.wikimedia.org/wiki/Analytics/AQS/Legacy_Pagecounts, accessed on October 2, 2019.
