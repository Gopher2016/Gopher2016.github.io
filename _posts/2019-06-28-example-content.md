---
layout: post
title: Forecasting Retail Store Demand with Time-Series Analysis
---

At one point or another we've all had a shopping experience in which we've gone out with the intention of buying a specific item, whether it be the newest iPhone, a new pair of headphones, or even just a generic food purchase from the grocery store, only to find that the item we had been looking for was out-of-stock. This is a common frustration that most people can relate to and as such I wanted to investigate whether I could solve this problem using data science.

The objective of my analysis was to forecast store-level demand across various retail locations to ultimately inform business decisions relating to the prediction of short-term and long-term store performance, demand and financial planning, as well as inventory management and supply decisions. In order to address these business problems store-level data was collected from the online machine learning community Kaggle which provided five years of sales data across ten different store locations.

To help visualize the retail sales data I grouped together total monthly sales by store and plotted the data in Tableau as a time-series which is shown below. From this plot it is clear that retail sales typically peak during the summer months and dip at the beginning of each calendar year. This seasonal trend appeared to be very consistent throughout each of the ten different store locations.

![Distribution](https://github.com/Gopher2016/Gopher2016.github.io/blob/master/images/Five_Year_Monthly_Sales_by_Store.png?raw=true)

All time-series modeling in my analysis was performed using the StatsModels API within python. I tested a total of four time-series models for each of the ten store locations which included autoregressive (AR), autoregressive moving average (ARMA), autoregressive integrated moving average (ARIMA), as well as a seasonal ARIMA (SARIMA) model which proved to be the best performing model for retail sales data.

From the five year data set, data was grouped by weekly observations representing total weekly sales. 2013 through 2016 sales data was used to train each model which could then forecast weekly sales for the 2017 calendar year. Forecasted sales could then be referenced with actual sales from 2017 to calculate model error. Below is a bar chart showing the average root mean squared error (RMSE) in dollars for each model tested for all ten store locations.

![Distribution](https://github.com/Gopher2016/Gopher2016.github.io/blob/master/images/Time_Series_Model_Evaluation.png?raw=true)

The seasonal trends observed within the retail sales data were so strong that adding a seasonality component to the previously tested ARIMA model (SARIMA) made massive improvements to overall model performance and reduced model error significantly. The bar chart above further highlights this point and helps illustrate the importance of accounting for annual trends in retail sales when making future sales predictions.

To help visualize the accuracy of the final SARIMA model used to forecast 2017 weekly sales, I have included a time-series plot below from one of the store locations in which 2013 - 2016 sales are shown in blue and 2017 forecasted sales are shown in green. Actual sales from the 2017 calendar year are shown in red and we can see that the SARIMA model predictions generalize very well to the out-of-sample sales data having a RMSE of just under $2,000. In other words, my model was off by less than $2,000 on average for weekly sales predictions made for the 2017 calendar year. Considering that average sales for this particular store was around $20,000, being off by less than $2000 on average, or less than 10% of average retail sales, confirmed that my model was making accurate predictions.

![Distribution](https://github.com/Gopher2016/Gopher2016.github.io/blob/master/images/2017_Weekly_Sales_Forecast.png?raw=true)

The results from this analysis may ultimately be leveraged to guide business decisions relating to annual retail sales. Gaining an understanding of future retail demands will ultimately enable businesses to make better judgements on long-term company goals and strategies that will allow for the best possible customer experience.
