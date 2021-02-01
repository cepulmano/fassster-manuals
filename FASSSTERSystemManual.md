# FASSSTER R Plumber Server

## Requirements

- R 4.0

## Installing the Required Packages
```
Rscript packages.R
```

## Starting the R Services
```
Rscript runFASSSTERPlumber.R
```

## Staring the Time-series Projections Server
```
Rscript timeseries/0_RunPlumber.R
```

# FASSSTER Python Tornado API Server

## Requirements

- Python 3.5 or higher

## Folder Structure

- datasets: Contains the CSV files relevant to the project
- handlers: Directory to contain Handler files used
- helpers: Helper functions

## Installation Instructions

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

# FASSSTER COVID-19

FASSSTER COVID-19

FASSSTER COVID-19 is a platform designed to compute and visualize output from the COVID-19 compartmental model designed specifically to capture the transmission behavior of the disease and its effect on the population. As an LGU dashboard, FASSSTER provides a variety of tools used for monitoring COVID-19 at the national, regional, provincial and city/municipal level.

## Technologies

- HTML5
- CSS3
- Javascript

## Framework

- Bootstrap 4.5
- Sass

## Libraries

- JQuery 3.5.1
- Template7 (template engine)
- Plotly
- Amcharts
- Leaflet

## Fonts

- Custom SVG
- Fontawesome
- Feather