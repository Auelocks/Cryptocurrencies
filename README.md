# Cryptocurrencies
Using Machine Learning to identify trends in cryptocurrencies that may help firms invest in cryptocurrencies.  

## Overview

The original data was provided as a csv file and included traded coin names, algorithms, a boolean indicating whether the coin is actively trading, Proof Type, Total Coins Mined, and Total Coin Supply.  The raw data was converted into a Pandas DataFrame.  To clean the data for evaluation, only cryptocurrencies actively being traded and with coins being mined were kept, rows with null values were removed, and the get_dummies method was used to create variables for Algorithm and Proof Type.  Finally, the Standard Scaler library is used to standardize the features.

Principal Component Analysis algorithm was applied to reduce the dimensions of the cleaned dataframe to three principal components.

In order to find the best K value for a K-means algorithm, hvplot is used to generate an elbow curve.  Based on the plot, a value of K=4 was used along with the K-means algorithm to predict the K clusters for the cryptocurrencies data and a new dataframe was generated where cleaned data, generated components, and clustered classes are merged into a new dataframe with the same coin name index as the original dataframe.

Finally, the results are visualized utilizing Plotly Express and hvplot to create 2D and 3D scatter plots along with a table of currently tradable cryptocurrencies.