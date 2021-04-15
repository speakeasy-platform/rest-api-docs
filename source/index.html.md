---
title: SpeakEasy API

language_tabs: # must be one of https://git.io/vQNgJ
  - shell

includes:
  - errors

search: true

code_clipboard: true
---

# Introduction

Welcome to the SpeakEasy API! This documentation is meant to be developer facing,
either for backend developers who would like to get a look at what our product
offers, or as a front end developer to see what endpoints they can leverage while
building their features.

We currently only have language bindings in Shell using cURL, but we'll provide
a javascript api as well when the time comes.

# Authentication

> To authorize, use this code:

```shell
# With shell, you can just pass the correct header with each request
curl "/i/dont/exist/yet" \
  -H "Authorization: sowwy"
```

We will implement authentication soon.

# Users

<!-- ## Get All Kittens

```shell
curl "http://example.com/api/kittens" \
  -H "Authorization: meowmeowmeow"
```

> The above command returns JSON structured like this:

```json
[
  {
    "id": 1,
    "name": "Fluffums",
    "breed": "calico",
    "fluffiness": 6,
    "cuteness": 7
  },
  {
    "id": 2,
    "name": "Max",
    "breed": "unknown",
    "fluffiness": 5,
    "cuteness": 10
  }
]
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
</aside> -->

## Get a Specific User

```shell
curl "http://localhost:8080/api/v1/users"
```

> The above command returns JSON structured like this:

```json
{
  "id": "e5d0a066-e33d-4ce4-85a4-4b84511ece4f",
  "username": "dusto",
  "email": "dusto@speakeasy.com"
}
```

This endpoint retrieves a specific user. Eventually there will be authentication attached to this so that only superusers and the actual owner of the account can obtain information from this endpoint. Right now it's fair game though. *shrug*

### HTTP Request

`GET http://localhost:8080/api/v1/users/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the user to retrieve
