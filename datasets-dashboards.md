# Datasets and dashboards available for analyzing the propagation of COVID 19 in Canada and Worldwide

## Names, Population and geo-locations of health regions

### Canada
https://www.stat.gouv.qc.ca/statistiques/profils/region_00/region_00_an.htm

Health region boundary files:  **  
https://www150.statcan.gc.ca/n1/pub/82-402-x/2011001/reg-eng.htm

### World
https://worldpopulationreview.com/canadian-provinces/
https://simplemaps.com/data/ca-cities

## Covid Data: Canada


### Official: 

The official source of information on the 2020 COVID-19 outbreak in Canada is: canada.ca/coronavirus.

www150.statcan.gc.ca:

Table: 13-10-0766-01

https://www150.statcan.gc.ca/t1/tbl1/en/tv.action?pid=1310076601
https://www150.statcan.gc.ca/n1/tbl/csv/13100766-eng.zip

replaces Table: 13-10-0767-01

- Archived Content (last updated 29/03/2020) https://www150.statcan.gc.ca/t1/tbl1/en/tv.action?pid=1310076701
(<--  https://search.open.canada.ca/en/od/?search_text=covid )

  - str1 <- "https://www150.statcan.gc.ca/t1/tbl1/#?pid=13100767&file=1310076701-eng.csv" - does not open in R directly?
  - str2 <- "https://www150.statcan.gc.ca/n1/tbl/csv/13100767-eng.zip" - problem openinig in R directly (need to besaved locally first)

https://www.canada.ca/en/public-health:

https://health-infobase.canada.ca/src/data/covidLive/covid19.csv, - opens in R directly (Subset from above?)
(from https://www.canada.ca/en/public-health/services/diseases/2019-novel-coronavirus-infection.html  


#### Crowdsourced by UofT - by city and details / links: see below - - opens in R directly

https://github.com/ishaberry/Covid19Canada ->
- https://docs.google.com/spreadsheets/d/1D6okqtBS3S2NRC7GFVHzaZ67DuTw7LX49-fqSLwJyeo/export?format=xlsx 
  - To open it in R: see https://github.com/ivi-m/R-Ottawa/blob/master/r101/r01-opendata.R
  - Used in dashboard below


### Dashboards:

- https://art-bd.shinyapps.io/covid19canada/ - https://github.com/ishaberry/Covid19Canada 
- https://covid19canada.herokuapp.com/
- https://georgeflerovsky-canada.github.io/Canada-COVID-19-dashboard/ - https://github.com/GeorgeFlerovsky-Canada/Canada-COVID-19-dashboard


Data source: Public Health Agency of Canada, Surveillance and Risk Assessment, Epidemiology update; Natural Resources Canada - Grey basemap

Credit: COVID-19 Situational Awareness tiger team Powered by ESRI-Canada and COVID-19 Canadian Geostatistical Platform, a collaboration between Public Health Agency of Canada, Statistics Canada and Natural Resources Canada.

- https://experience.arcgis.com/experience/2f1a13ca0b29422f9b34660f0b705043/

Geographic data: https://www150.statcan.gc.ca/n1/pub/82-402-x/2011001/reg-eng.htm
Population and geo-location of canadian cities: https://simplemaps.com/data/ca-cities
https://simplemaps.com/static/data/country-cities/ca/ca.csv

## Covid data: International

Mobility restrictions due to COVID-19: https://migration.iom.int/ (UN-IOM)

- EU open data on worldwide spread of COVID-19: https://www.europeandataportal.eu/data/datasets/covid-19-coronavirus-data

Open data:

- https://towardsdatascience.com/5-datasets-about-covid-19-you-can-use-right-now-46307b1406a
- https://towardsdatascience.com/top-5-r-resources-on-covid-19-coronavirus-1d4c8df6d85f
- https://www.opengovpartnership.org/collecting-open-government-approaches-to-covid-19/
- https://github.com/datasets/covid-19
- https://github.com/CSSEGISandData/COVID-19 - Main
- https://github.com/ibesora/covid-19-data


- https://venturebeat.com/2020/03/30/google-launches-covid-19-public-datasets-program-to-foster-coronavirus-fighting-ai-models/
- https://cloud.google.com/blog/products/data-analytics/free-public-datasets-for-covid19

- https://github.blog/2020-03-23-open-collaboration-on-covid-19/
- https://www.opengovpartnership.org/collecting-open-government-approaches-to-covid-19/

- https://www.ecdc.europa.eu/en/publications-data/download-todays-data-geographic-distribution-covid-19-cases-worldwide


## R Dashboards  

- https://github.com/AntoineSoetewey/coronavirus_dashboard)
- https://ramikrispin.github.io/coronavirus_dashboard/ 
- Ukraine: https://rstudio-pubs-static.s3.amazonaws.com/592327_4363a37b09fc4beeb877a1351c600ef9.html


- https://ourworldindata.org/coronavirus



## R Forecasting 

- https://alhill.shinyapps.io/COVID19seir/

Other COVID-19 apps that we recommend:

-    https://benflips.shinyapps.io/nCovForecast/ - For tracking the growth rate of infections over time, comparing contries, and estimating the fraction of cases detected
-    https://mackgrenfell.com/forecaster/covid19 - Simulations simple exponential growth and compares to hospital capacity
-    http://gabgoh.github.io/COVID/index.html - Visualize the impact of intervention timing and strength on the reduction of cases
-   https://neherlab.org/covid19/ - Similar to this app, simulating epidemic dynamics and comparing to hospital capacity



## Educational:

https://www.youtube.com/watch?v=gxAaO2rsdIs from  https://www.3blue1brown.com
Simulating an epidemic
3,368,784 views
•27 Mar 2020


test from other account
