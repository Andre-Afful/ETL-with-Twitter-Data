# ETL-with-Twitter-Data

## Task Overview

This task was based on basic ETL using twitter data and was divided in two parts. The first part of the task required scraping the tweets and then storing the output in Comma Separated Values file. Part 2 of this task deals with extracting and storing the tweets into a collection in MongoDB.

### Part 1

Write a script that downloads tweets data on a specific search topic using the standard search API. The script should contain the following functions:

1. scrape_tweets() that has the following parameters:

    * Search topic
    * The number of tweets to download per request
    * The number of requests  
    
    and returns a dataframe.
2. Save_results_as_csv() that has the following parameters:
    1. the dataframe from the above function  
    And returns a csv file with the following naming format:

    *tweets_downloaded_yymmdd_hhmmss.csv (where ‘yymmdd_hhmmss’ is the current  timestamp)*

The following attributes of the tweets should be extracted:

* Tweet text
* Tweet id
* Source
* Coordinates
* Retweet count
* Likes count
* User info
    - Username
    - Screenname
    - Location
    - Friends count
    - Verification status
    - Description
    - Followers count

Make sure to not include retweets.  
Make sure you the same tweets appearing multiple times in your final csv.

### Part 2

Create a MongoDB database called Tweets_db and store the extracted tweets into a collection named: raw_tweets.


## Requirements

* Twitter Developer Account
* Twitter API credentials


## Setting Up

This project was carried out using the follwing
* Python 3.6
* Anaconda
* Pandas
* Tweepy
* MongoDB
* Pymongo

### Create and activate environment

Create and activate the conda environment using the following commands;

```
conda create -n "env-name" python=3.6
```

```
conda activate env-name
```

### Install packages used for project

Using the following command;

```
pip install -r requirements.txt
```

## Resources

### Documentations

- [Twitter Search API](https://developer.twitter.com/en/docs/twitter-api/v1/tweets/search/api-reference/get-search-tweets)
- [Tweepy Doc](http://docs.tweepy.org/en/latest/index.html)
- [Pymongo Doc](https://pymongo.readthedocs.io/en/stable/)

### Research/ Tutorial Articles
- [Scraping Tweets With Tweepy Python](https://medium.com/python-in-plain-english/scraping-tweets-with-tweepy-python-59413046e788)


