---
layout: post
title: Topic Modeling of Cryptocurrency Topics on Twitter
---

Over the past several years the use and popularity of cryptocurrencies has soared. More recently, the price of bitcoin and other cryptocurrencies have steadily increased since earlier this year with the price of bitcoin surpassing $13,000 across several different exchanges at the time I am writing this post on the afternoon of June 26, 2019. With the strong amount of interest in cryptocurrencies on social media I thought it would be interesting to perform topic modeling of topics related to cryptocurrency on twitter using natural language processing techniques to identify various topics  being discussed that relate to digital currency.

In order to accomplish this task twitter data was streamed using the Tweepy streamer in python from which twitter data was stored in a MongoDB database. Tweets were streamed over a two week period and specifically filtered for terms relating to cryptocurrency including blockchain, bitcoin, ethereum, binance, etc. As a form of dimensionality reduction, topic modeling could then be performed to represent the text from each tweet in its topic space in which various topics could be identified as a cluster of similar tweets.

A total of 30,000 tweets were collected and stored in a MongoDB database. Latent semantic analysis (LSA), non-negative matrix factorization (NMF), and latent dirichlet allocation (LDA) were topic modeling algorithms that were performed. LSA provided the best separation between topics and yielded three distinct topics which could be identified as tweets relating to blockchain technology, trading and investing of cryptocurrencies, as well as the free distribution of virtual coins.

![Distribution](https://github.com/Gopher2016/Gopher2016.github.io/blob/master/images/Cryptocurrency_Topics.png?raw=true)

From the collection of tweets I could then perform sentiment analysis in which each tweet could be given a sentiment score of either positive, negative, or neutral. The results of this analysis are shown below. Although the majority of tweets within this sample were scored as having neutral sentiment, the number of tweets having a positive sentiment score outnumbered those having a negative sentiment score by a factor of three.

![Distribution](https://github.com/Gopher2016/Gopher2016.github.io/blob/master/images/Cryptocurrency_Sentiment_Analysis.png?raw=true)

In conclusion, the major topics relating to cryptocurrency being discussed on Twitter included topics relating to blockchain technology, trading and investing of cryptocurrencies, as well as the free distribution of virtual coins. At this point in time individuals tweeting about cryptocurrency seem to be more optimistic about its future prospects, based on sentiment analysis, however, digital currency is still in a relatively early adoption phase with many countries still yet to pass legislation regulating cryptocurrencies and still relatively few businesses accepting payment in the form of cryptocurrency. The price of bitcoin and other cryptocurrencies is still largely driven by speculation at this point in time and only time will tell how well these digital assets integrate within business and society.
