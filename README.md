# Cryptocurrencies

## Purpose of the project:
The purpose of this project is to use unsupervised machine learning (specifically K-means clustering) to categorize cryptocurrency data into separate clusters. 

## Data:
Data taken via CryptoCompare API. 
1,252 coins analyzed. 
Features were: CoinName, Algorithm, IsTrading (Boolean), ProofType, TotalCoinsMined, TotalCoinSupply

## Tools:
- Pandas
- Hvplot
- Plotly Express
- Sklearn.Preprocessing: StandardScaler, MinMaxScaler
- Sklearn.Decomposition: PCA
- Sklearn.Cluster: KMeans


## Methodology:

**1. Data Cleaning and Preparation:**<br></br>
Over 1,000 coins were analyzed using data from CryptoCompare.  Coins that didn't contain working algorithms, weren't being mined, and weren't being traded were dropped from the dataset. Afterwards, all non-numerical values were encoded and values standardized and scaled. <br></br>
<img width="617" alt="Screen Shot 2021-11-15 at 1 02 21 PM" src="https://user-images.githubusercontent.com/10199828/141831637-398c280d-4912-4a53-ae43-b150d8a87680.png">

**2. Reducing Data Dimensions Using PCA:**<br></br>
PCA was used to reduce the number of principal components to 3. 

**3. Clustering Cryptocurrencies Using K-means:**<br></br>
Using the PCA crypto data, an elbow curve was created using hvPlot to find the best value for K (the optimal number of K clusters ended up being 4).
Next, the K-means algorithm was used to make predictions of the K clusters for the cryptocurrencies’ data.
<img width="927" alt="Screen Shot 2021-11-15 at 1 01 33 PM" src="https://user-images.githubusercontent.com/10199828/141831531-bf21e5d7-2d06-4d1d-afa6-93be87b1729e.png">

**4. Visualizing Data:**<br></br>
Afterwards, the machine learning model's predicted classes were analyzed with 3D and 2D Scatter Plots in Plotly Express. 

## Results:
Both the 2-D and 3-D scatter plots show that the majority of cryptocurrencies are within the 0 and 3 cluster classes. A table was produced to allow users to sort coins by total coins mined and total supply of coins. 
<img width="953" alt="Screen Shot 2021-11-15 at 1 00 17 PM" src="https://user-images.githubusercontent.com/10199828/141831378-9c3a2bc6-6e55-43a3-a996-49fc18cce5a2.png">
<br></br>
<img width="829" alt="Screen Shot 2021-11-15 at 1 08 39 PM" src="https://user-images.githubusercontent.com/10199828/141832446-aa38408a-2168-4444-af4d-d9080c182165.png">
<br></br>
<img width="879" alt="Screen Shot 2021-11-15 at 1 08 15 PM" src="https://user-images.githubusercontent.com/10199828/141832378-7857c215-1d85-4f16-8f2a-e1a9389b53c0.png">



