# SpaceX Flight Outlook

## Webscrape - Exctracting data through selenium.

This repository was created to display any interesting findings on SpaceX flight data. Starting from the publicly available flights on wikipedia (2010) up to now, the data was webscraped using python's seleniun version, which was challenging due to the format inconsistency for each datapoint as can be seen below:

<p align="center">
  <img src="https://github.com/lherna/spacex_flights/blob/main/images/spacex_screenshot_short.png" title="spacex_table">
</p>

Extracted, cleaned and formatted, the data was processed through lists and eventually dumped onto a pandas dataframe, ending up in the form shown below:

<p align="center">
  <img src="https://github.com/lherna/spacex_flights/blob/main/images/dataframe_spacex_short.png" title="spacex_dataframe">
</p>

Ready to be analyzed in this form, it was temporarily placed on a database using python's SQL liteweight framework (more formally known as sqlite3).

## Analysis 

Breaking it down into two parts, once the data was prepared and waiting to be used, I contemplated on what could be done with it. Starting off with the description provided for each of the flights, I used this data to generate a wordcloud.

### Wordcloud

The first thing done was to use the data and make a wordcloud using the description column.

<p align="center">
  <img src="https://github.com/lherna/spacex_flights/blob/main/images/spacex_wordcloud.png", title="spacex_wordcloud">
</p>
