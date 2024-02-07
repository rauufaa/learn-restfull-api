# Contact API Spec

## Create Contact API
Endpoint : POST /api/contacts

Header : 
- Authorization : token 

Request Body
```json
{
    "first_name": "Joko",
    "last_name" : "Peni",
    "email" : "joni@gmail.com",
    "phone" : "08124124"
}
```

Response Body Success
```json
{
    "data": {
        "id": 1,
        "first_name": "Joko",
        "last_name" : "Peni",
        "email" : "joni@gmail.com",
        "phone" : "08124124"
    }, 
}
```

Response Body Error
```json
{
    "errors": "Email not valid"
}
```

## Update Contact API
Endpoint : PUT /api/contacts/:id

Request Body
```json
{
    "first_name": "Joko",
    "last_name" : "Peni",
    "email" : "joni@gmail.com",
    "phone" : "08124124"
}
```

Response Body Success
```json
{
    "data": {
        "id": 1,
        "first_name": "Joko",
        "last_name" : "Peni",
        "email" : "joni@gmail.com",
        "phone" : "08124124"
    }, 
}
```

Response Body Error
```json
{
    "errors": "Not valid"
}
```


## Get Contacts API

Endpoint : GET /api/contacts/:id

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
        "id": 1,
        "first_name": "Joko",
        "last_name" : "Peni",
        "email" : "joni@gmail.com",
        "phone" : "08124124" 
    }, 
}
```

Response Body Error
```json
{
    "errors": "Not Found"
}
```

## Search Contact API
Endpoint : Get /api/contact

Headers : 
- Authorization : token

Query Params :
- name : search by name, optional
- email : search by email like, opt
- phone : search by phone like, opt
- page : page number, default 1
- size : size per page, default 10

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
    "data": [
        {
           "id": 1,
            "first_name": "Joko",
            "last_name" : "Peni",
            "email" : "joni@gmail.com",
            "phone" : "08124124"  
        },
    ],
    "paging" : {
        "page" : 1, 
        "total_page" : 3,
        "total_item" : 12
    }    
}
```

Response Body Error
```json
{
    "errors": "Not Found"
}
```


## Remove Contact API
Endpoint : DELETE /api/contacts/:id

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
    "errors": "Contact nt found"
}
```