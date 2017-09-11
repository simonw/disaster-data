# irma-scraped-data

Data scraped by https://github.com/simonw/irma-scrapers

The most interesting output of this repo is its commit history, which
shows when the various scraping sources have been updated and what
changed: https://github.com/simonw/irma-scraped-data/commits/master

Some of these changes are published to the Irma response Slack, in
the #shelter_scraper_data channel. https://irma-response-slack.herokuapp.com/

## florida-shelters.json (published to Slack)

Data scraped from the table on http://www.floridadisaster.org/shelters/summary.aspx

## fema-open-shelters.json (published to Slack)

Data from https://gis.fema.gov/REST/services/NSS/OpenShelters/MapServer/0/query?f=json&returnGeometry=true&spatialRel=esriSpatialRelIntersects&geometry=%7B%22xmin%22%3A-10018754.171396945%2C%22ymin%22%3A2504688.5428529754%2C%22xmax%22%3A-7514065.628548954%2C%22ymax%22%3A5009377.085700965%2C%22spatialReference%22%3A%7B%22wkid%22%3A102100%7D%7D&geometryType=esriGeometryEnvelope&inSR=102100&outFields=*&outSR=102100

Documentation here: https://gis.fema.gov/REST/services/NSS/OpenShelters/MapServer

## fema-nss.json (published to Slack)

Data from https://gis.fema.gov/REST/services/NSS/FEMA_NSS/MapServer/0/query?f=json&returnGeometry=true&spatialRel=esriSpatialRelIntersects&geometry=%7B%22xmin%22%3A-10018754.171396945%2C%22ymin%22%3A2504688.5428529754%2C%22xmax%22%3A-7514065.628548954%2C%22ymax%22%3A5009377.085700965%2C%22spatialReference%22%3A%7B%22wkid%22%3A102100%7D%7D&geometryType=esriGeometryEnvelope&inSR=102100&outFields=*&outSR=102100

## pascocountyfl.json (published to Slack)

Data from http://www.pascocountyfl.net/index.aspx?NID=2816

## hernando-county.json (published to Slack)

Data from http://www.hernandocounty.us/em/shelter-information

## scemd-shelters.json (published to Slock)

South Carolina shelters data from http://scemd.org/shelters-rss

## georgia-gema-active-shelters.json (published to Slack)

Active shelter data from https://gema-soc.maps.arcgis.com/apps/webappviewer/index.html?id=279ef7cfc1da45edb640723c12b02b18

## georgia-gema-animal-shelters.json (published to Slack)

Animal shelter data from https://gema-soc.maps.arcgis.com/apps/webappviewer/index.html?id=279ef7cfc1da45edb640723c12b02b18

## ledger-polk-county.json (published to Slack)

Data from http://www.ledgerdata.com/hurricane-guide/shelter/

## zeemaps-2682928.json (not published to Slack)

Data pulled from https://zeemaps.com/map?group=2682928

## irma-shelters.json (not published to Slack)

Data from https://irma-api.herokuapp.com/api/v1/shelters

## irma-shelters-dupes.json (published to Slack)

This file is derived from https://irma-api.herokuapp.com/api/v1/shelters - it shows currently detected potential duplicate shelters, based on a comparison of their latitude/longitude. Shelters within 19m of each other are considered potential duplicates.

This allows us to follow the commit history of that file at https://github.com/simonw/irma-scraped-data/commits/master/irma-shelters-dupes.json (also published to Slack) to see when someone adds a potential duplicate, or fixes one. The file also shows shelters that do not have a valid latitude/longitude and/or address.

## fpl-county-outages.json (not published to Slack)

Power outage data from https://www.fplmaps.com/ - https://www.fplmaps.com/customer/outage/CountyOutages.json

Shaped like this:

    "charlotte": {
      "numberofaffected": 20400, 
      "numberofaccounts": 114100, 
      "numberofrestored": 4670, 
      "name": "Charlotte", 
      "numberofoutages": 15730
    }
 
 ## fpl-storm-outages.json

Power outage data from https://www.fplmaps.com/ - https://www.fplmaps.com/data/storm-outages.js

Shaped like this:

    {
      "Customers Out": "8", 
      "County Name": "Baker", 
      "Customers Served": "5,380"
    }
