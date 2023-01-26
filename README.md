# Cryptocurrencies
In this work, we use unsupervised machine learning techmeques to categorize a list of cryptocurrencies.

### Data
The [data](https://github.com/ranilb/Cryptocurrencies/blob/main/crypto_data.csv) was retrieved from [CryptoCompare](https://min-api.cryptocompare.com/data/all/coinlist) webpage.

## Results
The original data set has 1252 different crypto currencies, but only 1144 are being traded now. First 10 rows of the dataset is shown below.


<img width="548" alt="Screen Shot 2023-01-26 at 11 45 29 AM" src="https://user-images.githubusercontent.com/112113327/214896417-c6e44453-eee5-49ff-b502-cb7871f5514d.png">

For the analysis, we filtered the data to get cryptos with only non-zero "total number coins mined" and then it came down to 532 different coins. After removing the string data and making dummies, we got 98 columns and which introduced a higher dimentional problem. Therefore, we used the "Principle component analysis to reduce to dimentioin of the problem to 3. Then to determine the best k value for K-means method, the "Elbow curve" was created and observed that k=4 is the best value. The graph is shown below.

  <img width="743" alt="Screen Shot 2023-01-26 at 11 56 37 AM" src="https://user-images.githubusercontent.com/112113327/214899329-0f67d3f0-445e-438e-aa17-6049a4bc650b.png">

Then the dataset was categorized into four different categories and the first 10 rows are shown below.

  <img width="793" alt="Screen Shot 2023-01-26 at 11 59 10 AM" src="https://user-images.githubusercontent.com/112113327/214899878-9357667c-fd7b-410c-96a0-2a62f0841082.png">

The 3-D graph of three principle componets are shown below.

  <img width="744" alt="Screen Shot 2023-01-26 at 11 59 58 AM" src="https://user-images.githubusercontent.com/112113327/214900173-c1b30468-904a-4b00-9c8b-1adef5563bbb.png">

Lastly, the scatter plot of four groups are shown with "x="TotalCoinsMined" and y="TotalCoinSupply".

<img width="673" alt="Screen Shot 2023-01-26 at 12 03 27 PM" src="https://user-images.githubusercontent.com/112113327/214900807-132924e5-7f80-4d3a-9195-c6e4cafbbdaf.png">


## Summary
It can be observed that most of the coins fall into categories only two categories. They have a few total number of coins mined and less coin supply. 
To get more information about those two categories, we can use more data such as daily volume and the price for last 52 weeks. 
