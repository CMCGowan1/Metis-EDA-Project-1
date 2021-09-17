## WomenTechWomenYes(WTWY) - Street Team Placement Analysis 

### Goal
The goal of this project is to analyze the MTA turnstile data in order to provide optimum placement recommendations for street teams to build awareness for the WTWY.  In addition to buiding awareness, the street teams will collect email addresses of individuals who demonstrate a passionate interest in increasing women in technology.  These individuals will be sent an invitation to the annual summer gala fundraising event which will benefit the WTWY organization.
* A min, max and average number of voluteers needed at specific times may be an outcome of this analysis.

### Dataset and Description
The MTA public turnstile data set will be used for this analysis.  The project will use several characteristics including SCP, STATION, LINENAME, TIME, EXITS, ENTRIES.  The data is segmented in 4-hour increments.  Time frames for exit data between 4:00am and 8:00am may indicate arrival at the office and entry data between 4:00pm(16:00) AND 8:00pm(20:00) could idicate return from the office.  These time frames may capture working professions on their work commute.  Focusing on exit data in am may be the best souce as commuters won't be rushing to a train and have time to learn about WTWY. 
* Note: The Pandemic may have a negative impace on these assumptions as work from home is becoming more popular.
* Stretch Goal: If available merging the MTA data with major tech employers office location and proximity to stations could be valuable to fine tune street team placement. Affluent neighboorhood data, if available may be helpful to correlate with the entry data for return commute.
* The individual sample unit of data is turnstile by station.

### Tools
SQLite, pandas, matplotlib

### MVP Goal:
  A visualization of the data indicating the stations with the highest exit traffic between the hours of 4:00am and 8:00am using SQLite. 

