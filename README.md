# Cryptocurrencies:

Using machine learning to determine which Cryptocurrencies are worth the investment.

## Purpose of the Project:

Accountability Accounting, a prominent investment bank, is interested in offering a new cryptocurrency investment portfolio for its customers. The company, however, is lost in the vast universe of cryptocurrencies. The intended purpose is to create a report that includes what cryptocurrencies are on the trading market and how they could be grouped to create a classification system for this new investment.

The data is not ideal, so it will need to be processed to fit the machine learning models. Since there is no known output, unsupervised learning was employed. To group the cryptocurrencies a clustering algorithm was used.

## Preprocessing the Data for PCA:

Unnecessary columns were dropped, null rows were removed, as well as the removal of rows that did not have coins being mined.

The get_dummies() method was used to create variables for the text features, which were then stored in a new DataFrame (X). Finally, the features from the X DataFrame were standardized using the StandardScaler fit_transform() function.

## Reducing Data Dimensions Using PCA:

A new DataFrame named pcs_df was created. It includes the following columns: PC 1, PC 2, and PC 3. The DataFrame uses the index of the crypto_df as the index.

## Clustering Cryptocurrencies Using K-means:

Using the K-means algorithm, an elbow curve was created using hvPlot to find the best value for K from the pcs_df DataFrame. Running the K-means algorithm, the K clusters were predicted for the cryptocurrencies’ data.

## Visualizing Cryptocurrencies Results:

Scatter plots were created with Plotly Express and hvplot to visualize the distinct groups that correspond to the three principal components previously created. A table was also created with all the currently tradable cryptocurrencies using the hvplot.table() function. 

## 3D Clusters Scatterplot:

<img width="783" alt="image" src="https://user-images.githubusercontent.com/106691255/203685056-c95df7e1-142c-4822-84bf-1b463a247bca.png">

## Tradable Cryptocurrencies Table:

<img width="877" alt="image" src="https://user-images.githubusercontent.com/106691255/203685107-4498435f-577d-42d2-a2c8-c5933490ee95.png">

## Clustered DataFrame:

<img width="843" alt="image" src="https://user-images.githubusercontent.com/106691255/203685189-fddd2cca-3167-4803-bbb8-79817fad2a94.png">

## Coin Scatterplot:

<img width="1004" alt="image" src="https://user-images.githubusercontent.com/106691255/203685232-74e7d476-0e19-4784-9845-ebc00e88400c.png">
