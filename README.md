# Exploratory Data Analysis with Yelp in R
<img src="yelp.png">

### Why Yelp?

Becuase of Yelp Dataset Chanllenge!! This dataset (https://www.yelp.com/dataset/challenge) is plublicly available as part of the Yelp Dataset Challenge. This set includes information about local businesses in 11 metropolitan areas across 4 countries. 

There are five documents in that dataset: business.JSON, checkin.JSON, review.Json, tip.JSON, user.JSON. Because of large volume of data and limitation of my computer, I only used two of them: business and review.

### Part 1: Data Collection and Processing

**Read JSON Data Files**

These JSON files are actually called ‘NDJSON (Newline delimited JSON)’, which means there are multiple JSON values inside this file and each of the JSON values is considered as an independent object. Therefore, we need to use **stream_in()** function to read data into R.

Command: **business <- stream_in(file("business.json"))**

JSON data is nested and hierarchical so it is a bit confusing for analyzing data in R. I used **flatten()** to eliminate the structure.

**Data Cleaning and Storing**
Since I only focused on restaurant and food part, I removed unnecessary observations and saved them into CSV files. Detailed process shows in R file.

### Part 2: Data Analysis

**Analysis about Restaurant Ratings**

* What's the distribution of ratings?
* What is average ratings by state?
* What are the top 10 highest ratings restaurants and where are they located?
* What's the relationship between ratings and price range?

**Analysis about User Reviews**

* Which restaurants have most 5-star reviews and which have most 1-star reviews from users?
* What are the top 10 most common words appeared in the reviews of "Mon Ami Gabi"?
* Sentiment Analysis

### Part 3: Conclusions
Findings

