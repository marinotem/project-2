# project-2
This is our analysis of homicides vs. weather conditions to see if there is a correlation between weather such as humidity, events and temperature with homicide rates.

Our process began by choosing four datasets to use in order to answer our question. 
1. Homicide dataset that provides all homicides from USA from 1980-2014 from Kaggle.
2. Temperature dataset that provides temperatures for 28 cities in USA from 2012-2017 from Kaggle.
3. Weather dataset that provides weather condiitons for 28 cities in USA from 2012-2017 from Kaggle.
4. Humidity dataset that provides humidity for 28 cities in USA from Kaggle from 2012-2017 from Kaggle.

CLEANING

Clean Homicide Dataset
We dropped all unnecesary years to only leave us with the same years that are available in the weather datasets, so 2012-2014.
Dropped all unnecesary columns to only leave city, date, and the homicide incident.

Clean Temperature Dataset
Dropped all the years outside of 2012-2014
Converted datetime metric into two columns: month and year
The city names were columns so we had to switch it to rows using melt function
THen we created a new dataframe that averaged the temperature per month.

Clean Weather Dataset
Dropped all the years outside of 2012-2014
Converted datetime metric into two columns: month and year
The city names were columns so we had to switch it to rows using melt function
Then we created a new dataframe that pulled the mode of for each month to have the most common weather type for each month. 
We realized that some weather events had more than one value so we had to force our dataset to only choose one. 

Clean Humidity Dataset
Dropped all the years outside of 2012-2014
Converted datetime metric into two columns: month and year
The city names were columns so we had to switch it to rows using melt function
THen we created a new dataframe that averaged the humidity per month.

JOINING
We did an inner join on city, month, and year for all four datasets to merge together. 

Created our schemata for our new database (which can be found in our repo).
then created the tables in PGadmin (which can be found in our repo)
After merging the datasets and creating one database we were able to transition it into our PGadmin, post GRESQL

*Some of our csv files are too big, so the Resources folder is included in the .gitignore file incase if needed
