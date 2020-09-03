# internal-project
Internal project for Cognizant. (Car parking backend part)

**Problem**:   Some reservation process takes **a lot of paperwork** - that takes **a lot of time**.
**Target**:   **Automate parking** and room reservation, optimize badge management system.

## Functionality :

* Registration
* Car removing
* Cars switching
* Check registration

## Definition of Done :

* Design reviewed
* Code Produced
* Builds without errors
* Unit and functional tests passed
* Continuous Integration build passing
* Kanban Board – To-do list finished

## User stroies:

![GitHub Logo](/images/logo.png)
Format: ![Alt Text](url)

![GitHub Logo](/images/logo.png)
Format: ![Alt Text](url)

# Car parking service

## Flow directions

![GitHub Logo](/images/logo.png)
Format: ![Alt Text](url)

## Controller

Controller for car parking is located in file *src/main/java/com/example/RestService/api/CerConroller.java*
Request Mapping is: *api/car_park*
 
Below are described all controller mappings:
 
* Update car registration status in database | Approve car registration

**PUT** : {{base_url}}/{{car_park}}/car/approve

**BODY** :

```
{
    "userId": USER_ID,
    "carNum": "CAR_NUMBER",
    "approvedStatus": true
}
```
**RETURNS** :  HTTP STATUS OK
 
 
* Set active car

**PUT** : {{base_url}}/{{car_park}}/car/set_active

**BODY** :

```
{
    "userId": USER_ID,
    "carNum": "CAR_NUMBER",
}
```
**RETURNS** :  HTTP STATUS OK
 
 
* Get list with all information about all cars in database

**GET** : {{base_url}}/{{car_park}}/car/all

**RETURNS** :  HTTP STATUS OK
 
 
* Get list with information about all persons cars by his ID from database

**GET** : {{base_url}}/{{car_park}}/car/:userId/all

**RETURNS** :  HTTP STATUS OK
 
 
* Get all information about one car by car number from database

**GET** : {{base_url}}/{{car_park}}/car/person/:carNum

**RETURNS** :  HTTP STATUS OK
 
 
* Get list with all information about all persons from database

**GET** : {{base_url}}/{{car_park}}/person/all

**RETURNS** :  HTTP STATUS OK
 
 
* Get all information about person by ID from database

**GET** : {{base_url}}/{{car_park}}/person/:personid

**RETURNS** :  HTTP STATUS OK
 
 
* Delete person from database (by admin)

**DEL** : {{base_url}}/{{car_park}}/person/:personId

**RETURNS** :  HTTP STATUS OK
 
 
* Delete car from database by car number (by admin)

**DEL** : {{base_url}}/{{car_park}}/car/:carnum

**RETURNS** :  HTTP STATUS OK
 
 
* Add person and car to database

**POST** : {{base_url}}/{{car_park}}

**BODY** : 

```
{
    "userId": USER_ID,
    "name": "USER_NAME",
    "surname": "USER_SURNAME",
    "phone": "USER_PHONE",
    "carNum": "CAR_NUMBER"
}
```
**RETURNS** :  HTTP STATUS OK
 
**VARIABLES**:

```
{{base_url}} - localhost:8080
{{car_park}} - api/car_park
```

## BPMN: CAR ADDING PROCESS

![GitHub Logo](/images/logo.png)
Format: ![Alt Text](url)


# Database











