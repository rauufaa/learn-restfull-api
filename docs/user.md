# User API Spec

## Register User API
Endpoint : POST /api/users

Request Body
```json
{
    "username": "Joni",
    "password" : "1223345",
    "name" : "Joko Peni"
}
```

Response Body Success
```json
{
    "data": {
        "username": "Joni",
        "name" : "Joko Peni"
    }, 
}
```

Response Body Error
```json
{
    "errors": "Username already registered"
}
```

## Login User API
Endpoint : POST /api/users/login

Request Body
```json
{
    "username": "Joni",
    "password" : "1223345",
}
```

Response Body Success
```json
{
    "data": {
        "token": "unique-token"
    }, 
}
```

Response Body Error
```json
{
    "errors": "Username or password wrong"
}
```


## Update User API

Endpoint : PATCH /api/users/current

Headers : 
- Authorization : token

Request Body
```json
{
    "name": "Joko Peni",
    "password" : "new pass", 
}
```

Response Body Success
```json
{
    "data": {
        "username": "Joni",
        "name" : "Joko Peni", 
    }, 
}
```

Response Body Error
```json
{
    "errors": "String limit"
}
```

## Get User API
Endpoint : PATCH /api/users/current

Headers : 
- Authorization : token

Request Body
```json
{
    "name": "Joko Peni",
    "password" : "new pass", 
}
```

Response Body Success
```json
{
    "data": {
        "username": "Joni",
        "name" : "Joko Peni", 
    }, 
}
```

Response Body Error
```json
{
    "errors": "Unauthorized"
}
```


## Logout User API
Endpoint : DELETE /api/user/logout

Headers : 
- Authorization : token

Response Body Success :
```json
{
    "errors": "OK"
}
```

Response Body Success :
```json
{
    "errors": "Unauthorized"
}
```