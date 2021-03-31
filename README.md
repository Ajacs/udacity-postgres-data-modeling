# Sparkify Data Modeling

## General description and Data Model

Sparkify is a music company that required to know which songs are played at what time, to do this
we have the following schema with this five tables:

* Users:
    - user_id
    - first_name
    - last_name
    - gender
    - level

* Time
    - start_time
    - hour
    - day
    - week
    - month
    - year
    - weekday

* Songs
    - song_id
    - title
    - artist_id
    - year
    - duration

* Artists
    - artist_id
    - name
    - location
    - latitude
    - longitude

* Songplays
    - songplay_id
    - start_time
    - user_id
    - level
    - song_id
    - artist_id
    - session_id
    - location
    - user_agent

In this case our *Fact* table is Songplays because it haves the relationships with the other tables, out *Dimention* tables are *Users, Time, Songs and Artists*.

## Files in the project
The project consists of the following files and folders:

* **data**: Here we have the data in json files that contains the *log_data* and *song_data*
* **create_tables.py**: This file is responsible of the table and schema management, and contains methods for the creation, and deletion for the database and the different tables.
* **sql_queries.py**: Contains all the SQL sentences for the creation and deletion of the tables and the sentences to insert data into the tables.
* **test.ipynb**: Contains SQL sentences to select the data in the tables to verify that the data has been entered correctly.
* **execute_main.ipynb**: This file just executes the *create_tables.py* script.
* **etl.ipynb**: This file helps to understand step by step the process to read, process and save the information contained in the data directory
* **etl.py**: This script contains the methods to process the data in the data directory.

## Executing the scripts
If you're using Jupyter you can run each script clicking in the run button, but if you're in a local developmnet environment, and after installing the dependencies you can run the `.py` scripts with: 

```
python3 {script_name}.py
```