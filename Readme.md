# Drupal Docker

A docker-compose file to start a local [Drupal](https://www.drupal.org/) service.

This docker-compose consists of two components:
1. Official [Drupal image](https://hub.docker.com/_/drupal) (drupal:9)
2. Official [PostgreSQL image](https://hub.docker.com/_/postgres) (postgres:11)

## Start the service

To start Drupal service, simply checkout this repository and run
```
docker-compose up -d
```

Drupal will be installed and accessible at port 8000.

If run locally, Drupal can be accessed by going to ```http://localhost:8000``` using the web browser.

## Stop the service

To stop the service, simply run
```
docker-compose down
```

## Persistent storage and backup

This compose creates two persistent volumes to store the data:
1. drupal_sitedata - stores all files of the site including all uploaded items,
2. drupal_dbdata - stores the data of PostgreSQL database. 

These volumes can be backed up and managed via the ```docker volume``` utility.
