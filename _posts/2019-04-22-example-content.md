---
layout: post
title: Modeling GDP per Capita
---

While GDP, or gross domestic product, is the most widely used measure of a country's economic activity, GDP per capita is a much better indicator of a nation's living standards since it adjusts for population differences between countries. I performed a regression analysis on GDP data in order to investigate factors that predict GDP per capita on a country level.

In order to accomplish this task a number of factors were considered in this analysis. Of the many potential factors influencing GDP, metrics considered in this analysis were those relating to global economics, government policies, public health, public education, and access to natural resources.

The top 20 countries by GDP per capita (in USD) are shown in the graph below. The United States is 12th on this list with an 2018 GDP per capita of $62,606. The nations that top this list, and their respective GDP per capita, include Qatar ($130,475), Macau ($116,808) and Luxembourg ($106,704).

![Distribution](https://github.com/Gopher2016/Gopher2016.github.io/blob/master/images/Top_20_Countries_by_GDP.png)

Linear regression, lasso regression and ridge regression algorithms were used to model GDP per capita at a country level. Each regression algorithm was cross-validated on test data and model performance was compared between models. Lasso regularization was used to drop features that did not contribute to model performance. Following this iterative process each model could be retested and cross-validated comparing model performance at each point.

In this analysis the best performing model was found to be a lasso regression model including features for health adjusted life expectancy (HALE), economic freedom, proven oil reserves per capita, population density, whether or not a country was landlocked, as well as total land area. A correlation heatmap for the response variable, GDP per capita, and each of the features included in the final model is provided below to visually display the relative correlation of each individual feature with GDP per capita.

![Distribution](https://github.com/Gopher2016/Gopher2016.github.io/blob/master/images/Correlation_Heatmap.png)

The results from this analysis can serve to inform public policy decisions that may ultimately influence GDP per capita at a national level. The ability to make better data-driven decisions based on new insights is a key component of data science and one that should not be limited to the data science industry.
