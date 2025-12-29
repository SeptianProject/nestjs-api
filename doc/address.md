# Address API Spec

## Create Address

Endpoint : POST /api/contacts/:contactId/addresses

Headers:

- Authorization: token

Request Body :

```json
{
  "street": "Jl. Merdeka No.1", // optional
  "city": "Jakarta", // optional
  "province": "DKI Jakarta", // optional
  "country": "Indonesia",
  "postal_code": "10110"
}
```

Response Body:

```json
{
  "data": {
    "id": 1,
    "street": "Jl. Merdeka No.1",
    "city": "Jakarta",
    "province": "DKI Jakarta",
    "country": "Indonesia",
    "postal_code": "10110"
  }
}
```

## Get Address

Endpoint : GET /api/contacts/:contactId/addresses/:addressId

Headers:

- Authorization: token

Response Body:

```json
{
  "data": {
    "id": 1,
    "street": "Jl. Merdeka No.1",
    "city": "Jakarta",
    "province": "DKI Jakarta",
    "country": "Indonesia",
    "postal_code": "10110"
  }
}
```

## Update Address

Endpoint : PUT /api/contacts/:contactId/addresses/:addressId

Headers:

- Authorization: token

Request Body :

```json
{
  "street": "Jl. Merdeka No.1", // optional
  "city": "Jakarta", // optional
  "province": "DKI Jakarta", // optional
  "country": "Indonesia",
  "postal_code": "10110"
}
```

Response Body:

```json
{
  "data": {
    "id": 1,
    "street": "Jl. Merdeka No.1",
    "city": "Jakarta",
    "province": "DKI Jakarta",
    "country": "Indonesia",
    "postal_code": "10110"
  }
}
```

## Remove Address

Endpoint : DELETE /api/contacts/:contactId/addresses/:addressId

Headers:

- Authorization: token

Response Body:

```json
{
  "data": true
}
```

## Search Address

Endpoint : GET /api/contacts/:contactId/addresses

Headers:

- Authorization: token

Response Body:

```json
{
  "data": [
    {
      "id": 1,
      "street": "Jl. Merdeka No.1",
      "city": "Jakarta",
      "province": "DKI Jakarta",
      "country": "Indonesia",
      "postal_code": "10110"
    },
    {
      "id": 2,
      "street": "Jl. Merdeka No.1",
      "city": "Jakarta",
      "province": "DKI Jakarta",
      "country": "Indonesia",
      "postal_code": "10110"
    }
  ]
}
```
