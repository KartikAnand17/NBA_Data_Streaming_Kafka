# NBA Data Streaming Using Spark Structured Streaming, Kafka, Reddit API

### Introduction
This project focuses on implementing a specified data processing workflow using the Reddit platform as the data source. We adhere closely to the outlined project requirements by streaming real-time comments from the 'nba' subreddit using PRAW (Python Reddit API Wrapper). The goal is to analyze these comments for named entity recognition, count occurrences, and visualize the data using a series of interconnected technologies.

### Architecture


### About Dataset/API
The data is sourced from Reddit, specifically the 'nba' subreddit, which provides a continuous stream of user comments. We use PRAW for its efficient 
access to Reddit’s API, enabling real-time data streaming.

###  System Configuration
We serialize incoming data into JSON and send it to a Kafka topic named 'topic1'. This approach ensures that our data pipeline is robust and prepared for high-volume data flows.

### Data Processing
Our PySpark application processes the stream from 'topic1'. It identifies and counts named entities within the comments, 
aligning with the task of understanding community focus within the NBA discussions.

### Data Transmission and Visualization 
We transfer the processed data to another Kafka topic, 'topic2'. From there, Logstash forwards this data to Elasticsearch, which we then visualize in Kibana as a bar plot of the most frequently mentioned named entities.



