# Contact API Spec

## Create Contact

Endpoint : POST /api/contacts

Headers:

- Authotization: token

Request Body:

```json
{
  "first_name": "Septianz",
  "last_name": "Code",
  "email": "septianz@gmail.com",
  "phone": "086666666666"
}
```

Response Body :

```json
{
  "data": {
    "id": 1,
    "first_name": "Septianz",
    "last_name": "Code",
    "email": "septianz@gmail.com",
    "phone": "086666666666"
  }
}
```

## Get Contact

Endpoint : GET /api/contacts/:contactId

Headers:

- Authotization: token

Response Body :

```json
{
  "data": {
    "id": 1,
    "first_name": "Septianz",
    "last_name": "Code",
    "email": "septianz@gmail.com",
    "phone": "086666666666"
  }
}
```

## Update Contact

Endpoint : PUT /api/contacts/:contactId

Headers:

- Authotization: token

Request Body:

```json
{
  "first_name": "Septianz",
  "last_name": "Code",
  "email": "septianz@gmail.com",
  "phone": "086666666666"
}
```

Response Body :

```json
{
  "data": {
    "id": 1,
    "first_name": "Septianz",
    "last_name": "Code",
    "email": "septianz@gmail.com",
    "phone": "086666666666"
  }
}
```

## Remove Contact

Endpoint : DELETE /api/contacts/:contactId

Headers:

- Authotization: token

Response Body :

```json
{
  "data": true
}
```

## Search Contact

Endpoint : GET /api/contacts

Headers:

- Authotization: token

Query Params:

- name: string, optional
- phone: string, optional
- email: string, optional
- page: number, default 1
- size: number, default 10

Response Body :

```json
{
  "data": [
    {
      "id": 1,
      "first_name": "Septianz",
      "last_name": "Code",
      "email": "septianz@gmail.com",
      "phone": "082838782492"
    },
    {
      "id": 2,
      "first_name": "Septianz",
      "last_name": "Code",
      "email": "septianz@gmail.com",
      "phone": "086666666666"
    }
  ],
  "paging": {
    "current_page": 1,
    "total_pages": 5,
    "size": 10
  }
}
```
