# DATA 512 - Project Plan

### Motivation
##### Background
Short-term rentals are getting popular and people have been considering short-term accommodations over hotels as an affordable
and convenient alternative. Various hosts open up their property for such short-terms and provide services.
Their listings are available online which can be browsed by customers before they opt for it.
It is very similar to hotels, but anyone can host their property even if it is a small place.
There is a lot of diversity in such short-term accommodations and their prices vary largely
due to the diverse sets of individual hosts and different types of property hosted.

##### Potential Impact
There are broadly two types of stakeholders - tenants who are either moving in to a new city or tourists who are visiting
a city for a considerable amount of time, and hosts who list their property on the short-term rentals.

Tenants and tourists moving to a new city would be very interested to know about the cost of living in the city.
Particularly, they might be interested to learn how the prices are distributed across different areas of a city.
Such information might help them plan their stay according to their budget and standard of living.
Also, they might be interested in knowing how the prices vary across different types of property like shared room, private room
or an entire house. This information provides transparency and granularity which might
help select appropriate listing based on the number of people and their budgets.

New hosts who are willing to list their property on short-term rental portals might be very interested to
set an appropriate price for their listing. Predicting prices based on the neighborhood,
and property type would be helpful to support these needs.
Also, if a host is planning to build a property to rent, they might be interested in knowing what type of property to build.
Understanding the distribution of types of property in a neighborhood might help hosts get an insight to make their decision.

### Data Description
Airbnb is one of the largest short-term rental providers which connects various hosts to customers on the
Airbnb portal where the listings provided by hosts can be opted by customers who browse the portal.
Hence, I would like to use the New York City Airbnb Open Data which provides details on Airbnb lists
and metrics in New York city for 2019 [[1](https://www.kaggle.com/dgomonov/new-york-city-airbnb-open-data)]
till 07 Jun 2019 (since 27 March 2011). The dataset contains 49,080 Airbnb listings across 5 different
neighbourhood groups in New York City along with the listing title, geographic location,
neighbourhood (area and wider region), type of property (entire house, private room or shared room),
minimum nights for booking and price. It also contains some traffic information like the number of
days when the listing was available for booking in a year, the number of reviews per month, and
the date of the latest review. This dataset contains a large number of listings in one of the more
populated cities in the US along with the above-mentioned attributes which makes this dataset very relevant for this problem.
Example of values and the attributes present in the data are listed in the table below.

##### Data Attributes and Examples.
| Number | AttributeName                  | Description                                          | Example                            |
|--------|--------------------------------|------------------------------------------------------|------------------------------------|
| 1      | id                             | Listing ID                                           | 2539                               |
| 2      | name                           | Name of the listing                                  | Clean & quiet apt home by the park |
| 3      | host_id                        | Host ID                                              | 2787                               |
| 4      | host_name                      | Name of the host                                     | Personal Name                             |
| 5      | neighbourhood_group            | Location                                             | Brooklyn                           |
| 6      | neighbourhood                  | Area                                                 | Kensington                         |
| 7      | latitude                       | Latitude coordinates                                 | 40.64749                           |
| 8      | longitude                      | Longitude coordinates                                | -73.97237                          |
| 9      | room_type                      | Listing space type                                   | Private room                       |
| 10     | price                          | Price in dollars                                     | 149                                |
| 11     | minimum_nights                 | Amount of nights minimum                             | 1                                  |
| 12     | number_of_reviews              | Number of reviews                                    | 9                                  |
| 13     | last_review                    | Latest review                                        | 2018-10-19                         |
| 14     | reviews_per_month              | Number of reviews per month                          | 0.21                               |
| 15     | calculated_host_listings_count | Amount of listing per host                           | 6                                  |
| 16     | availability_365               | Number of days when listing is available for booking | 365                                |

##### Licence
This dataset is hosted on Kaggle under CC0 licence [[2](https://creativecommons.org/publicdomain/zero/1.0/)] which
dedicates this data to public domain making it open to copy, modify, distribute and perform the work without seeking permission. This data is compiled from public information from the Airbnb website, and hence the dataset providers claim that it is not private information as these are available on the public website. However, the dataset providers have also posted a disclaimer [[3](http://insideairbnb.com/about.html#disclaimers)] regarding the usage.

##### Human-Centred and Ethical Considerations
The data does contain the names of hosts and location of their properties,
while it is posted under CC0 license [[2](https://creativecommons.org/publicdomain/zero/1.0/)].
Therefore, on the topic of ethics, it may increase the risk (harm or bias) to the hosts if the data
is analysed and distributed through re-publishing. However, the insights from analyzing this data may
be very beneficial to study the cost of living in a city like New York from a different perspective
and maybe helpful for future hosts. But, we do not need the actual names of the hosts in this data or
the exact titles of the listing (as the name of the host can be retrieved from the listing title) to
perform this analysis.

##### Considerations for Redistributing the Data.
As an act of ethical analysis, I will anonymize the data by removing the names of hosts,
and the name of listings while analyzing and re-publishing the data. As with the original licence terms,
I would release it under CC0 licence [[2](https://creativecommons.org/publicdomain/zero/1.0/)].

### Related Work
Regarding cost-of-living in a city like New York is well documented as present in this article
[[4](https://smartasset.com/mortgage/what-is-the-cost-of-living-in-new-york-city)] by *smartasset*.
However, more analysis is present considering long-term lease rentals which may not clearly reflect the same trends
to short-term rentals. Since short-term rentals have gained popularity recently, analyzing Airbnb data to answer the
questions on short-term rentals may potentially be impactful and help both kinds of stakeholders.

### Problem Statement and Objectives
The research questions corresponding to this problem have been categorized according to its stakeholders - tenants of
a short-term rental and the host who has listed their property for short term rent.

##### Research Questions: Tenants
- **Q1.** How does the Airbnb prices distributed across the diverse set of neighborhoods in New York City?
- **Q2.** How does the type of the property - shared room, private room or entire house - affect the prices of Airbnb listings in New York City?

##### Research Questions: Hosts
- **Q3.** Can we predict prices for Airbnb listings based on selected relevant attributes? What can we understand from the prediction model?
- **Q4.** How are different types of property distributed in a given neighborhood and how dense are they?

### Methodology
##### Data Cleaning
The data is analysed to find the extent of missing information in each attribute.
Depending on the coverage of the data, appropriate method would be used to fill the data if necessary.
If a certain field has default values which could be the result of missing information would be encoded appropriately.
The data will be checked for outliers to observe if any outlier is unrealistic.

##### Feature Selection and Encoding
The attributes required for the analysis to answer the above stated research questions would be retained,
and all other attributes would be removed. Appropriate encoding would be used based on the type of data.
For instance, z-score (mean centered and standardization) [[5](https://en.wikipedia.org/wiki/Standard_score)] would be used for numerical values,
while categorical variables would be transformed to one-hot encoding [[6](https://en.wikipedia.org/wiki/One-hot)].

##### Analytical Methods
The analytical methods used are categorized based on the relevant research questions.
Each item also contains the method used for presentation and visualization.
- **Q1.** The data would be grouped based on the ```neighborhood_group```, and different aggregate metrics
for the price would be calculated. This information can be visualized effectively in a list of box-plots.
- **Q2.** The data would be grouped based on ```room_type```, and different aggregate metrics for the price
would be calculated. For a more granular understanding, the data could be grouped by ```room_type``` and
```neighborhood_group``` to observe how prices vary for different types of property across neighborhoods.
A set of box-plots (for each room-type) can be put in a sections for each neighborhood to visualize the distribution.
- **Q3.** A linear regression model [[7](https://en.wikipedia.org/wiki/Linear_regression)] can be built on the few selected independent variables like neighborhood and room type
to predict the price of the listing. This model could be trained on a subset of data and evaluated on a held-out subset
to determine our effectiveness in prediction. This model can be evaluated on the R-squared metric [[8](https://en.wikipedia.org/wiki/Coefficient_of_determination)].
Interpretation of the model coefficients can help in understanding the model inferences.
- **Q4.** The data can be grouped based on ```neighborhood_group```, and aggregate metrics based on counts of
different ```room_types``` can be computed. This would also be visualized in matrix of box-plots as in Q2.

The above data manipulation and analytical methods would be performed on Python. For visualizations,
I might use Tableau or Excel. Note that a consistent types of visualization has been maintained to make
it easier for users to consume the analysis, and multiple small plots approach is taken to make it easier
for visual comparison which is effective for humans consumption.

### Unknowns and Dependencies
The traffic information is present as availability in the last 365 days which is a proxy to
the number of days the listing is booked. This can be ambiguous as hosts might not update their listing,
or post the listing even if it is not available. Hence, if traffic information is being used, it would
be a heuristic and would involve an assumption to find the valid metric for popularity.

### References
[1] Kaggle - New York City Airbnb Open Data, published by Dgomonov. Web. 2019. [Link](https://www.kaggle.com/dgomonov/new-york-city-airbnb-open-data).

[2] Creative Commons CC0 1.0 Public Domain Dedication. Web. [Link](https://creativecommons.org/publicdomain/zero/1.0/).

[3] Disclaimer by Inside Airbnb which is the original source. Web. [Link](http://insideairbnb.com/about.html#disclaimers).

[4] What Is the True Cost of Living in New York City? by smartasset. Web. May 29, 2019. [Link](https://smartasset.com/mortgage/what-is-the-cost-of-living-in-new-york-city)

[5] Z-Score - Standard Score. Wikipedia. Web. 2019. [Link](https://en.wikipedia.org/wiki/Standard_score).

[6] One-Hot. Wikipedia. Web. 2019. [Link](https://en.wikipedia.org/wiki/One-hot).

[7] Linear Regression. Wikipedia. Web. 2019. [Link](https://en.wikipedia.org/wiki/Linear_regression).

[8] R-Squared - Coefficient of determination. Wikipedia. Web. 2019. [Link](https://en.wikipedia.org/wiki/Coefficient_of_determination).
