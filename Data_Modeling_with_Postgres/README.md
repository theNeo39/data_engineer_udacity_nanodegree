### Project Overview
---
<br/>
A startup called Sparkify wants to analyze the data they've been collecting on songs and user activity on their new music streaming app. All the data is in JSON format and they would like to have a Postgres database with star schema data modelling to optimize the queries for analysis and bulid ETL pipeline using python.They are particularly interested in understanding what songs users are listening to.

<br/>

### Database Schema
---
<br/>

##### Fact Table

<br/>

**songplays** -records the log data associated with song plays with page NextSong.

> songplay_id, start_time, user_id, level, song_id, artist_id, session_id, location, user_agent

<br/>

##### Dimesion Tables

<br/>

**users** -users in the app

> user_id, first_name, last_name, gender, level

**songs** -songs in music database

> song_id, title, artist_id, year, duration

**artists** -artists in music database

> artist_id, name, location, latitude, longitude

**time** - timestamps of records in songplays broken down into specific units

> start_time, hour, day, week, month, year, weekday 

<br/>

### ETL Pipeline
---
<br/>

1. Extracted the necessary columns from the JSON files.
2. Performing the necessary transformation to get desired information.
3. Loading the data into fact and dimension tables.

<br/>

### Project Files
---
<br/>

* **create_tables.py** - it contains code for setting up the database *sparkifydb* and tables.

* **sql_queries.py** - this contains SQL queries for *creation*, *dropping*, *inserting* table.

* **etl.py** - this has the code to perform necessary operations to load data into tables.

<br/>

### How To Run
---
<br/>

Run the following code in sequence to get perform the ETL 

`python create_tables.py` <br/>
`python etl.py`

<br/>

### References
---
<br/>

* [PostgreSQL Tutorial](https://www.postgresqltutorial.com/)
* [pyscopg Doc](https://www.psycopg.org/docs/)
* [postgreSQL Doc](https://www.postgresql.org/)

