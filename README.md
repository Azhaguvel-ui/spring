## Environment
- Java version: 17
- Maven version: 3.*
- Spring Boot version: 3.0.6E

## Data
Example of a Vehicle data JSON object:
```json
{
    "id":1,
    
    "brand":"suzuki",
    
    "type":"hatchback",
    
    "cc":1200,

    "color": "red"
}
```

## Requirements
In this project, The vehicle data are provided for many countries with API endpoints for fetching specific information. Note that all the data are virtual.

Following REST Endpoints have been implemented.

`POST` request to `/api/vehicle`:
* accepts a vehicle object without id and returns status code 201 of creation
* if the vehicle object with id is provided, returns status code 400

`GET` request to `/api/vehicle/{id}`:
* returns the vehicle entry with given id and status code 200
* returns status code 404 if requested vehicle doesn't exist
* returns status code 400 if requested vehicle id is invalid

* `GET` request to `/api/vehicle`:
* returns all the vehicle entries with status code 200
 
There are 6 tests already written and of which a few are failing due to the bug in the implementation of those endpoints. Your task is to find the bug and fix so that all the tests pass.

## Commands
- run: 
```bash
mvn clean spring-boot:run
```
- install: 
```bash
mvn clean install
```
- test: 
```bash
mvn clean test
```