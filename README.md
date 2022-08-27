# Crypto Sentiment Analyzer

## Purpose

In this notebook I want to demonstrate some of the VAST functionality python provides for NLP. Since crypto is a hot topic (especially for traders), I chose Bitcoin and Ethereum as a launching point. The main topics I'll cover:

1. [Sentiment Analysis](#1---Sentiment-Analysis)
2. [Natural Language Processing](#2---Natural-Language-Processing)
3. [Named Entity Recognition](#3---Named-Entity-Recognition)


### 1 - Sentiment Analysis

Here we will use a free [newsapi](https://newsapi.org/) to pull the latest news articles for Bitcoin and Ethereum and create DataFrames of sentiment scores for each coin.

Combining this with Pandas, it's SUPER easy to get descriptive statistics like:

> Which coin had the highest mean positive score?
>
> Which coin had the highest negative score?
>
> Which coin had the highest positive score?



### 2 - Natural Language Processing

In this section, I'll will use NLTK (Natural Language Toolkit) and Python to tokenize text, find n-gram counts, and as a bonus create word clouds for both coins (because why not!). 

#### Tokenize

For the NLTK library's tokenizing features to work properly:

1. Lowercase each word.
2. Remove punctuation.
3. Remove stop words.

#### N-grams

Next, I'll look at the ngrams and word frequency for each coin.

1. Use NLTK to produce the ngrams for N = 2.
2. List the top 10 words for each coin.

#### Word Clouds

Finally for a bonus, I'll generate word clouds for each coin to visually summarize the news for each coin.

![btc-word-cloud.png](Images/btc-word-cloud.png)

![eth-word-cloud.png](Images/eth-word-cloud.png)


### 3 - Named Entity Recognition

In this section, I'll build out a fast named entity recognition model for both coins and visualize the tags using SpaCy.

![btc-ner.png](Images/btc-ner.png)

![eth-ner.png](Images/eth-ner.png)



### Resources

[Vader Sentiment Analysis](http://www.nltk.org/howto/sentiment.html)


### Hints and Considerations

The free developer version of the News API limits the total daily requests, so be careful not to exceed the free limits.

I put the code in a notebook so you can copy and paste, play around with it -- build your own models! Use different topics. If you run into snags, go to the documentation for whichever method caused the issue. Walk it a step back and print out the last step's output to see what you're working with. 

It would be *AMAZINGLY* simple to turn this notebook into a cool streamlit app, and let users enter their own news topics (user_news = st.input_text("What news should I analyze?") -- off to the races). Or for your team, you can use the Pandas .to_csv() method to grab your data and use it with Power BI or Tableau to make dashboards... This might be coming to the repo.
