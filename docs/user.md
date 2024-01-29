# User API Spec

## Register User API

Endpoint : POST /api/users

Request Body :

```json
{
  "username": "admin",
  "password": "admin123",
  "name": "Deri Fauzi"
}
```

Response Body Succes:

```json
{
  "data": {
    "username": "admin",
    "name": "Deri Fauzi"
  }
}
```

Response Body Error:

```json
{
  "errors": "Username Already Registered"
}
```

## Login User API

Endpoint : POST /api/users/login

Request Body :

```json
{
  "username": "admin",
  "password": "admin123"
}
```

Response Body Succes :

```json
{
  "data": {
    "token": "unique-token"
  }
}
```

Response Body Error:

```json
{
  "errors": "Username or Password Wrong"
}
```

## Update User API

Endpoint : PATCH /api/users/current

Headers :

- Authorization : token

Request Body :

```json
{
  "name": "new name",
  "password": "new password"
}
```

Response Body Succes:

```json
{
  "data": {
    "username": "admin",
    "name": "Deri Fauzi"
  }
}
```

Response Body Error:

```json
{
  "errors": "Username Already Registered"
}
```

## Get User API

Endpoint : GET /api/users/current

Headers :

- Authorization : token

Response Body Success :

```json
{
  "data": {
    "username": "admin",
    "name": "Deri Fauzi"
  }
}
```

Response Body Error :

```json
{
  "errors": "Unauthorized"
}
```

## Logout User API

Endpoint : DELETE /api/users/logout

Response Body Success :

```json
{
  "data": "OK"
}
```

Response Body Error :

```json
{
  "errors": "Unauthorized"
}
```
