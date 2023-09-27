# Cyclistic-Case-Study
Google Data Analytics Capstone: Case Study

## Introduction
In Cyclistic bike-share, while working with a junior data analyst, we need to understand how the company works. 
It's very important to understand the process in analysis: ask, prepare, process, analyze, share, and act. 
After running through all these processes, we can understand the marketing analyst team at Cyclistic, a bike-share company in Chicago

### Scenario and Company
Working with the marketing analyst team at Cyclistic, the director of marketing believes the company needs to maximize the number of annual memberships. 
We need to understand how casual riders and annual members use Cyclistic bikes differently. The company started in 2016 and launched a successful bike-share offering. 
The objective in this analysis is to convert casual riders into members.

## Ask
### Questions
In this process we have 3 questions that guide this marketing program:
1. How do annual members and casual riders use Cyclistic bikes differentyly?
2. Why would casual riders buy Cyclistic annual memberships?
3. How can Cyclistic use digital media to influence casual riders to become members?


## Prepare
After answering the questions, we run this process to prepare our data.
The dataset is located on an AWS file server where the zip files are, and we need to download and store them locally on the desktop.
In this phase, we need to understand our data and see if it is secure.

After that we need understand the credibility and integrity of the data - ROCCC
* Reliablity
* Originality
* Comprehensiveness
* Current
* Cited

## Process
### Data Cleaning
The format our data is CSV. All the table we have same set of column names:
* ride_id;
* rideable_type;
* started_at;
* ended_at;
* start_station_name;
* start_station_id;
* end_station_name;
* end_station_id;
* start_lat;
* start_lng;
* end_lat;
* end_lng;
* member_casual;

#### Excel
For formating our data we can use Power Query and this tool can automatic process to combine files in a single, but we can use programmer languagues to create one fast process.
For using this we can go in this:

![Power Query](images/01_Power_Query-Get-Data.png)
![Power Query](images/01_Power_Query-Transform.png)

* Wait: Use this method is not recommend because we had a lot rows and maximum number of rows in Power Query is limitation in 1,048,576.
* To use this tool we need divide in multiples files and because this is most recommend use programmer. And in this case we use R or SQL.

#### R
Similar in Power Query, we can solve our problem in fast way. Import our CSV and renamed.
After rename, we can wrangle data and combine into a single file.

To read and rename our data we use this command:

```
jan21 <- read_csv('202101-divvy-tripdata.csv')
```

To exam our process, we use this command:

```
colnames(jan21)
```

To compare our dataset file we use this command:

```
compare_df_cols(jan21, fev21, mar21, apr21, may21, jun21, jul21, aug21, sep21, oct21, nov21, dec21)
```

After we see than our data is uniform we can combined our data in single dataset file:
  
```
divvy_tripdata_raw<- rbind(jan21, feb21, mar21, apr21, may21, jun21, jul21, aug21, sep21, oct21, nov21, dec21)
```

For see the head of the combined dataset, we use this command:

```
head(divvy_tripdata_raw)
```

And least command is this process, we can see examined our data using this comamand:

```
dim(divvy_tripdata_raw)
```

In the clean process data for analysis to prepare we can use the strptime() and after that, we can use str() to show effective.
To removed unneecssary data we can use filter()

* Finalized our data cleaning process we can export the csv file to realized analysis in Tableau.





### SQL

Similar when we used R, in data cleaning we can use SQL to combine and clean our data.
In this case, we use BigQuery`s and une the UNION operator to combine all the files into one table with the name "2021_tripdata"
```
SELECT
      ride_id, 
      rideable_type,
      started_at,
      ended_at,
      start_station_name,
      start_station_id,
      end_station_name,
      end_station_id,
      start_lat,
      start_lng,
      end_lat,
      end_lng,
      member_casual
FROM course50.cyclistic.202101
UNION ALL
SELECT
      ride_id, 
      rideable_type,
      started_at,
      ended_at,
      start_station_name,
      start_station_id,
      end_station_name,
      end_station_id,
      start_lat,
      start_lng,
      end_lat,
      end_lng,
      member_casual
FROM course50.cyclistic.202102
UNION ALL
SELECT
      ride_id, 
      rideable_type,
      started_at,
      ended_at,
      start_station_name,
      start_station_id,
      end_station_name,
      end_station_id,
      start_lat,
      start_lng,
      end_lat,
      end_lng,
      member_casual
FROM course50.cyclistic.202102
```
* REPETY THE UNION ALL COMMAND TO ALL OUR 12 FILES or MORE IF YOU WANT.

* To found no misspelling or issue use this command:

```
SELECT DISTINCT [string column]
FROM course50.cyclistic.bikeshare
```




## Analyze
### R



# Share
Teste9

# Act
Teste10
