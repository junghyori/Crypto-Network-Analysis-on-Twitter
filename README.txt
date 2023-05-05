# Analysing Cryptocurrency Communities on Twitter : A Multilayer Network Study

This project involves the analysis of cryptocurrency communities on Twitter using a multilayer network approach. The study investigates the interplay between the hashtag-hashtag layer and the crypto-crypto layer, and explores how these layers are related to network centrality and community detection. The results provide valuable insights for investors, traders, and businesses looking to make informed decisions in the cryptocurrency market.

This README file does not cover the details on the method and result. Please check the details on the project and analysis result in the submitted report.

-----------------------------------------------------------------------------------
## README Contents:
    - Folder structure
    - How to use this folder
    - File descriptions
  
-----------------------------------------------------------------------------------
## Folder structure:

This folder contains 6 files, of the formats .ipynb, .csv and .txt and is structured as follows. The number beside each file name is referred back to in the descriptions of each file given in the 'file description' 

    (1) 1_Data Scraping.ipynb
    (2) 2_Data Preprocessing.ipynb
    (3) 3_Multilayer Network Analysis.ipynb
    (4) 4_Centrality Correlation Analysis.ipynb
    (5) twitter_concat.csv
    README.txt
    
-----------------------------------------------------------------------------------
## How to use this folder (to reproduce results discussed in the accompanying report):

There are 4 notebooks, which are all implementations of experiments discussed in the research, including data scraping and processing, building and analysing the network.

The running procedures starts from the 1_Data Scraping.ipynb > 2_Data Preprocessing.ipynb > 3_Multilayer Network Analysis.ipynb > 4_Centrality Correlation Analysis.ipynb. To replicate results discussed in the research, it will suffice to run the notebooks with necessary dependencies installed except for the data scraping, someone who want to replicate it should use their own API keys.

-----------------------------------------------------------------------------------
## File descriptions:

    (1)   File name: 1_Data Scraping.ipynb
          File type: Jupyter notebook
          File contents: This file contains data scraping with API from CoinMarketCap and Twitter. CoinMarketCap API is used to
          scrape the top 100 coin names by market cap. These coin names are used as keywords to scrape related social media data
          using TwitterAPI which end with 79,099 data points. 
          
    (2)   File name: data_processing.ipynb
          File type: Jupyter notebook
          File contents: This file imports data from the (1) as 'twitter_concat.csv'. The main function in this file is text
          processing. This includes converting to lowercase, removing punctuation, handling negation cues, removing stop words and
          replacing contractions with their expanded form, tokenizing and lemmatizing with NLTK library. Some meaningless words
          were also removed for data cleaning and only english data were used by filtering non-english text with Langdetect
          library. After the whole process, 59097 data points were finally used for the analysis.
    
    (3)   File name: 3_Multilayer Network Analysis.ipynb
          File type: Jupyter notebook
          File contents: This file imports preprocessed data from (2) and performs modelling: The multilayer network was modeled
          using the Py3Plex and NetworkX library in Python. There are mainly 3 parts: Multilayer Network (the whole network),
          Hashtag-Hashtag Layer and Crypto-Crypto Layer. For each part, centrality metrics were computed for each layer of the
          network and community detection was performed.
         
    (4)   File name: 4_Centrality Correlation Analysis.ipynb
          File type: Jupyter notebook
          File contents: This file imports centrality measures in Crypto-Crypto Layer calculated from (3) and investigated the
          relationship between network centrality metrics and other metrics including sentiment scores, market capitalization and
          tweet count for each cryptocurrency. Sentiment analysis was performed with the TextBlob library. Correlation analysis
          was performed to examine the relationship between these metrics and shown in the heatmap.
                 
    (5)   File name: twitter_concat.csv
          File type: CSV
          File contents: This is the key dataset used in the study generated from (1).