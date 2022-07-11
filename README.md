# Cryptocurrencies
Crypto currency analysis using unsupervised machine learning method

## Overview
The purpose of this project is to analyze a dataset from many alternative cryptocurrencies to spot trends that make a company or person want to invest in them. The problem with cryptos is that the most common ones, like bitcoin or ethereum, are becoming unaffordable for the common public. That being said, I will be using unsupervised machine learning to see if we can spot any trends that result in opportunities for these cryto currency market.

## Results:
* Preprocess and transform the data so that unsupervised machine learning could work. This included dropping null values, using only tradeable and mined cryptocurrencies, numerically encoding categorical columns using the pandas.get_dummies method, and scaling the data using the StandardScaler() method as well.

* Proceeded with the Principal Component Analysis (PCA) to reduce the 98 scaled columns I had, to only 3 principal components.

Then, using elbow curve to see how many clusters (k) can be devided in the cryptos in:


* As it can be seen, the optimal result was 4 clusters. So, I then proceeded with the KMeans analysis to fit the PCA dataframe and predict the clustering. The product was this clustered_df with a 'Class' column that showed the predictions to which group it belonged to.

* And last but not least, I came up with some visualizations to better understand the results.

* This first one was a 3D scatter plot which located each clustered crypto in relation to the 3 principal components created on the PCA. As it is seen, there are 3 major groups and one outlier.

* Similarly, when trying to graph the clustered cryptos by total supply and mined coins, we can observe two outliers. The first one with a lot of supply and a lot of mined coins (BitTorrent Crypto) and another one with a lot of supply but not too many coins mined (TurtleCoin).


## Summary
The job of unsupervised machine learning is to discover patterns or groups of data when there is no known output. That being said, this analysis was successful at grouping cryptocurrencies into 4 groups. If we were to create a crypto investment portfolio we would need to further analyze the clusters. Nevertheless, we have a good start point where we can see that the most profitable and known cryptos are somewhat in the 2 groups that have less supply and mined coins in comparison to others. These cryptos are Bitcoin and Ethereum. Nevertheless, we should keep up with the innovations of technology where new altcoins are being created with very interesting value propositions.
