# covidify  [![PyPi Version](https://img.shields.io/pypi/v/covidify.svg)](https://pypi.python.org/pypi/covidify/) ![PyPI - Downloads](https://img.shields.io/pypi/dm/covidify) ![PyPI - License](https://img.shields.io/pypi/l/covidify?color=yellow) [![Python Versions](https://img.shields.io/pypi/pyversions/yt2mp3.svg)](https://pypi.python.org/pypi/covidify/)
<img src="./resources/default.png"/>

<p align="center">
  <a href="#features">Features</a> •
  <a href="#how-to-use">How To Use</a> •
  <a href="#install">Install</a> •
  <a href="#visualizations">Visualizations</a> •
  <a href="https://github.com/CSSEGISandData/COVID-19">Data Source</a> •
  <a href="#credits">Credits</a> •
  <a href="https://github.com/AaronWard/covidify/projects">To-Do List</a> 
</p>
<hr>


## Features
Covidify downloads the latest [covid-19](https://www.who.int/health-topics/coronavirus) data for confirmed cases, deaths and recoveries. 
- Creates a time series dataset
- Creates a daily stats dataset 
- Generate visualizations
- Filter by country
- List all countries affected
- Shows number of people currently infected
- Generates an excel report including all of the above 

![logo](./resources/run.gif "logo")


<hr>


## Install

- ```pip install covidify```

## How to use

```powershell
$ covidify
Usage: covidify [OPTIONS] COMMAND [ARGS]...

  ☣  COVIDIFY ☣

   - use the most up-to-date data to generate reports of 
     confirmed cases, fatalities and recoveries.

Options:
  --help  Show this message and exit.

Commands:
  list  List all the countries that have confirmed cases.
  run   Generate reports for global cases or refine by country.
```

```powershell
$ covidify run --help
Usage: covidify run [OPTIONS]

Options:
  --output TEXT   Folder to output data and reports [Default:
                  /Users/<USER>/Desktop/covidify-output/]
  --source TEXT   There are two datasources to choose from, John Hopkins
                  github repo or wikipedia -- options are git or wiki
                  respectively [Default: git]
  --country TEXT  Filter reports by a country [Default: Global cases]
  --help          Show this message and exit.
```


**Example Commands:**

```powershell
# List all countries affected 
covidify list --countries
```

```powershell
# Will default to desktop folder for output and github for datasource
covidify run 
```


```powershell
# Specify output folder and source
covidify run --output=<PATH TO DESIRED OUTPUT FOLDER>
```

```powershell
# Filter reports by country
covidify run --country="South Korea"
```

<hr>

## Visualizations
An excel spreadsheet is generated with a number of visualizations and statistics.

![logo](./resources/report.gif "logo")


##### Accumalitive Trend

This is an accumulative sum trendline for all the confirmed cases, deaths and recoveries.
![alt text](./reports/images/confirmed_trendline.png)

##### Daily Trendline

This is a daily sum trendline for all the confirmed cases, deaths and recoveries.
![alt text](./reports/images/new_confirmed_cases_trendline.png)

##### Stacked Daily Confirmed Cases

This stacked bar chart shows a daily sum of people who are alread confirmed (<i>red</i>) and the people who have been been confirmed on that date (<i>blue</i>)

![alt text](./reports/images/confirmed_cases_stacked_bar.png "Number of people actually with the virus for each day")


##### Daily Confirmed Cases

A count for new cases on a given date, does not take past confirmations into account. 
![alt text](./reports/images/new_confirmed_cases_bar.png)

##### Daily Deaths

A count for deaths on a given date, does not take past deaths into account. 
![alt text](./reports/images/new_deaths_bar.png)

##### Daily Recoveries

A count for new recoveries on a given date, does not take past recoveries into account. 
![alt text](./reports/images/new_recoveries_bar.png)

##### Currently Infected

A count for all the people who are currently infected for a given date.
![alt text](./reports/images/currently_infected_bar.png)


<hr>

## Credits
- Written by me (Aaron Ward  - https://www.linkedin.com/in/aaronjward/)
- A special thank you to the [JHU CSSE](https://systems.jhu.edu/) team for maintaining the data
- Also a special thank you to @ajaymaity for bug fixes 🎉