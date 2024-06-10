# Sparkify Database

## Purpose

The purpose of the Sparkify Database acts as a foundation for analytical insights for the startup business Sparkify, a music streaming service. By analyzing user interactions with songs such as which songs are played most often, user engagement, and other metrics, Sparkify can gain valuable insights int what their useres preferences are. These insights van be used to improve user experiences and frive future business decisions. 

## Database Schema Design

The database schema is designed with a star schema to optimize queries and simplify data analysis. It consists of the following tables:
### 1. Fact Table:
songplays - Records in the log data associated with song plays
### 2. Dimension Tables:
Users - Users of the sparkify app
Songs - Songs available in the Sparkify library
Artists - Artists of the songs in the Sparkify library
Time - Timestamps of records in songplays broken down into specific unit

# ETL Pipeline
The ETL pipeline is implemented to populate the database from raw data files. The process is as follows:
## Extract
Raw data files are extracted from the data directory, which contains both song data and log data in JSON format.
## Transform
Song data files are processed to extract song and artist information and populate the songs and artist tables.
Log data files are processed to extract user information, timestamp information, and songlplay details. These are used to populate the users, time, and songplays tables
## Load
Processed data is loaded into the respective tables in the PostgreSQL database.

# Steps for running 
## Run create_tables.py
This drops any tables that already exist and creates new tables.
## Run etl.py to process data and load it into the tables
This step processes data for loading, extracting, and inserting it into appropriate tables.
## Run test.ipynb to confirm creation of database and existence of data.