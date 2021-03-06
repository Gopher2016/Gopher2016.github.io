---
layout: post
title: MTA Turnstile Data
---

Hello and welcome to my blog! As a student in the Chicago Metis Data Science cohort I was tasked with analyzing Metro Transit Authority (MTA) data in the New York City metro area. The insights from this analysis would be used to assist a nonprofit client in sending out street teams to various MTA train stations to advocate for an upcoming WomenTechWomenYes gala being held at the beginning of summer.

In order to accomplish this task a number of factors were considered in our analysis. Many of the turnstile entries recorded within this data set did not change from one date to the next indicating a broken turnstile counter. These turnstiles were removed from the data. Furthermore, a large number of turnstiles counted in reverse and thus measures for daily entries were converted to the absolute value of the change in entries between days. Turnstiles that reset their counter as well as turnstiles that were transferred to new location were also accounted for in this analysis.

The sample distribution of daily entries for all New York City MTA stations is plotted below. The data followed a Poisson distribution in which the right tail of the sample distribution contained some of the busier stations in the New York City metro area. These stations ranged anywhere from 4,000 to 6,000 mean daily entries.

![Distribution](https://github.com/Gopher2016/Gopher2016.github.io/blob/master/images/Distribution_Daily_Entries_MTA_Stations.png?raw=true)

An interesting trend emerged when plotting out the data such that weekly highs and lows in measures of daily entries at the five busiest terminals followed a similar trend. This observation was found to correspond with differences in weekday and weekend traffic at each station.

![Distribution](https://github.com/Gopher2016/Gopher2016.github.io/blob/master/images/May_June_2018_Daily_Entries_by_Station.png?raw=true)

The results from this analysis not only provide insight into which MTA stations in the New York City metro area experience the greatest number of daily entries but more specifically help identify which days of the week will have the greatest foot traffic. Sending street teams out to the MTA stations identified as having the greatest number of daily entries during weekdays will allow WomenTechWomenYes to promote their gala to the greatest number of individuals as well as to target residents living and working in the New York City area who are more likely to attend the event. 
