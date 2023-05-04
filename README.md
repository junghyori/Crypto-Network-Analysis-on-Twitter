# Multilayer Network Analysis : Cryptocurrency Communities on Twitter

This project involves the analysis of cryptocurrency communities on Twitter using a multilayer network approach. The study investigates the interplay between the hashtag-hashtag layer and the crypto-crypto layer, and explores how these layers are related to network centrality and community detection. The results provide valuable insights for investors, traders, and businesses looking to make informed decisions in the cryptocurrency market.

This README file does not cover the details on the method and result. You can check the details on the project and analysis result [here.](https://drive.google.com/file/d/1DeQi6W5oK2T-9IzXAYFzRg1YOmjRgwPC/view?usp=sharing)

## Data
### Data Scraping
Use CoinMarketCap API to scrape the top 100 coin names by market cap. Use coin names as keywords to scrape related social media data. Use TwitterAPI to scrape the data. End with 79,099 data points. Define keywords for each coin (e.g., 'Bitcoin': ['bitcoin', 'btc', 'bitcoinprice']).

### Network from the Data
The data was processed to construct a multilayer network consisting of two layers: hashtag-hashtag and crypto-crypto. The hashtag-hashtag layer represents connections between hashtags used in tweets, while the crypto-crypto layer represents connections between cryptocurrencies mentioned in tweets.

## Model/Algorithm/Method
### Data Preprocessing
NLTK library is used for text processing including tokenizing and lemmatizing. Other preprocessing is performed including converting to lowercase, removing punctuation, handling negation cues, removing stop words and replacing contractions with their expanded form. Some meaningless words were also removed for data cleaning and only english data were used by filtering non-english text with Langdetect library. After the whole process, 59097 data points were finally used for analysis. 

### Network Analysis
- Modelling: The multilayer network was modeled using the Py3Plex and NetworkX library in Python.

- Centrality: The study computed centrality metrics for each layer of the network, including degree centrality, betweenness centrality, and eigenvector centrality. These metrics were used to identify the most important and influential nodes in the network.

- Community Detection: Community detection was performed to identify groups of nodes that were more densely connected within each layer. The Louvain algorithm was used to detect communities in the network.

### Network Centrality Correlation Analysis
The study investigated the relationship between network centrality metrics and other metrics including sentiment scores, market capitalization and tweet count for each cryptocurrency. Sentiment analysis was performed with the TextBlob library. Correlation analysis was performed to examine the relationship between these metrics and shown in the heatmap.

## Acknowledgements
This project was completed as part of MSIN0074 Network Analysis module of UCL. Special thanks to all the supervisors for the guidance. If you have any questions or comments, feel free to contact me at gracejeonghyeon@gmail.com!
