---
title: Contact API CRUD Documentation

language_tabs:
  - nodeJS

toc_footers:
  - <a href='https://github.com/GranitB/slate'>Source code for API Documentation</a>
  - <a href='https://github.com/GranitB/API'>Source Code for Contact API</a>

includes:
  - errors

search: true
---

# Introduction

Welcome to the NodeJS CRUD API! You can use our API to access CRUD API endpoints, which you can get information for Contacts in our database.

We have make validation, if you type and invalid data or want to edit delete you will always have confirmation like updated succesully, delete sucessfully
or invalid data we hoppe you will love our simple application if you have any issue please contact us we're here to help you .

It a simple application , you can create contact , get , update and delete contact from the database. All these in Json format . You can view code examples in the dark area to the right with the SHELL commands.

For contacts i have used this data to be stored : Name , LastName , Email , Address , and five Phonenumbers 

This example API documentation page was created by Granit Berisha for links in GIT you can find in the footer link. 



# Contacts

## Get All Contacts

```shell
curl -X GET -H "Content-type: application/json" -H "Accept: application/json"  "http://granitberisha.herokuapp.com/api/contact
```

> The above command returns JSON structured like this:

```json
{
  "success": "Database Readed successfuly.",
  "data": [
    {
      "id": 1,
      "name": "NewName",
      "lastname": "Berisha",
      "address": "NEwAddress",
      "email": "granit@hotelkeyapp.com",
      "phonenumber1": null,
      "phonenumber2": "111111",
      "phonenumber3": null,
      "phonenumber4": null,
      "phonenumber5": null
    },
    {
      "id": 3,
      "name": "Granit",
      "lastname": "Berisha",
      "address": "Kline",
      "email": "granit@hotelkeyapp.com",
      "phonenumber1": "049666456",
      "phonenumber2": "044444444",
      "phonenumber3": null,
      "phonenumber4": null,
      "phonenumber5": null
    }
  ]
}
```

This endpoint retrieves all contacts.

### HTTP Request

`GET http://granitberisha.herokuapp.com/api/contact`


<aside class="success">
Remember — this method will return any contact in database 
</aside>

## Get a Specific Contact



```shell
curl -X GET -H "Content-type: application/json" -H "Accept: application/json"  "http://granitberisha.herokuapp.com/api/contact/3"
```

> The above command returns JSON structured like this:

```json
{
  "success": "Read data with id",
  "data": [
    {
      "id": 3,
      "name": "Granit",
      "lastname": "berisha",
      "address": "Kline-Kosovo",
      "phonenumber": "049666456",
      "email": "niti@niti.com"
    }
  ]
}
```

This endpoint retrieves a specific contact.



### HTTP Request

`GET http://granitberisha.herokuapp.com/api/contact/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the contact to retrieve

<aside class="notice">If you're not using an ID thats is registered in Database, will return error </aside>

## Create a Contact



```shell
curl -i -X POST -H "Content-Type: application/json" -d "{""name"":""granit"",""lastname"":""berisha"",""address"":""kline"",""email"":""granit@herokuapp.com"",""phonenumber1"":""049666456""}" "https://granitberisha.herokuapp.com/api/contact"
```

> The above command returns JSON structured like this:

```json
{
  "success": "Contact inserted successfuly into database."
}
```

This endpoint updates a specific contact.


### HTTP Request

`POST http://granitberisha.herokuapp.com/api/contact/`

### URL Parameters

Parameter | Requirement | Description
--------- | ------- | -----------
name | true | The Name that you like add
last-name | false | The Last Name that you like to add 
address | false | The Address that you like to add
email | false | The new Email that you like to add
phonenumber1 | false | The Phone number that you like add
phonenumber2 | false | The Phone number that you like add
phonenumber3 | false | The Phone number that you like add
phonenumber4 | false | The Phone number that you like add
phonenumber5 | false | The Phone number that you like add


<aside class="notice">If you're not using an ID thats is registered in Database, will return error </aside>


## Update a Specific Contact


```shell
curl -i -X PUT -H "Content-Type: application/json" -d "{""id"":""1"",name"":""granit"",""lastname"":""berisha"",""address"":""kline"",""email"":""granit@herokuapp.com"",""phonenumber1"":""049666456""}" "https://granitberisha.herokuapp.com/api/contact"
```

> The above command returns JSON structured like this:

```json
{
  "success": "Contact updated successfully in the database."
}
```

This endpoint updates a specific contact.



### HTTP Request

`PUT http://granitberisha.herokuapp.com/api/contact/`

### URL Parameters

Parameter | Requirement | Description
--------- | ------- | -----------
ID | true | The ID of the contact to update 
name | false | The new Name that you like to change
last-name | false | The new Last Name that you like to change
address | false | The new Address that you like to change
email | false | The new Email that you like to change
phonenumber1 | false | The new Phone number that you like to change
phonenumber2 | false | The new Phone number that you like to change
phonenumber3 | false | The new Phone number that you like to change
phonenumber4 | false | The new Phone number that you like to change
phonenumber5 | false | The new Phone number that you like to change

<aside class="notice">If you're not using an ID that's is registered in Database, will return error </aside>


## Delete a Specific Contact
```shell
curl -i -X DELETE -H "Content-Type: application/json" -d "{""id"":""1""}" "https://granitberisha.herokuapp.com/api/contact"
```

> The above command returns JSON structured like this:

```json
{
  "success": "Contact successfuly deleted from the database."
}
```

This endpoint delete a specific contact.

<aside class="notice">If you're not using an ID thats is registered in Database, will return error </aside>

### HTTP Request

`DELETE http://granitberisha.herokuapp.com/api/contact/`

### URL Parameters

Parameter | Requirement | Description
--------- | ------- | -----------
ID | true | The ID of the contact to delete

<aside class="warning">If you delete a Contact it will permanently deleted you cant restore </aside>