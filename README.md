# artistic-funding-and-employment-baltimore
This study analyzes how the amount of artistic funding in a Baltimore neighborhood impacts the number of employed creative people.

## Background

Baltimore is home to a thriving arts community. Institutions like the Maryland Institute College of Art and programs like Artscape have propelled the city to the [#10 spot of the nation’s top arts destinations.](https://www.greaterbaltimore.org/news/blog/importance-arts-economic-development). Proponents of these programs [argue](https://www.baltimoresun.com/opinion/op-ed/bs-ed-mica-hoi-20151227-story.html) that art can promote community cohesion, foster character growth in young people, and beautify neighborhoods. Given the strength of the Baltimore arts economy and its benefit to communities, we should investigate what conditions this sector thrives under and how resources are currently being distributed. Considering that [most arts businesses are small businesses](https://www.arts.gov/stories/blog/2020/taking-note-monitoring-role-freelancers-and-small-businesses-arts-economy-and-early-signs-covid-19), we should also investigate Baltimore’s small business economy.

## Business Questions

What is the relationship between small business funding and the number of young, small businesses in Baltimore? 

What is the relationship between small business funding and the arts employment rate in Baltimore? How does this relationship vary between neighborhoods? 

## Datasets

All data was taken from Baltimore City Open Data. They can be downloaded from our GitHub repository under the [Datasets](https://github.com/vchen19/artistic-funding-and-employment-baltimore/tree/main/Datasets) folder, or found at the following links: 

[Total Dollar Amount Invested in Small Businesses per 50 Businesses](https://data.baltimorecity.gov/datasets/bniajfi::total-dollar-amount-invested-in-small-businesses-per-50-businesses?geometry=-77.142%2C39.192%2C-76.099%2C39.378&page=6&selectedAttribute=Shape__Length)

This data gives the total dollar amount invested in small businesses per 50 businesses in every community statistical area in Baltimore for the years 2016 through 2019.

[Percent of Businesses that are 2 Years old or less](https://data.baltimorecity.gov/datasets/bniajfi::percent-of-businesses-that-are-2-years-old-or-less-1?geometry=-77.142%2C39.192%2C-76.099%2C39.378)

This data gives the percent of businesses in every community statistical area in Baltimore that are 2 years old or less for the years 2010 through 2019. 

[Total Employment in Arts Related Businesses](https://data.baltimorecity.gov/datasets/bniajfi::total-employment-in-arts-related-businesses/data?page=2)

This data gives the number of employed persons in arts related businesses in every community statistical area in Baltimore for the years 2010 through 2018. 

[Total Population - Community Statistical Area](https://data.baltimorecity.gov/datasets/bniajfi::total-population-community-statistical-area/data?geometry=-77.142%2C39.192%2C-76.099%2C39.378&selectedAttribute=tpop10)

This data gives the population of each community statistical area from the 2010 Census. Though we generally look at data from 2016 in this study, the Census only occurs every 10 years and 2020 Census data has not yet been released, so this population data is the most up to date data we have.

The map of Baltimore City community statistical areas was screenshotted from [this website](https://health.baltimorecity.gov/neighborhoods/neighborhood-health-profile-reports), and can also be found under the Datasets folder in this respository.

## Methods

Detailed methods for linear regression, [cluster analysis](https://github.com/vchen19/artistic-funding-and-employment-baltimore/blob/main/cluster_analysis_methods.md.md), and [geospatial analysis](https://github.com/vchen19/artistic-funding-and-employment-baltimore/blob/main/geospatial_analysis_methods.md) can be found in our GitHub repository.

Generally speaking, linear regression analysis was conducted to find the relationship between small business funding and the number of new small businesses in the year 2016. Then, linear regression analysis was conducted to find the relationship between small business funding and the share of the population that is employed in arts-related businesses in the year 2016. Then, cluster analysis was conducted to group Baltimore's community statistical areas (CSA's) into categories based on their small business funding and their arts employment. Finally, geospatial analysis was conducted based on this cluster analysis to visualize where the clusters lie in Baltimore.

## Results

### Linear Regression

### Cluster Analysis

![Cluster Characteristics Table](https://github.com/vchen19/artistic-funding-and-employment-baltimore/blob/main/Cluster%20Characteristics%20Table.png)
![Cluster Characteristics Bar Graph](https://github.com/vchen19/artistic-funding-and-employment-baltimore/blob/main/Cluster%20Characteristics%20Bar%20Graph.png)
![Cluster Frequency](https://github.com/vchen19/artistic-funding-and-employment-baltimore/blob/main/Frequency%20of%20Clusters.png)


The cluster analysis returned Washington Village/Pigtown, Inner Harbor/Federal Hill, Glen-Falstaff, and Downtown/Seton Hill as the four clusters. The first cluster had relatively high arts employment and relatively high investment/ business; the second had high arts employment and high investment/ business; the third cluster had relatively low arts employment and relatively low investment/ business; and the fourth cluster had high arts employment and low investment/ business. 13 CSA's, or neighborhoods, fell into the first cluster, 1 into the 2nd, 40 into the 3rd, and 1 into the 4th. 

### Geospatial Analysis
![Geospatial Analysis](https://github.com/vchen19/artistic-funding-and-employment-baltimore/blob/main/Geospatial%20Analysis.png)

## Discussion

From this data, we can resonably conclude that small business funding has a greater impact on arts employment than it does on the small business economy as a whole. Proponents of arts programs could use this data to suggest that because small business funding is most effective in arts businesses in particular, more funding should be directed toward the arts in order to target sectors that will return the greatest investment. A limitation of this study is that it is perhaps an uneven comparison to make to compare arts employment with the number of small businesses that pop up. In the future, we should look to reduce variability between these two factors and compare, for example, arts employment to general small business employment.

Additionally, we can see that funding and employment is rather disparately distributed throughout Baltimore, with the vast majority (40, 72.7%) of neighborhoods falling into cluster 3 with low arts employment and low small business funding. Meanwhile, only 14 (25.4%) of neighborhoods receive high funding and high employment. In the geospatial visualization of this data, we can visually see that most of the resources are distributed in South and Central Baltimore, with not as much in West Baltimore and Northeast Baltimore. The one neighborhood with extremely high employment and small business funding was Inner Harbor/ Federal Hill. We know that Inner Harbor/ Federal Hill is [one of the wealthiest neighborhoods in Baltimore](https://data.baltimorecity.gov/datasets/bniajfi::percent-of-households-earning-more-than-75000-community-statistical-area-1/data?geometry=-77.142%2C39.192%2C-76.099%2C39.378&orderBy=hhm7517&page=6), ranking 4th highest in percent of households earning more than $75,000 in 2013-2017. Thus, we can make the argument that resources need to be distributed more evenly throughout Baltimore, especially since arts programs and businesses can have such a positive impact on communities.

Future studies could analyze the movement of funds and employment throughout Baltimore through the years. We observed stark changes in arts employment in certain years, so more research should be done into why this happens and what impact it has on communities. Additionally, once 2020 Census data is released, this study could be conducted again with 2020 data in order to more accurately predict the share of the population that is employed in the arts.


