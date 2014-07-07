# TrailScribe Map Tiling Service
This repo contains scripts to process and tile Geotiff images for OpenLayers TMS overview.

## Requirements
* Ubuntu 12.04.4
* Python 2.7
* MySQL-python
* GDAL
* python-gdal

## Installation Guide
* Installing MySQL-python
 - `apt-get install python-pip`
 - `pip install -U pip`
 - `apt-get install python-dev libmysqlclient-dev`
 - `pip install MySQL-python`
 - `pip install --allow-external mysql-connector-python mysql-connector-python`

* Installing GDAL and python-gdal
 - `apt-get install gdal-bin`
 - `apt-get install python-gdal`

* The files **setup_map** and **setup_map.py** must be executable
 - `chmod 755 setup_map setup_map.py`

## Usage
* Start by uploading a Geotiff map image to the current location on the server
 - `scp map.tif <user>@<host>:~/trailscribe/scripts/.`

* Run Python script. Usage: `python setup_map.py <source map> <target map name>`
 - `python setup_map.py map.tif map1`

* Newly created tiles can be found at: `~/trailscribe/media/map/map1_tiles.tgz`
