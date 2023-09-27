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
* ride_id, character, unique primary key for each ride trip
* rideable_type, character, the type of bike used in bike trip
* started_at, time-date data, the starting date and time for each bike trip
* ended_at, time-date data, the ending date and time for each bike trip
* start_station_name, character, starting station name for the bike trip
* start_station_id, character, ID used for identifying starting station
* end_station_name, character, ending station name for the bike trip
* end_station_id, character, ID used for identifying ending station
* start_lat, geographic data, latitude of starting station of the bike trip
* start_lng, geographic data, longitude of starting station of the bike trip
* end_lat, geographic data, latitude of ending station of the bike trip
* end_lng, geographic data, longitude of ending station of the bike trip
* member_casual, character, the member status of bike user, fell into only casual (user) and member

#### Excel
For formating our data we can use Power Query and this tool can automatic process to combine files in a single, but we can use programmer languagues to create one fast process.
For using this we can go in this:
* PICTURE

After rename our datafiles.


#### R
Similar in Power Query, we can solve our problem in fast way. Import our CSV and renamed.
After rename, we can wrangle data and combine into a single file.
* PICTURE

To exam our process, we use this command:
* insert line code

  For see the head of the combined dataset, we use this command:
* insert line code


### SQL
TEste7


## Analyze
TEste8

# Share
Teste9

# Act
Teste10
