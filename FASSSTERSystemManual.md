# FASSSTER Systems Manual

This document outlines the technical requirements to set up the FASSSTER v4 Platform. 

## FASSSTER Architecture

<p>The FASSSTER architecture diagram displays the data sources up to the web-based visualization. Users of the system access FASSSTER through the Web Visualization Application. Generally, the architecture comprises three main groups, ie. front-end visualization, data processing, and data store.</p>
<p>The front-end web visualization application serves as the main access point for the users of the platform. It is where users select parameters and initiate requests for visualization. After requests are made, data are gathered from the data processing services via REST APIs. All data used for processing are pulled from the different data stores.
</p>

![FASSSTER Architecture](https://i.imgur.com/HIHgtBg.png)

## Infrastructure Requirements

#### FASSSTER Web Visualization, User Management Service
- OS: Ubuntu 20.04
- 8GB RAM
- 4 cores
- 32GB storage

#### Data Aggregation Service, Data Pre-processing Service (Synchronous)
- OS: Ubuntu 20.04
- 16GB RAM
- 8 cores
- 50GB storage

#### Data Pre-processing Service (Asynchronous)
- OS: Ubuntu 20.04
- 16GB RAM
- 32 cores
- 100GB storage

#### RDBMS, FHIR Data Store, MongoDB, CSV Files
- OS: Ubuntu 20.04
- 8GB RAM
- 4 cores
- 100GB storage

## Software

#### FASSSTER R Plumber Server

##### Requirements

- R 4.0

##### Installing the Required Packages
```
Rscript packages.R
```

##### Starting the R Services
```
Rscript runFASSSTERPlumber.R
```

##### Staring the Time-series Projections Server
```
Rscript timeseries/0_RunPlumber.R
```

#### FASSSTER Python Tornado API Server

##### Requirements

- Python 3.5 or higher

##### Folder Structure

- datasets: Contains the CSV files relevant to the project
- handlers: Directory to contain Handler files used
- helpers: Helper functions

##### Installation Instructions

1. Install Python 3.5
2. Install the required packages
```
pip install -r requirements.txt
```
3. Create a `settings.py` file
```
database = {
    'HOST': 'localhost',
    'PORT': 3306,
    'USER': 'user',
    'PASSWORD': 'password',
    'DATABASE_NAME': 'emrhandler'
}
```
4. Start the server
```
python server.py
```

#### FASSSTER COVID-19 Web Visualization

FASSSTER COVID-19 is a platform designed to compute and visualize output from the COVID-19 compartmental model designed specifically to capture the transmission behavior of the disease and its effect on the population. As an LGU dashboard, FASSSTER provides a variety of tools used for monitoring COVID-19 at the national, regional, provincial and city/municipal level.

##### Technologies

- HTML5
- CSS3
- Javascript

##### Framework

- Bootstrap 4.5
- Sass

##### Libraries

- JQuery 3.5.1
- Template7 (template engine)
- Plotly
- Amcharts
- Leaflet

##### Fonts

- Custom SVG
- Fontawesome
- Feather

#### Datastores

- RDBMS: MySQL v5.6
- FHIR v4.0.1
- MongoDB v4.4
