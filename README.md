# Cryptocurrencies
Crypto currency analysis using unsupervised machine learning method

## Overview
The purpose of this project is to analyze a dataset from many alternative cryptocurrencies to spot trends that make a company or person want to invest in them. The problem with cryptos is that the most common ones, like bitcoin or ethereum, are becoming unaffordable for the common public. That being said, I will be using unsupervised machine learning to see if we can spot any trends that result in opportunities for these cryto currency market.

## Results:
* Preprocess and transform the data so that unsupervised machine learning could work. This included dropping null values, using only tradeable and mined cryptocurrencies, numerically encoding categorical columns using the pandas.get_dummies method, and scaling the data using the StandardScaler() method as well.

* Proceeded with the Principal Component Analysis (PCA) to reduce to only 3 principal components.
![ThreePrincipleComponents](https://user-images.githubusercontent.com/100484606/178184995-610a620f-e5df-4313-b89a-e9192bd4df79.JPG)


Then, using elbow curve to see how many clusters (k) can be devided in the cryptos:
![ElbowCurve](https://user-images.githubusercontent.com/100484606/178185050-a5e431c7-bfb2-4793-a888-621b6fb7cf4a.JPG)


* As it can be seen, the optimal result was 4 clusters. Then, using the KMeans analysis to fit the PCA dataframe and predict the clustering. The product was this clustered_df with a 'Class' column that showed the predictions to which group it belonged to.
![ClusteredShape](https://user-images.githubusercontent.com/100484606/178185117-aa7d5c72-3b40-42ce-928b-812e534ab4d1.JPG)


* Following are some visualizations to better understand the results:

* This first one was a 3D scatter plot which located each clustered crypto in relation to the 3 principal components created on the PCA. There are 3 major groups and one outlier.
![3DShape](https://user-images.githubusercontent.com/100484606/178185182-52f2b462-b27d-49c7-b1a3-c16f13b8ec15.JPG)

* Similarly, when trying to graph the clustered cryptos by total supply and mined coins, we can observe two outliers. The first one with a lot of supply and a lot of mined coins and another one with a lot of supply but not too many coins mined.
![TotalCoinSupply](https://user-images.githubusercontent.com/100484606/178185224-fe0ae52d-d880-4ace-aa1f-4adb39f86b75.JPG)

## Summary
The job of unsupervised machine learning is to discover patterns or groups of data when there is no known output. That being said, this analysis was successful at grouping cryptocurrencies into 4 groups. If we want to create a crypto investment portfolio we would need to further analyze the clusters.
