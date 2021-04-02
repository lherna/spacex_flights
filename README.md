# SpaceX Flight Outlook

This repository was created to display any interesting findings that could arise from publicly available SpaceX flight data. Using wikipedia as my source of information for this project, the first question arose on how to extract the information in order to work with it, which is the first tackled task.

## Webscrape - Exctracting data through selenium.

Starting from the publicly available flights on wikipedia (2010) up to now, the data was webscraped using python's seleniun version, which was challenging due to the format inconsistency for each datapoint as can be seen below:

<p align="center">
  <img src="https://github.com/lherna/spacex_flights/blob/main/images/spacex_screenshot_short.png" title="spacex_table">
</p>

Extracted, cleaned and formatted, the data was processed through lists and eventually dumped onto a pandas dataframe, ending up in the form shown below:

<p align="center">
  <img src="https://github.com/lherna/spacex_flights/blob/main/images/dataframe_spacex_short.png" title="spacex_dataframe">
</p>

Ready to be analyzed in this form, it was temporarily placed on a database using python's SQL liteweight framework (more formally known as sqlite3).
For a detailed runthrough on the steps taken to perform this first process, please reference the <a href='https://github.com/lherna/spacex_flights/blob/main/Webscrape_SpaceX.ipynb'>Webscrape_SpaceX.ipynb</a> jupyter notebook.

## Data Exploration 

Breaking it down into a couple of parts, once the data was prepared and waiting to be used, the first thing that came to mind was the set of questions posed on the <a href="https://www.kaggle.com/scoleman/spacex-launch-data">Kaggle challenge</a> from which I originally got this idea.

### Launch Progress

Using the information for the date(s) of launch, these were counted and visualized using matplotlib and seaborn. Presented in the findings below, a pattern can be somewhat seen with three peaks in three different years: 2017, 2019 and 2020.

<p align="center">
  <img src="https://github.com/lherna/spacex_flights/blob/main/images/change.png", title="spacex_wordcloud">
</p>

Having the extra ability to consider the description section available on the scraped wiki data, I went ahead and checked to see if there were any interesting insights through the available wordcloud package in python. 

### Wordcloud

The first thing done was to use the data and make a wordcloud using the description column.

<p align="center">
  <img src="https://github.com/lherna/spacex_flights/blob/main/images/spacex_wordcloud.png", title="spacex_wordcloud">
</p>








