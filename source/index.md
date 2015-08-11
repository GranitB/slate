---
title: API CRUD Documentation

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
curl -X GET -H "Content-type: application/json" -H "Accept: application/json"  "http://granitberisha.herokuapp.com/api/db
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

This endpoint retrieves all kittens.

### HTTP Request

`GET http://example.com/api/kittens`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
include_cats | false | If set to true, the result will also include cats.
available | true | If set to false, the result will include kittens that have already been adopted.

<aside class="success">
Remember — a happy kitten is an authenticated kitten!
</aside>

## Get a Specific Contact

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
api.kittens.get(2)
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
api.kittens.get(2)
```

```shell
curl "http://example.com/api/kittens/2"
  -H "Authorization: meowmeowmeow"
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "name": "Isis",
  "breed": "unknown",
  "fluffiness": 5,
  "cuteness": 10
}
```

This endpoint retrieves a specific kitten.

<aside class="warning">If you're not using an administrator API key, note that some kittens will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`GET http://example.com/kittens/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the kitten to retrieve

