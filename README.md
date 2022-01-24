# Departure Delay Analysis on NYC flight in 2013
* Written by: [Poon Athit S. ](https://www.linkedin.com/in/athit-srimachand/), Ivy Wu, Carol Fan
* Technologies: R, Tableau, tidyverse

## 1. Introduction
This project aims to utilise R and [Tableau dashboard](https://public.tableau.com/views/DepartureDelayAnalysisonNYCflightin2013/Dashboard?:language=en-US&:display_count=n&:origin=viz_share_link) to visualize the New York city flight dataset in 2013 and gain insights regarding how to improve departure delay, which is one of the most addressed problems faced by all stakeholders within the supply chain of air travel. We believe the four most critical factors - **time, weather, planes (age and type) and carrier** - entail departure delays. To quantify, we choose different indicators of departure delay to visualize, in terms of **average delay time (in minutes)**, **delay occurrences**, and **departure delay percentage**. Therefore, the analysis will provide the answers to the following questions:
- Question 1: What is the time pattern of departure delay?
- Question 2: What is the effect of weather on departure delay?
- Question 3: What is the impact of carrier performance on departure delay?
- Question 4: How does the plane type and age affect the departure delay?

## 2. Key findings
The Port Authority of New York and New Jersey operates the 3 major airports including JFK, EWR and LGA in NYC. The analysis is focused on the historical data in 2013 and is aimed at understanding the general trends in flights and performance of NYC airports as to examine different factors related to departure delays. With all careful analysis and data exploration, recommendations are provided in three aspects to address the long departure delay issue in NYC airports.

### 2.1 Delay pattern throughout the year of 2013
<img src="https://github.com/PoonAthitS/departure-delay-analysis-nyc-flight/blob/main/IMAGES/Average%20departure%20delay%20calendar.png?raw=true" width="550">

By observing the density of yellow grids in Average departure delay calendar, it is obvious that April, June, July and December have a higher percentage of departure delay. The delayed pattern seems to be following the holiday occasions in the United States in which Easter, Summer Holiday and Christmas are in April, June and July, December respectively. It is also clear that a high percentage of delays are observed at night, which is possibly caused by the propagation delay – a subsequent flight might be delayed because it is awaiting the takeoff of the previous flight. <br />

Based on the above findings in time series analysis, it is suggested that the port authority should modify the scheduled departure time for those busy months. A flexible slack time should be re-allocated in the flight schedule in which the ability of departure delay absorption during peak hours should be stronger than that of other months. The enhanced flight schedule could reduce the propagation delay caused by the preceding flight delays and reduce the phenomenon of flights are likely to delay at night. On the other hand, it is foreseeable that passenger volume will substantially increase during holiday periods and often resulting in long queues for flight check-in and security check. It is suggested to increase the air carrier crew during the holiday period to withstand the high pressure of check-in volume and baggage loading problems. More check-in counters should be opened for passengers to increase efficiency and ultimately prevent the departure delay caused by ground staff.

### 2.2 Carrier performance
<img src="https://github.com/PoonAthitS/departure-delay-analysis-nyc-flight/blob/main/IMAGES/Performance%20of%20carriers%20per%20origin.png?raw=true" width="550">

As indicated by the graph, for EWR airport, EV and UA had the worst performance with 31% and 22% of their flights were delayed respectively. Since both carriers provided a high number of flights, they contributed a lot of flight delays in NYC. For JFK airport, B6 and 9E were the bad performers with 23% and 28% of their flights being delayed respectively.  Whereas B6 contributed 13% of flights and 9E contributed 4% of flights in NYC. Considering EWR and JFK airport serves as major international hubs, the delays of those airlines are probably caused by waiting for connecting passengers, bags or crews that are arriving from another destination. It is suggested that a clear guideline should be provided for any connecting passengers to make sure they follow the flight transit time straightly. In addition, those airlines should ensure enough or even additional crew on staff during peak hours in case of unexpected situations that the original crew is delayed by other flights. <br />

For LGA, although we observed a lot of red bars with high percentages, those carriers did not contribute much to the total departure delays as they only offer very few flights in LGA. Instead, we can conclude that EV was the bad performer with 16% of its flights being delayed and contributing a relatively high number of flights. As LGA is the flagship domestic airport in NYC, a domestic aircraft will typically be used for more flights per day compared to ones used internationally. Again, a ripple effect might occur if the preceding domestic flight has a significant delay. In consequence, domestic flights are likely to have less time for preparing the aircraft such as cleaning, loading and unloading catering equipment and supplies, etc. Therefore, it is suggested that the EV airline should collaborate with the airline catering agent and cleaning agent by sending more staff for aircraft preparation during the peak hours in LGA airport. The route for catering trucks transportation should also be optimized to efficiently decrease the unnecessary travel time within the airport ground.

### 2.3 Effects from weather factors
<img src="https://github.com/PoonAthitS/departure-delay-analysis-nyc-flight/blob/main/IMAGES/average%20delay%20vs%20weather%20factors.png?raw=true" width="550">

Significant meteorological conditions might cause departure delays. As indicated by the graph, flights are mostly affected by high precipitation and high relative humidity level which shows that heavy rainfall will contribute to departure delays. On the other hand, visibility also adversely affects the flight departure when it drops to 3 miles or below. <br /> 

Although it is impossible to alter the weather, an upgrade in the runway lighting system might be useful to withstand the low visibility conditions resulting from fog or heavy rainfall. Furthermore, it is always better to get ready for service resumption when the weather becomes normal again. It is suggested that Airlines should always update their weather forecasting techniques or tools so that they can deal with the aftermath as soon as possible to minimize the flight departure delay time.

## 3. Tableau Dashboard
<img src="https://github.com/PoonAthitS/departure-delay-analysis-nyc-flight/blob/main/IMAGES/Tableau%20dashboard.PNG?raw=true" width="550">

Tableau public dashboard link: [Departure Delay Analysis on NYC flight in 2013](https://public.tableau.com/views/DepartureDelayAnalysisonNYCflightin2013/Dashboard?:language=en-US&:display_count=n&:origin=viz_share_link) <br /> 

Building on results from the analysis in R, an interactive dashboard is developed to enable exploration of the data and extract insights that would be the most important to communicate in the context of problems. This dashboard covers all time pattern, effect of weather and impact of carrier performance toward the departure delay.
## 4. About the programming

### 4.1 Files
* The analysis in R is developed in [R Markdown notebook](https://github.com/PoonAthitS/departure-delay-analysis-nyc-flight/blob/main/Departure_Delay_Analysis_on_NYC_flight_in_2013.Rmd)
* The report of R analysis is knitted in [HTML report](https://github.com/PoonAthitS/departure-delay-analysis-nyc-flight/blob/main/Departure_Delay_Analysis_on_NYC_flight_in_2013.html)
* Tableau dashboard is pulished in [Tableau public link](https://public.tableau.com/views/DepartureDelayAnalysisonNYCflightin2013/Dashboard?:language=en-US&:display_count=n&:origin=viz_share_link)

### 4.2 Data
The [NYC flight 2013 dataset](https://github.com/PoonAthitS/departure-delay-analysis-nyc-flight/tree/main/data) (nycflights13) collects 3,273,346 flights details from three NYC airports - John F. Kennedy International Airport (JFK), Newark Liberty International Airport (EWR) and LaGuardia Airport (LGA). It also captures information about weather, airports, airlines and planes.

### To learn more about Poon Athit S., visit his [LinkedIn profile](https://www.linkedin.com/in/athit-srimachand/)

All rights reserved 2022. All codes are developed and owned by Poon Athit S. or the metioned team member(s). If you use this code, please visit his LinkedIn and give him a skill endorsement in Data analytics and the aforementioned coding technologies.
