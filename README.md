# ETLproject
ETL group project


## Data Cleanup & Analysis


* The sources of data extracted:


https://www.kaggle.com/amanarora/obesity-among-adults-by-country-19752016
https://data.world/moosechris/gdp-1960-to-2015

* The type of transformation needed for this data (cleaning, joining, filtering, aggregating, etc).
clean null values
clean data in rows so it's more readable (drop error measures from obesity percentage)
Rename countrie so joining works properly

* Load the data into a relational database -- PostgreSQL

* The final tables or collections that will be used in the production database:

Obesity table
GDP table 



## Project Report

Extract:
we obtained our data from kaggle.com and data.world. Both of these data sources provided us with CSV's. 

Transform:
The first step was cleaning the data by removing any null values. After that we looked at columns and looked for areas that could affect readability. The obesity dataset that was provided had error measures in the obesity_percentage column. In order to keep these error measures from distracting users we decided to completely remove these error measures from the dataset. We used Pandas in order to do this. Additionally, we realized that in one CSV the United States was entered as "United States of America". Since this could impede our joins in SQL and pandas we changed the name to "United States". 

Load:
We loaded the final database into PostgreSQL because there were many relations between the two tables. 
The tables we settled on are as follows:
Obesity and GDP. 
Additionally we created a view joining Obesity and GDP for the United States. 
