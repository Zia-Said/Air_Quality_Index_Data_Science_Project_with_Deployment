## Predicting Air Quality Index (Data Science Project with Deployment)

### Link (Deployed in Heroku): https://airqualitydatascienceproject.herokuapp.com/

### Data Source: https://en.tutiempo.net/ & https://openweathermap.org/

The first website was scrapped as in Html_script.py for collecting weather data (from 2013 to 2018) related to New Delhi (The Capital of India).
The data columns were as following:
T	Average Temperature (°C)
TM	Maximum temperature (°C)
Tm	Minimum temperature (°C)
SLP	Atmospheric pressure at sea level (hPa)
H	Average relative humidity (%)
PP	Total rainfall and / or snowmelt (mm)
VV	Average visibility (Km)
V	Average wind speed (Km/h)
VM	Maximum sustained wind speed (Km/h)
VG	Maximum speed of wind (Km/h)
RA	Indicate if there was rain or drizzle (In the monthly average, total days it rained)
SN	Snow indicator (In the monthly average, total days that snowed)
TS	Indicates whether there storm (In the monthly average, Total days with thunderstorm)
FG	Indicates whether there was fog (In the monthly average, Total days with fog)

The html pages for each month in the years first downloaded to our local environment by Requests Library and then Beautiful Soup Library was applied to extract the data as in Plot_AQI.py and Extract_combine.py and saved in different csv files. 
The dependent feature (PM 2.5) values were bought from the second website and then combined with the data in the previously created csv files and finally one large file (Real_combine) was generated containing all the required values for the project.

The data was further investigated by exploratory data analysis and feature selection was employed as in the Jupyter Notebooks in the Entire Project Folder. In addition, several machine learning models were developed to predict the air quality index including linear regression, lasso regression, decision tree, random forest, xgboost and K nearest neighbor regressor. Random forest and xgboost showed the best performance. Accordingly, we chose random forest model to be deployed in Heroku.
