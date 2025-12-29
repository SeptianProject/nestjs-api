# User API Spec

## Register User

Endpoint : POST /api/users

Request Body :

```json
{
  "username": "septianz",
  "password": "secret",
  "name": "SeptianzCode"
}
```

Response Body (Success) :

```json
{
  "data": {
    "username": "septianz",
    "name": "SeptianzCode"
  }
}
```

Response Body (Failed) :

```json
{
  "errors": "Username already exists"
}
```

## Login User

Endpoint : POST /api/users/login

Request Body :

```json
{
  "username": "septianz",
  "password": "secret"
}
```

Response Body (Success) :

```json
{
  "data": {
    "username": "septianz",
    "name": "SeptianzCode",
    "token": "session_id_generated"
  }
}
```

Response Body (Failed) :

```json
{
  "errors": "Username or password is wrong"
}
```

## Get User

Endpoint : GET /api/users/current

Headers :

- Authorization: token

Response Body (Success) :

```json
{
  "data": {
    "username": "septianz",
    "name": "SeptianzCode"
  }
}
```

Response Body (Failed) :

```json
{
  "errors": "Unauthorized"
}
```

## Update User

Endpoint : PATCH /api/users/current

Headers :

- Authorization: token

Request Body :

```json
{
  "name": "SeptianzCode", // optional
  "password": "secret" // optional
}
```

Response Body (Success) :

```json
{
  "data": {
    "username": "string",
    "name": "string"
  }
}
```

## Logout User

Endpoint : DELETE /api/users/current

Headers :

- Authorization: token

Response Body (Success) :

```json
{
  "data": true
}
```
