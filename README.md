# ParkingLotTrackerServer
Server application for the ParkingLotTracker project.

## Table of Contents

- [Installation](#installation)
- [How to run](#how-to-run)
- [API Documentation](#api-documentation)

## Installation

```sh
$ npm install
```

Change the database settings in Config directory.
 - default is the production database.
 - dev is the development database.
 - test is for the test database.

To enable additional settings modify src/dbconnection.js
To find out which options that are available look at:
- https://github.com/mysqljs/mysql#connection-options
- https://github.com/mysqljs/mysql#pool-options

## How to run

```sh
$ npm start
```
To change which database is used change the package.json start script.

## Tests

To run tests
```sh
$ npm test
```
This script uses the test database.

## API Documentation
API Endpoint | Description
------------ | -------------
parkingLots |
/api/v0/parkinglots | GET - All parkinglots
/api/v0/parkinglots/:id | GET - Single parkinglot
/api/v0/parkinglots | POST - Creates new parkinglot
/api/v0/parkinglots | PUT - Updates a parkinglot
parkingLogs |
/api/v0/parkinglogs | GET - All parkinglogs
/api/v0/parkinglogs/:id | GET/DELETE - Single parkinglog
/api/v0/parkinglogs | POST - Creates new parkinglog
/api/v0/parkinglogs | PUT - Updates a parkinglog, only the currentParked value can be changed.
/api/v0/parkinglogs/latest | GET - Single parkinglog of latest date.
