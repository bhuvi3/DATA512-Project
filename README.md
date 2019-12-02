# A6: Final Project Report
## DATA512: Human Centred Data Science

This is an academic course project carried out as part of "DATA512: Human Centred Data Science"
([course-wiki](https://wiki.communitydata.science/Human_Centered_Data_Science_(Fall_2019)#Week_1:_September_26)).

### Abstract
**TODO**

### Usage
The Jupyter notebook named ```final_project_report.ipynb``` is present in this repository which analyses
the attached data (```airbnb_ny-2019.csv```) to answer interesting research questions.
The notebook can be run by downdloading it and placing the data file in the same directory.

#### Dependencies
The study performed in this project uses Python code. The following dependencies can be installed to reproduce this analysis.
- ```Python==3.6.7```: Please refer to this [link](https://www.python.org/downloads/release/python-367/) for information on the python version used for this analysis.
- ```pandas==0.24.2```: Install this python library which provides functions to process structured data by referring to this [link](https://pandas.pydata.org/pandas-docs/version/0.24/install.html).
- ```numpy==1.14.6```: Install this python library which provides linear algebraic functions by referring to this [link](https://libraries.io/pypi/numpy/1.14.6).
- ```matplotlib==3.0.3```: Install this python library which provides functions to get data visualizations by referring to this [link](https://pypi.org/project/numpy/).
- ```Jupyter```: This package allows us to open Jupyter notebooks and access the python environment in an interactive format used in this study. Install Jupyter by referring this [link](https://jupyter.org/).
These above dependencies can be easily installed using the ```conda``` package manager. Please find more information in this [link](https://www.anaconda.com/distribution/).

### Data Description
Airbnb is one of the largest short-term rental providers which connects various hosts to customers on the
Airbnb portal where the listings provided by hosts can be opted by customers who browse the portal.
The dataset included in this repository ```airbnb_ny-2019.csv``` contains 49,080 Airbnb listings across 5 different
neighbourhood groups in New York City along with the geographic location,
neighbourhood (area and wider region), type of property (entire house, private room or shared room),
minimum nights for booking and price. It also contains some traffic information like the number of
days when the listing was available for booking in a year, the number of reviews per month, and
the date of the latest review. This dataset contains a large number of listings in one of the more
populated cities in the US along with the above-mentioned attributes which makes this dataset very relevant for this problem.

#### Data Source
The data used for this study has been derived from the New York City Airbnb Open Data which provides details on Airbnb lists
and metrics in New York city for 2019 [data-link](https://www.kaggle.com/dgomonov/new-york-city-airbnb-open-data)
till 07 Jun 2019 (since 27 March 2011).
This dataset is hosted on Kaggle under [CC0 licence](https://creativecommons.org/publicdomain/zero/1.0/) which
dedicates this data to public domain making it open to copy, modify, distribute and perform the work without seeking permission. This data is compiled from public information from the Airbnb website, and hence the dataset providers claim that it is not private information as these are available on the public website. However, the dataset providers have also posted a [disclaimer](http://insideairbnb.com/about.html#disclaimers) regarding the usage.

#### Human-Centred and Ethical Considerations and Redistributed Data in the Repository
The data does contain the names of hosts and the names of their properties,
while it is posted under [CC0 licence](https://creativecommons.org/publicdomain/zero/1.0/).
Therefore, on the topic of ethics, it may increase the risk (harm or bias) to the hosts if the data
is analysed and distributed through re-publishing. However, the insights from analyzing this data may
be very beneficial to study the cost of living in a city like New York from a different perspective
and maybe helpful for future hosts. But, we do not need the actual names of the hosts in this data or
the exact titles of the listing (as the name of the host can be retrieved from the listing title) to
perform this analysis.
Therefore, the redistributed version of the data on which this study is based on and is included in this repository, has been anonymized by removing the host names and the names of the listings.

#### Data License
The data included in this repository is released under the [CC0 licence](https://creativecommons.org/publicdomain/zero/1.0/), which dedicates this data to public domain making it open to copy, modify, distribute and perform the work without seeking permission.

##### Data Attributes and Examples.
| Number | AttributeName                  | Description                                          | Example                            |
|--------|--------------------------------|------------------------------------------------------|------------------------------------|
| 1      | id                             | Listing ID                                           | 2539                               |
| 2      | host_id                        | Host ID                                              | 2787                               |
| 3      | neighbourhood_group            | Location                                             | Brooklyn                           |
| 4      | neighbourhood                  | Area                                                 | Kensington                         |
| 5      | latitude                       | Latitude coordinates                                 | 40.64749                           |
| 6      | longitude                      | Longitude coordinates                                | -73.97237                          |
| 7      | room_type                      | Listing space type                                   | Private room                       |
| 8     | price                          | Price in dollars                                     | 149                                |
| 9     | minimum_nights                 | Amount of nights minimum                             | 1                                  |
| 10     | number_of_reviews              | Number of reviews                                    | 9                                  |
| 11     | last_review                    | Latest review                                        | 2018-10-19                         |
| 12     | reviews_per_month              | Number of reviews per month                          | 0.21                               |
| 13     | calculated_host_listings_count | Amount of listing per host                           | 6                                  |
| 14     | availability_365               | Number of days when listing is available for booking | 365                                |
