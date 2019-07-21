# DEP Noise Scheduling
This project aims at creating using features based on the location and times of the complaints to be able to guess whether
new complaints will be enforcable or not. 

## This notebook is divided into three sections:

### Feature Engineering
The first section deals with getting 2016 complaints and features related to each complaint. Here we join the complaints to:
* American Community Survey(ACS) based on the location of complaints
* Primary Land Use Tax Lot Output(PLUTO) based on the location of complaints
* NOAA Weather data based on the time of complaints
* After Hour Variance(AHV) permits: AHV permits are what allow construction jobs to take place after hours. A construction taking place after this without a permit would be enforceable by the DEP. These permits are not publicly available so we had to make use of a scraper to obtain these permits. Assigning AHV permits to complaints was done in another notebook.

A key step in the feature engineering was mapping the resolution description of the closed complaints to 1 or 2 based on enforceability. For example the ""

### Modelling
In the second section we test out models to maximize the F1-Score which is the harmonic mean between Precision and Accuracy. The problem we faced with the the data was that by

### Testing on newer data
The third section uses the model trained on 2016 data and tests it on the last week of 2019 June.
