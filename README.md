# Vacation Planning at Hawaii
## Overview
Hawaii is known for one of the best places in the world for vacation, thanks to its evergreen islands and extremely comfortable weather. In this repository, Hawaii weather parameters such as precipitation and temperature are analyzed to see if the weather of the pre-picked vacation dates is good or not.
  
![Hawaii Image - Henry Le](/Images/Hawaii.jpg)
  
## Workflow  
* Establish connection between Jupyter Notebook and SQL_Lite Database  
* Perform Precipitation Analysis:
    - Retrieve data during the past 12 months (from the latest available date)  
    - Plot total rainfall over time  
    - Perform quick statistical analysis on the rainfall data (mean, max, min, count, etc.)  
    
* Perform Station Analysis:  
    - Produce a comprehensive list of all available stations and number of records  
    - Identify the most active weather station by most data amount recorded  
            - Calculate max, min, average temperature  
            - Plot the temperature histogram  
   
* Perform weather analysis based on the historical data during planned vacation dates  
    - Calculate max, min, average temperature  
    - Plot a bar chart showing average temperature with error bar  
    - Create a table store ID, Total Rainfall, Name, Longitude, Latitude, Elevation of all stations  
    - Investigate the consistency of Hawaii weather throughout the year by:  
             - Retrieve temperature all available data of the same months of Jun and Dec in all years   
             - Perform T-test to determine the statistical significance of both month weather conditions    
    - Plot temperature max, min, average for the entire duration of the vacation trip  

* Build an Application Programming Interface (API) to get access to entire database with JSON format  

## Tools and Techniques
* Python | Pandas | SQLAlchemy | Flask | Matplotlib | Pyplot | Statistics | API  
* Advance Query with Engine, create session to retrieve data  
* Merge table, convert query to dataframe, perform query functions  
* List Comprehension, datetime<=>string conversion
* Plot data by bar chart, line chart, histogram, with "fivethirtyeight" style matplotlib


## Table of Contents  
* **Images** ::  folder contains all images of exported graphs and readme image  
* **Resources**  ::  folder contains datafile of Hawaii weather   
  - **hawaii.sqlite**  ::  SQL database with two tables - *measurement* and *station*   
  - **hawaii_measurements.csv**  ::  contains columns : *station, date, prcp*   
  - **hawaii_stations.csv**  ::  contains columns : *station, name, latitude, longitude, elevation*    
* **.gitignore**  ::  archive of not uploaded file name
* **README.md**  ::  markdown readme file of this repository
* **app.py**  ::  source codes to create API app from Python Flask
* **climate.ipynb**  ::  source codes of all weather analysis of Hawaii
