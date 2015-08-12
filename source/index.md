---
title: Contact API CRUD Documentation

language_tabs:
  - nodeJS

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>
  - <a href='http://github.com/tripit/slate'>Documentation Powered by Slate</a>

includes:
  - errors

search: true
---

# Introduction

Welcome to the NodeJS CRUD API! You can use our API to access CRUD API endpoints, which can get information on various cats, kittens, and breeds in our database.

We have language bindings in Shell, Ruby, and Python! You can view code examples in the dark area to the right, and you can switch the programming language of the examples with the tabs in the top right.

This example API documentation page was created with [Slate](http://github.com/tripit/slate). Feel free to edit it and use it as a base for your own API's documentation.


# Contacts

## Get All Contacts

```shell
curl -X GET -H "Content-type: application/json" -H "Accept: application/json"  "http://granitberisha.herokuapp.com/api/contact
```

> The above command returns JSON structured like this:

```json
{
  "success": "Read data with success",
  "data": [
    {
      "id": 3,
      "name": "Granit",
      "lastname": "berisha",
      "address": "Kline-Kosovo",
      "phonenumber": "049666456",
      "email": "niti@niti.com"
    },
    {
      "id": 1,
      "name": "Granitiiii",
      "lastname": "berisha",
      "address": "Kline-Kosovo",
      "phonenumber": "049666456",
      "email": "niti@niti.com"
    }
  ]
}
```

This endpoint retrieves all contacts.

### HTTP Request

`GET http://granitberisha.herokuapp.com/api/contact`


<aside class="success">
Remember — you can use other application for GET like Postman
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

This endpoint retrieves a specific kitten.

<aside class="notice">If you're not using an ID thats is registered in Database, will return Success but with no data on it </aside>

### HTTP Request

`GET http://granitberisha.herokuapp.com/api/contact/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the contact to retrieve



## Update a Specific Contact



```shell
curl -X UPDATE -H "Content-type: application/json" -H "Accept: application/json"  "http://granitberisha.herokuapp.com/api/contact/3"
  
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

This endpoint retrieves a specific kitten.

<aside class="notice">If you're not using an ID thats is registered in Database, will return Success but with no data on it </aside>

### HTTP Request

`UPDATE http://granitberisha.herokuapp.com/api/contact/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the contact to retrieve

