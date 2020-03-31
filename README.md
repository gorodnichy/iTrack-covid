# iTrack-covid


## Codes and resources for https://itrack.shinyapp.io/covid

Related to Canada:

https://www150.statcan.gc.ca/t1/tbl1/en/tv.action?pid=1310076701
( https://search.open.canada.ca/en/od/?search_text=covid )


https://towardsdatascience.com/5-datasets-about-covid-19-you-can-use-right-now-46307b1406a

Open data:

https://www.opengovpartnership.org/collecting-open-government-approaches-to-covid-19/

https://github.com/datasets/covid-19
https://github.com/CSSEGISandData/COVID-19
https://github.com/ibesora/covid-19-data

https://www.ecdc.europa.eu/en/publications-data/download-todays-data-geographic-distribution-covid-19-cases-worldwide

Script for downloading the Excel file into “R” software
Please note that this script updates every day automatically using the time of your computer. Hence, it might show an error message if you try to download the file before we have updated it.

Make sure that you have the “readxl” and “httr” packages installed.

#these libraries are necessary

library(readxl)

library(httr)

#create the URL where the dataset is stored with automatic updates every day

url <- paste("https://www.ecdc.europa.eu/sites/default/files/documents/COVID-19-geographic-disbtribution-worldwide-",format(Sys.time(), "%Y-%m-%d"), ".xlsx", sep = "")

#download the dataset from the website to a local temporary file

GET(url, authenticate(":", ":", type="ntlm"), write_disk(tf <- tempfile(fileext = ".xlsx")))

#read the Dataset sheet into “R”

data <- read_excel(tf)


https://venturebeat.com/2020/03/30/google-launches-covid-19-public-datasets-program-to-foster-coronavirus-fighting-ai-models/
https://cloud.google.com/blog/products/data-analytics/free-public-datasets-for-covid19


https://github.blog/2020-03-23-open-collaboration-on-covid-19/
https://www.opengovpartnership.org/collecting-open-government-approaches-to-covid-19/
