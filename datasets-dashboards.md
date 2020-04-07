# datasets and dashboards for https://itrack.shinyapp.io/covid

## Related to Canada:

### Data:

Official: 
- Archived Content (last updated 29/03/2020) https://www150.statcan.gc.ca/t1/tbl1/en/tv.action?pid=1310076701
(<--  https://search.open.canada.ca/en/od/?search_text=covid )

  - str1 <- "https://www150.statcan.gc.ca/t1/tbl1/#?pid=13100767&file=1310076701-eng.csv" - does not open in R directly?
  - str2 <- "https://www150.statcan.gc.ca/n1/tbl/csv/13100767-eng.zip" - problem openinig in R directly (need to besaved locally first)

- https://health-infobase.canada.ca/src/data/covidLive/covid19.csv, - opens in R directly
(from https://www.canada.ca/en/public-health/services/diseases/2019-novel-coronavirus-infection.html  (Canada, Public Health)


Crowdsourced by UofT - by city and details / links: see below - - opens in R directly

- https://docs.google.com/spreadsheets/d/1D6okqtBS3S2NRC7GFVHzaZ67DuTw7LX49-fqSLwJyeo/export?format=xlsx 
  - To open it in R: see https://github.com/ivi-m/R-Ottawa/blob/master/r101/r01-opendata.R
  - Used in dashboard below


### Dashboards:

- https://art-bd.shinyapps.io/covid19canada/ - https://github.com/ishaberry/Covid19Canada 
- https://covid19canada.herokuapp.com/
- https://georgeflerovsky-canada.github.io/Canada-COVID-19-dashboard/ - https://github.com/GeorgeFlerovsky-Canada/Canada-COVID-19-dashboard

Geographic data: https://www150.statcan.gc.ca/n1/pub/82-402-x/2011001/reg-eng.htm

## International

Mobility restrictions due to COVID-19: https://migration.iom.int/ (UN-IOM)

-          EU open data on worldwide spread of COVID-19: https://www.europeandataportal.eu/data/datasets/covid-19-coronavirus-data?locale=en

https://www.europeandataportal.eu/data/datasets?locale=en&query=%22covid%22%20OR%20%22corona%22&page=1

Open data:

- https://towardsdatascience.com/5-datasets-about-covid-19-you-can-use-right-now-46307b1406a
- https://www.opengovpartnership.org/collecting-open-government-approaches-to-covid-19/
- https://github.com/datasets/covid-19
- https://github.com/CSSEGISandData/COVID-19
- https://github.com/ibesora/covid-19-data


- https://venturebeat.com/2020/03/30/google-launches-covid-19-public-datasets-program-to-foster-coronavirus-fighting-ai-models/
- https://cloud.google.com/blog/products/data-analytics/free-public-datasets-for-covid19

- https://github.blog/2020-03-23-open-collaboration-on-covid-19/
- https://www.opengovpartnership.org/collecting-open-government-approaches-to-covid-19/

- https://www.ecdc.europa.eu/en/publications-data/download-todays-data-geographic-distribution-covid-19-cases-worldwide

```
library(readxl)
library(httr)

#create the URL where the dataset is stored with automatic updates every day
url <- paste("https://www.ecdc.europa.eu/sites/default/files/documents/COVID-19-geographic-disbtribution-worldwide-",format(Sys.time(), "%Y-%m-%d"), ".xlsx", sep = "")

#download the dataset from the website to a local temporary file
GET(url, authenticate(":", ":", type="ntlm"), write_disk(tf <- tempfile(fileext = ".xlsx")))

#read the Dataset sheet into “R”
data <- read_excel(tf)
```
