# pdo-crud-for-free-repositories-sample-project

[![Open in Gitpod](https://gitpod.io/button/open-in-gitpod.svg)](https://gitpod.io/#https://github.com/dr-matt-smith/gitpod-db-test-01)

This sample project illustrates how to use the PHP package `pdo-crud-for-free-repositories`

All code is (intended :-) to follow PSR-1, PSR-12 coding standards. Classes are following the PSR-4 autoloading standard.

## Install

Via Git:

``` bash
$ git clone git@github.com:dr-matt-smith/pdo-crud-for-free-repositories-sample-project.git
```

Then run Composer to populate the `/vendor` directory with dependencies:
``` bash
$ composer install
```

## MySQL database settings`/.env`

File `.env` defines the 5 required constants for DB access.

Update them as required for your own MySQL setup:
```
    MYSQL_USER=root
    MYSQL_PASSWORD=passpass
    MYSQL_HOST=127.0.0.1
    MYSQL_PORT=3306
    MYSQL_DATABASE=evote
```

Create the database schema, e.g. `evote` in this example

## Run the migration and initial data fixtures script

In folder `db` is a file `migrateAndLoadFixtures.php`. Run this script to create the DB table `movie`, and insert 2 initial records:

```bash
php movieMigrationAndFixtures.php
```

## Run the web server

Run your web server, making `/public` the web root:

```bash
php -S localhost:8000 -t public
```

## Open a browser 
Open a browser to `http://localhost:8000`

or whatever port your webserver is running at

![screenshot of browser](screenshot.png)
