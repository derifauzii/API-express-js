# Contact API Spec

## Create Contact API

Endpoint : POST /api/contacts

Headers :
-Authorization : token

Request Body :

```json

{
 "first_name" : "Dandy",
 "last_name" : "fauzan",
 "email" : "dandy@gmail.com",
 "phone" : "0193490371"

}
```


Response Body Success :

```json
{
    "data" : {
        "id" : 1,
        "first_name" : "Dandy",
        "last_name" : "fauzan",
        "email" : "dandy@gmail.com",
        "phone" : "0193490371"
    }
}
```
Response Body Error :

```json
{
    "errors" : "Email is not valid format" 
}
```


## Update Contact API

Endpoint : FETCH /api/contacts/:id

Headers :
-Authorization : token

Request Body :

```json
{
    "id" : 1,
    "first_name" : "Dandy",
    "last_name" : "fauzan",
    "email" : "dandy@gmail.com",
    "phone" : "0193490371"
}
```
Response Body Success :

```json
{
    "data" : {
        "id" : 1,
        "first_name" : "Dandy",
        "last_name" : "fauzan",
        "email" : "dandy@gmail.com",
        "phone" : "0193490371"
    }
}
```

Response Body Error :

```json
{
    "errors" : "Email is not valid format" 
}
```

## Get Contact API

Endpoint : GET /api/contacts/:id

Headers :
-Authorization : token

Response Body Success :



Response Body Error :

## Search Contact API

Endpoint : POST /api/contacts

Headers :
-Authorization : token

Request Body :

Response Body Success :

Response Body Error :

## Remove Contact API

Endpoint : POST /api/contacts

Headers :
-Authorization : token

Request Body :

Response Body Success :

Response Body Error :