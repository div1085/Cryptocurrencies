## Unsupervised ML model for clustering Cryptocurrencies

### Overview of the analysis:
Accountability Accounting, a prominent investment bank, is interested in offering a new cryptocurrency investment portfolio for its customers. The company, however, is lost in the vast universe of cryptocurrencies. So, they’ve asked you to create a report that includes what cryptocurrencies are on the trading market and how they could be grouped to create a classification system for this new investment.
This classification is generated by unsupervized machine learning model: that process data, and cluster data, model should also reduce dimensions, and reduce the principal components using PCA.

### Results

#### Preprocessing: 
Load the file crypto_data.csv, it is further preprocessed by: 
    1. The data such currecy not trading, 'IsTrading', rows with null valaue, that are not useful are removed.
    2. Create variables for the text features by get_dummies() method
    3. Features are than standardized using the StandardScaler fit_transform() function

#### Reducing Data Dimensions Using PCA:
PCA algorithm reduces the dimensions of the X DataFrame down to three principal components. A new DataFrame to hold the principal components is created and has the following three columns, PC 1, PC 2, and PC 3, and has the index from the processed DataFrame.

#### Clustering Cryptocurrencies Using K-means:
K-means algorithm is used to cluster the cryptocurrencies using the PCA data. An elbow curve is created using hvPlot to find the best value for K=4. Predictions are made on the K clusters of the cryptocurrencies’ data. Finally,  new DataFrame is created with the same index as the processed DataFrame had, new columns of principal component and scaled data is created.

![Visualizing Clustering Results](https://github.com/div1085/Cryptocurrencies/blob/a1b88d88c4cb94264b043f592975974c29363256/Resources/clustering.png)


#### Visualizing Cryptocurrencies Results:
Scatter plot with axis as with x= Total Coins Mined, y= Total Coin Supply, labled by Class, is created to view the data clusters:

![Visualizing Cryptocurrencies Results](https://github.com/div1085/Cryptocurrencies/blob/7634acb2407de0045c9e1837f5953634338e9dfb/Resources/bokeh_plot.png)

