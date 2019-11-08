# DATA 512 - Project Proposal

### Motivation
Short-term rentals are getting popular and people have been considering short-term accommodations over hotels as an affordable and convenient alternative. Various hosts open up their property for such short-term and provide services. Their listings are available online which can be browsed by customers before they opt for it. It is very similar to hotels, but anyone can host their property even if it is a small place. There is a lot of diversity in such short-term accommodations and their prices vary largely due to the diverse sets of individual hosts and different types of property hosted.

I would like to explore how the prices are distributed across different areas of a city, and how prices vary for different types of property. Also, such an analysis could help new hosts to decide an appropriate price for their listing. Can this inform us about the cost of living in different areas of a city?

### Data Description
Airbnb is one of the largest short-term rental providers which connects various hosts to customers on the Airbnb portal where the listings provided by hosts can be opted by customers who browse the portal. hence, I would like to use the New York City Airbnb Open Data which provides details on Airbnb lists and metrics in New York city for 2019 [[1](https://www.kaggle.com/dgomonov/new-york-city-airbnb-open-data)] till 07 Jun 2019 (since 27 March 2011). The dataset contains 49,080 Airbnb listings across 5 different neighbourhood groups in New York City along with the listing title, geographic location, neighbourhood (area and wider region), type of property (entire house, private room or shared room), minimum nights for booking and price. It also contains some traffic information like the number of days when the listing was available for booking in a year, the number of reviews per month, and the date of the latest review. This dataset contains a large number of listings in one of the more populated cities in the US along with the above-mentioned attributes which makes this dataset very relevant for this problem.

This dataset is hosted on Kaggle under CC0 licence [[2](https://creativecommons.org/publicdomain/zero/1.0/)] which dedicates this data to public domain making it open to copy, modify, distribute and perform the work without seeking permission. This data is compiled from public information from the Airbnb website, and hence the dataset providers claim that it is not private information as these are available on the public website. However, the dataset providers have also posted a disclaimer [[3](http://insideairbnb.com/about.html#disclaimers)] regarding the usage.

The data does contain the names of hosts and location of their properties, while it is posted under CC0 license [[2](https://creativecommons.org/publicdomain/zero/1.0/)]. Therefore, on the topic of ethics, it may increase the risk (harm or bias) to the hosts if the data is analysed and distributed through re-publishing. However, the insights from analyzing this data may be very beneficial to study the cost of living in a city like New York from a different perspective and maybe helpful for future hosts. But, we do not need the actual names of the hosts in this data or the exact titles of the listing (as the name of the host can be retrieved from the listing title) to perform this analysis. As an act of ethical analysis, I would consider anonymizing or removing the names of hosts, and the name of listings while analyzing and re-publishing the data.

### Unknowns and Dependencies
The traffic information is present as availability in the last 365 days which is a proxy to the number of days the listing is booked. This can be ambiguous as hosts might not update their listing, or post the listing even if it is not available. Hence, if traffic information is being used, it would be a heuristic and would involve an assumption to find the valid metric for popularity.

### References
[1] Kaggle - New York City Airbnb Open Data, published by Dgomonov. Web. 2019. [Link](https://www.kaggle.com/dgomonov/new-york-city-airbnb-open-data).

[2] Creative Commons CC0 1.0 Public Domina Dedication. Web. [Link](https://creativecommons.org/publicdomain/zero/1.0/).

[3] Disclaimer by Inside Airbnb which is the original source. Web. [Link](http://insideairbnb.com/about.html#disclaimers).
