# Dataset Description
The dataset consists of the following key attributes:
- track_id: Unique identifier for each track
- track_name: Name of the song
- artist: Name of the artist who performed the track
- duration: Length of the song in milliseconds
- popularity: A numerical value indicating the track’s popularity
- source: https://www.kaggle.com/datasets/tonygordonjr/spotify-dataset-2023
# Workflow and Techniques Used

## 1. Data Storage
- The dataset is stored in HDFS (/user/hadoop/dataset/spotify_data.csv) to enable distributed storage and processing.

## 2. Data Preprocessing with Apache Pig
- The raw dataset is loaded into Pig for preprocessing.
- Cleaning steps include filtering out null values and inconsistent data.
- Aggregation is performed to compute average track popularity per artist.
- The cleaned and aggregated data is stored back in HDFS (/user/hadoop/output/spotify_cleaned).

## 3. Data Analysis wit Hive
- A Hive table is created to store the structured dataset.
- Data is loaded from HDFS into Hive for querying.
- Three key queries are executed to analyze the dataset:
1. Identifying the top 5 most popular tracks.
2. Computing the average popularity of tracks per artist.
3. Finding the total number of tracks per artist.

## 4. Query Results and Export
- The results of Hive queries are stored back into HDFS for further use.
- The processed data can be exported and visualized for deeper insights.
