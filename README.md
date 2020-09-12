# Cryptocurrencies

In this challenge we are tasked to run Unsupervised Machine Learning on a set of cryptocurrencies traded on the market.

## Goals

For this challenge we prepare the data for dimension reduction with PCA and clustering using KMeans, reduce data dimensions using PCA algorithms from sklearn, predict clustering using cryptocurrencies data using the KMeans algorithm from sklearn, and create some plots and data tables to present the results.

### Activity

The programs starts with reading in the crypto_data.csv dataset into a Pandas DataFrame and then processing the information for the machine learning clustering. The programs deletes currencies not traded on the market and have yet to be mined, removes rows containing NULL values, and converts text values into numerical data. The program then takes the remaining dataset and scales the information using StandardScaler from the sklean library.

The PCA algorithm from sklearn is then used to reduce the dimensions of the scaled DataFrame resulting in a three-dimension dataset. An elbow curve is created to find the optimal value of K. It was found that point 4 resulted in a possibly good K value. The KMeans algorithm is then run to find 4 clusters for the cryptocurrency dataset.

The data is then visualized via a 3D scatter plot, a datatable of currently tradable currencies, and a standard scatter plot. The datatable and standard scatter plot were created using the hvplot library. The scatter plot from hvplot uses x = "TotalCoinsMined" and a y = "TotalCoinSupply".
