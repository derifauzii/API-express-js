# Address API Spec

## Create Address API

Endpoint: POST /api/contacts/:contactsId/addresses

Headers: 
- Authorization : token

Request Body : 

```json
{
    "street": "Jalan sesama",
    "city" : "Malang",
    "province" : "Jawa Timur",
    "country" : "Indonesia" ,
    "postal_code" : 63155,
}
```

Response Body Success:

```json
{
    "data" : {
        "id" : 1,
        "street": "Jalan sesama",
        "city" : "Malang",
        "province" : "Jawa Timur",
        "country" : "Indonesia" ,
        "postal_code" : 63155,
    }

}
```

Response Body Error:

```json
{
    "errors" : "Country is require"
}
```

## Update Address API

Endpoint: PUT /api/contacts/:contactId/addresses/:addressId

Headers: 
- Authorization : token

Request Body :

```json
{
    "street": "Jalan sesama",
    "city" : "Malang",
    "province" : "Jawa Timur",
    "country" : "Indonesia" ,
    "postal_code" : 63155,
}
```

Response Body Success:

```json
{
    "data" : {
        "id" : 1,
        "street": "Jalan sesama",
        "city" : "Malang",
        "province" : "Jawa Timur",
        "country" : "Indonesia" ,
        "postal_code" : 63155,
    }

}
```

Response Body Error:

```json
{
    "errors" : "Country is require"
}
```

## Get Address API

Endpoint: GET /api/contacts/:contactId/addresses/:addressId

Headers: 
- Authorization : token

Response Body Success:

```json
{
    "data" : {
        "id" : 1,
        "street": "Jalan sesama",
        "city" : "Malang",
        "province" : "Jawa Timur",
        "country" : "Indonesia" ,
        "postal_code" : 63155,
    }

}
```

Response Body Error:

```json
{
    "errors" : "Contact is not found"
}
```

## List Address API

Endpoint: GET /api/contacts/:contactId/addresses

Headers: 
- Authorization : token

Response Body Success:

```json
{
    "data" : [
        {
        "id" : 1,
        "street": "Jalan sesama",
        "city" : "Malang",
        "province" : "Jawa Timur",
        "country" : "Indonesia" ,
        "postal_code" : 63155,
        },
        {
        "id" : 2,
        "street": "Jalan sesama",
        "city" : "Malang",
        "province" : "Jawa Timur",
        "country" : "Indonesia" ,
        "postal_code" : 63155,
        }
    ]
}
```

Response Body Error:

```json
{
    "errors" : "Contact is not found"
}
```

## Remove Address API

Endpoint: DELETE /api/contacts/:contactId/addresses/:addressId
Headers: 
- Authorization : token

Response Body Success:

```json
{
    "data" : "OK"
}
```

Response Body Error:

```json
{
    "errors" : "Contact is not found"
}
```