## WomenTechWomenYes(WTWY) - Street Team Placement Analysis 

### Goal
The goal of this project is to analyze the MTA turnstile data in order to provide optimum placement recommendations for street teams to build awareness for the WTWY.  In addition to buiding awareness, the street teams will collect email addresses of individuals who demonstrate a passionate interest in increasing women in technology.  These individuals will be sent an invitation to the annual summer gala fundraising event which will benefit the WTWY organization.
* A min, max and average number of voluteers needed at specific times may be an outcome of this analysis.

### Dataset 
The MTA public turnstyle data set will be used for this analysis.  The data is segmented in 4-hour increments.  Time frames for exit data between 4:00am and 8:00am may indicate arrival at the office and entry data between 4:00pm(16:00) AND 8:00pm(20:00) could idicate return from the office.  These time frames may capture working professions on their work commute.  Focusing on exit data in am may be the best souce as commuters won't be rushing to a train and have time to learn aboutu WTWY>. Note: The Pandemic may have a negative impace on these assumptions as work from home is becoming more popular.

Stretch Goal: If available merging the MTA data with major tech employers office location and proximity to stations could be valuable to fine tune street team placement. 

### MVP Goal:
  A visualization of the data indicating the stations with the highest exit traffic between the hours of 4:00am and 8:00am using SQLite.



Data Description:  THE MTA DATA IS ORGANIZED BY 

What dataset(s) do you plan to use, and how will you obtain the data? 
MTA DATA, DOWNLOADED FROM THE MTA WEBSITE, IF AVAIALBLE MAJOR TECH EMPLOYER LOCATIONS PROXIMITY TO STATIONS, IF AVAILABLE AFFLUENT NEIGHBORHOOD DATA

What is an individual sample/unit of analysis in this project? 

What characteristics/features do you expect to work with? SCP, STATION, LINENAME, TIME, EXITS, ENTRIES

If modeling, what will you predict as your target? 
STATIONS WITH HIGHEST EXITS BETWEEN 4:00AM AND 8:00AM AND HIGHEST ENTRIES BETWEEN 4:00PM(16:00) AND 8:00PM(20:00)
POTENTIALLY STATIONS SERVED MULTIPLE LINES(INTERSECTION)

Tools:

How do you intend to meet the tools requirement of the project? PYTHON, VISUALIZATION TOOLS TBD

Are you planning in advance to need or use additional tools beyond those required?

MVP Goal:

A VISUALIZATION OF THE DATA INDICATING THE LOCATIONS WITH THE HIGHEST TRAFFIC STATIONS
MAP OF THE SUBWAY STATIONS MARKED WITH A RED DOT OF WHERE TO PLACE THE VOLUNTEERS
A SCHEDULE FOR VOLUNTEERS TO BE AT THE STATION
