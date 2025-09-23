# Airline Flights Analysis

---
## Contents
Project Overview | Data Source | Tools Used | Table Outlay | Query Languages (SQL) | Visualization

---
## Project Overview:
>> This project explores an airline dataset containing details such as flight, source city, and destination city. The analysis focuses on understanding travel patterns, route popularity, and connectivity between cities. By cleaning and organizing the dataset, exploratory data analysis (EDA) was performed to identify the most frequent flight routes, the busiest source and destination cities, and overall distribution of air traffic. This project demonstrates how simple travel data can reveal insights into passenger movement, city connectivity, and airline operations.

## Data Sources:
www.kaggle.com/dataset

## Tools Used:
+ Pivot Table / Charts
+ PowerBI
+ SQL

## Table Outlay:
First Three Records


| Index | airline | flights | source_city | departure_time | stops | arrival_time | destination_city | class | duration | days_left | price |
|-----|-----|-----|------|-----|-----|-----|------|-----|-----|------|-----|          
| 0 |	SpiceJet | SG-8709 |	Delhi |	Evening	| zero	| Night	| Mumbai | Economy	| 2.17	| 1 |	5953 |
| 1 | SpiceJet | SG-8157 |	Delhi |	Early_Morning |	zero |	Morning |	Mumbai | Economy |	2.33 |	1 |	5953 |
| 2 |	AirAsia |	I5-764 |	Delhi |	Early_Morning |	zero |	Early_Morning | Mumbai |	Economy |	2.17 |	1  |	5956 |
| 3 |	Vistara |	UK-995 |	Delhi |	Morning |	zero |	Afternoon | Mumbai |	Economy |	2.25 |	1 |	5955 |

## Query Language: (SQL)
Some of the query language to retrieve records are displayed here
```SQL
---Retrieve airlines_flights_data Dataset
SELECT * FROM airlines_flights_data;

```
```SQL
---Retrieve number of airlines available
SELECT COUNT (DISTINCT airline) AS 'No_Available_Airline' FROM airlines_flights_data;

```
```SQL
--- Retrieve the most patronized arline

SELECT airline, COUNT (airline) AS 'Total' FROM airlines_flights_data
GROUP BY airline
ORDER BY Total DESC
;

```
```SQL
--- Retrieve most frequent departure time
SELECT departure_time, COUNT (departure_time) AS 'Frequency' FROM airlines_flights_data
GROUP BY departure_time
ORDER BY Frequency DESC;

```
```SQL
---- Retrieve most frequent Arrival time 
SELECT arrival_time,  COUNT(arrival_time) AS 'Frequency' FROM airlines_flights_data
GROUP BY arrival_time
ORDER BY Frequency DESC
; 

```
## Visualization
### Pivot Tables
<img width="860" height="401" alt="pivot_Tables" src="https://github.com/user-attachments/assets/4bdda40c-4c3a-40f5-aa7e-84f56fd90235" />

### PowerBI Dashboard



