# Contact API Spec

## Create Contact API

Endpoint : POST /api/contacts

Headers :
-Authorization : token

Request Body :

```json
{
  "first_name": "Dandy",
  "last_name": "fauzan",
  "email": "dandy@gmail.com",
  "phone": "0193490371"
}
```

Response Body Success :

```json
{
  "data": {
    "id": 1,
    "first_name": "Dandy",
    "last_name": "fauzan",
    "email": "dandy@gmail.com",
    "phone": "0193490371"
  }
}
```

Response Body Error :

```json
{
  "errors": "Email is not valid format"
}
```

## Update Contact API

Endpoint : PUT /api/contacts/:id

Headers :
-Authorization : token

Request Body :

```json
{
  "id": 1,
  "first_name": "Dandy",
  "last_name": "fauzan",
  "email": "dandy@gmail.com",
  "phone": "0193490371"
}
```

Response Body Success :

```json
{
  "data": {
    "id": 1,
    "first_name": "Dandy",
    "last_name": "fauzan",
    "email": "dandy@gmail.com",
    "phone": "0193490371"
  }
}
```

Response Body Error :

```json
{
  "errors": "Email is not valid format"
}
```

## Get Contact API

Endpoint : GET /api/contacts/:id

Headers :
-Authorization : token

Response Body Success :

```json
{
  "data": {
    "id": 1,
    "first_name": "Dandy",
    "last_name": "fauzan",
    "email": "dandy@gmail.com",
    "phone": "0193490371"
  }
}
```

Response Body Error :

```json
{
  "errors": "Contact is not found"
}
```

## Search Contact API

Endpoint : GET /api/contacts

Headers :
-Authorization : token

Query Params:

- name : search by first_name or last_name using like query
- email : search by email using like query
- phone : search by phone using like query
- page : number of page, default by 1
- size : size per page, default by 10

Response Body Success :

```json
{
  "data": [
    {
      "id": 1,
      "first_name": "Dandy",
      "last_name": "fauzan",
      "email": "dandy@gmail.com",
      "phone": "0193490371"
    },
    {
      "id": 2,
      "first_name": "Dandy",
      "last_name": "fauzan",
      "email": "dandy@gmail.com",
      "phone": "0193490371"
    }
  ],
  "paging": {
    "page": 1,
    "total_page": 3,
    "total_item": 30
  }
}
```

Response Body Error :

```json
{
  "errors": "data not found"
}
```

## Remove Contact API

Endpoint : DELETE /api/contacts/:id

Headers :
-Authorization : token

Response Body Success :

```json
{
  "data": "OK"
}
```

Response Body Error :

```json
{
  "errors": "Contact is not found"
}
```
