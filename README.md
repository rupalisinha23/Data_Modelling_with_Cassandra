# Data Modelling with Apache Cassandra
:raising_hand: This project performs ETL operations using Apache Cassandra. First, we preprocess the data from csv files. Then we model Cassandra tables using the given three queries. At the end, we drop the tables and close the connection to the cassandra server.

### Data
Put all the given csv files inside the folder **event_data**. <br>
Once you will run the code for preprocessing in the jupyter notebook, the csv file **event_datafile_new.csv** will be generated. 
The csv data looks like: <br><br>
![data](images/image_event_datafile_new.jpg)

### Prerequisites
- Python 3.5+ --> Download from here https://www.python.org/downloads/
- Apache Cassandra --> Download from here http://cassandra.apache.org/

### Data Modelling
There are three queries provided on whose basis we have created three tables:

```
SELECT artist, song, length 
    FROM songinfo_by_session 
    WHERE sessionId=338 AND itemInSession = 4;
```
```
SELECT artist, song, firstName, lastName 
    FROM artistinfo_by_session 
    WHERE userId=10 AND sessionId = 182;
```
```
SELECT firstName, lastName
    FROM music_info 
    WHERE song='All Hands Against His Own';
```

### Running the project
Open **project_cassandra.ipynb** notebook and execute each cell.

### Authors
* **Rupali Sinha** - *Initial work*
