# Data Modeling with Cassandra

## **Project Overview**
A startup called Sparkify wants to analyze the data they've been collecting on songs and user activity on their new music streaming app. The analysis team is particularly interested in understanding what songs users are listening to. Currently, there is no easy way to query the data to generate the results, since the data reside in a directory of CSV files on user activity on the app. This project requires data modeling with Apache Cassandra and an ETL pipeline using Python.

## **Dataset**
We have one dataset as csv files ```event_data```

## **Data Modeling**
In Apache Cassandra we always think about queries first when modeling the data. Once we know what type of queries we are interested in, then we start building the models to create tables.
> its preferable to have one query one table approach  

## **Business Logic**
1. Get the song details in music app history for a particular session.
2. Get the name of artist and songs played by the particular user in specific session.
3. Get all the users who listened to specific song.

## **ETL Pipeline**
1. Append all the csv files into one file as read operation would be easy.
2. Extracted necessary columns from the csv file.
3. Created tables with ```partition and clustered keys``` based on the queries we need. 

## **How To Run**
Execute all the cells in the jupyter notebook ```Project_1B_Project_Template.ipynb```



