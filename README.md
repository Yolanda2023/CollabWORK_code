# CollabWORK_code

# Twitter Web Scraping.ipynb

This is an IPython notebook for scraping data from Twitter using Selenium and Python. 

## Requirements
Before running this script, you should install the following Python libraries if they are not installed yet:
- Selenium 
- Google Drive
- pandas
- numpy
- requests
- re
- random
- os
- collections
- nltk
- lxml
- json
- tqdm
- csv
- time
- warnings

You can install them using pip:
```
pip install selenium pandas numpy requests re random os collections nltk lxml json tqdm csv time warnings
```

## Usage

The code provides functions to initialize a browser session, save the scraped data into a .csv file, and perform web scraping on Twitter. 

The script starts by initializing a browser session and opening the Twitter homepage. 

It then scrapes tweets based on specified keywords such as "Democratic Party" and "Republican Party". 

The scraping process involves multiple steps:
1. Rolling down the webpage multiple times to load more tweets.
2. For each tweet found, it retrieves the publisher ID, tweet content, and the time of publishing.
3. It saves these details in a .csv file.

Please modify the paths, file names, and the keywords as per your requirements before running the script. 

Note that the scraping process may take a long time due to the large amount of data on Twitter, and sometimes the script might encounter exceptions when the targeted elements are not found. This usually happens when the page hasn't loaded completely. The script handles these exceptions and continues with the scraping.

Please also make sure you abide by Twitter's policy on data scraping.

## Note
This script works as of the last update on May 23, 2023. Twitter's website structure may change over time, which might make the script outdated. If this happens, please update the xpaths in the script accordingly. 

Please also remember that scraping and using the data should comply with both the website's terms of service and your local laws and regulations.


# Twitter Sentiment Analysis

This notebook applies sentiment analysis to tweets from the Democratic and Republican parties during two time periods: 
2018-2019 and 2022-2023. 
The sentiment analysis is conducted using two methods: VADER and NRC emotion lexicon.

## Installation

pip install nltk


## Data

The data is in CSV format, collected from the following sources:

- `Democratic_alltime_100likes_18-19.csv`
- `Democratic_alltime_100likes_22-23.csv`
- `Republican_alltime_100likes_18-19.csv`
- `Republican_alltime_100likes_22-23.csv`

These files contain the tweets, categorized by party and year.

## Libraries

The following libraries are used:

- `nltk.sentiment.vader`: To conduct sentiment analysis with VADER (Valence Aware Dictionary and sEntiment Reasoner).
- `pandas`: To handle data in DataFrame format.
- `numpy`: To handle numerical computations.
- `tqdm`: To display a progress bar during computations.

## Procedures

1. Import the data and VADER sentiment analyzer.
2. Define a function `vadar_sentiment_analysis()` to calculate the sentiment scores (negative, neutral, positive, and compound) for each tweet.
3. Apply this function to the tweets from each party and year.
4. Calculate the average sentiment compound for each category.
5. Define a function `get_nrc_data()` to retrieve the NRC emotion lexicon.
6. Define a function `emotion_analyzer()` to calculate the emotional content of each tweet.
7. Apply this function to the tweets from each party and year.
8. Calculate the average scores for each emotion for each category.
9. Create word clouds to visualize the most frequent words in the tweets from each category.

## Results

The average sentiment compounds and emotion scores are displayed. They provide insights into the emotional trends in the tweets from the Democratic and Republican parties in 2018-2019 and 2022-2023.

## Further Development

Further analysis can be conducted to compare these trends with significant events during these periods, or to correlate these trends with the popularity of each party or their performance in elections.

## Note

Remember to install the WordCloud package:

pip install wordcloud --user
