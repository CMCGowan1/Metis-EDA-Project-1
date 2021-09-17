# Subway Station Analysis for Street Team Placement for WomenTechWomenYes (WTWY)

Cheryl McGowan

### Abstract

The goal of this project is to use the publicly available MTA subway turnstile dataset to identify optimum locations for the WomenTechWomenYes organization for placement of street teams to maximize email address collection points in NYC.  The data was cleaned up for reverse station entries, duplicates and outliers.  The information was plotted on a bar graph using Matplotlib and a subset of the STATION data focused on Big Tech Office locations was graphed using Seaborne.  I compared the stations with the most traffic to commercial real estate maps showing the locations of big tech and start-up tech companies. The commercial data is based on lease activity and real estate purchases for the tech sector companies Amazon, Apple, Facebook, Google and Netflix.  A recommendation for 15 total street teams is made and the teams are assigned to best cover the stations with the most traffic close to Big tech Office locations.   

### Design

This project originates as a client request from WTWY.  The design of the project focused on filtering and summing the data for cumulative daily entries.  This data was used to identify stations with the highest volume of traffic.  This station list was then compared to Big Tech Office locations and a subset of stations was identified with close proximity to Big Tech Office locations.  This dataset was used to make recommendations to WTWY for an optimum number of street teams of 15 to cover offices for Google, Amazon, Apple, Facebook and Netflix.  

### Data

The data is provided by the Metro Transit Authority (MTA) with each row representing turnstile data collected in approximately 4 hour increments.  The data has some irregularities regarding data collected in reverse order resulting in negative totals, duplicate entries and abnormally high values that skewed the analysis.  These incidences were identified and corrected or removed from the data set.  The dataset contains records for a little over 8 months from Jan 1, 2021 to Sept 3, 2021.  It has over 7 million entries or rows from 379 stations.  One observation is the cumulative number of daily entries collected at a turnstile for a 24 hour period. The features of this data are C/A UNIT, SCP, STATION, LINENAME, DIVISION, DATE, TIME, DESC, ENTRIES AND EXITS.  The primary ket consists of C/A UNIT, SCP, STATION, and a new column for DATETIME.

C/A      = Control Area (A002)
UNIT     = Remote Unit for a station (R051)
SCP      = Subunit Channel Position represents an specific address for a device (02-00-00)
STATION  = Represents the station name the device is located at
LINENAME = Represents all train lines that can be boarded at this station
           Normally lines are represented by one character.  LINENAME 456NQR repersents train server for 4, 5, 6, N, Q, and R trains.
DIVISION = Represents the Line originally the station belonged to BMT, IRT, or IND   
DATE     = Represents the date (MM-DD-YY)
TIME     = Represents the time (hh:mm:ss) for a scheduled audit event
DESc     = Represent the "REGULAR" scheduled audit event (Normally occurs every 4 hours)
           1. Audits may occur more that 4 hours due to planning, or troubleshooting activities.
           2. Additionally, there may be a "RECOVR AUD" entry: This refers to a missed audit that was recovered.
ENTRIES  = The comulative entry register value for a device
EXIST    = The cumulative exit register value for a device

### Algorithms

Calculations for DAILY_ENTRIES are shown in the column headers.

### Tools

The data science tools utilized are SQLite, pandas, matplotlib, and seaborne.

### Communication

Model Evaluation and Selection

Bar charts were created to show station volume for top stations and for stations in the Big Tech Office locations areas.  Future analysis is needed to identify data sets for commercial real estate to be used to update the maps for refining optimal street team placement.
