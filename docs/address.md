# Address API Spec

## Create Address API

Endpoint : POST /api/contacts/:contactid/adressess

Headers : 
- Authorization : token

Request Body :
```json
{
    "street": "Jl, Pramuka",
    "city": "Pesawarn",
    "province": "Lampung",
    "country": "Indonesia",
    "postal_code": "55221",
}
```

Request Body Success :
```json
{
    "data": {
        "id": 1,
        "street": "Jl, Pramuka",
        "city": "Pesawarn",
        "province": "Lampung",
        "country": "Indonesia",
        "postal_code": "55221",
    }
    
}
```

Request Body Errors:
```json
{
    "errors": "Something went wrong"
}
```

## Update Address API

Endpoint : PUT /api/contacts/:contactid/adressess/:addressid

Headers : 
- Authorization : token

Request Body :
```json
{
    "street": "Jl, Pramuka",
    "city": "Pesawarn",
    "province": "Lampung",
    "country": "Indonesia",
    "postal_code": "55221",
}
```

Request Body Success :
```json
{
    "data": {
        "id": 1,
        "street": "Jl, Pramuka",
        "city": "Pesawarn",
        "province": "Lampung",
        "country": "Indonesia",
        "postal_code": "55221",
    }
    
}
```

Request Body Errors:
```json
{
    "errors": "Something went wrong"
}
```

## Get Address API

Endpoint : GET /api/contacts/:contactid/adressess/:addressid

Headers : 
- Authorization : token

Request Body Success :
```json
{
    "data": {
        "id": 1,
        "street": "Jl, Pramuka",
        "city": "Pesawarn",
        "province": "Lampung",
        "country": "Indonesia",
        "postal_code": "55221",
    }
    
}
```

Request Body Errors:
```json
{
    "errors": "Contact not found"
}
```
## List Address API

Endpoint : GET /api/contacts/:contactid/adressess

Headers : 
- Authorization : token

Request Body Success :
```json
{
    "data": [
        {
            "id": 1,
            "street": "Jl, Pramuka",
            "city": "Pesawarn",
            "province": "Lampung",
            "country": "Indonesia",
            "postal_code": "55221",
        },
        {
            "id": 1,
            "street": "Jl, Pramuka",
            "city": "Pesawarn",
            "province": "Lampung",
            "country": "Indonesia",
            "postal_code": "55221",
        }
    ] 
    
}
```

Request Body Errors:
```json
{
    "errors": "Contact not found"
}
```

## Remove Address API
Endpoint : DELETE /api/contacts/:contactid/adressess/:addressid

Headers : 
- Authorization : token

Request Body Success :
```json
{
    "data": "Ok"
    
}
```

Request Body Errors:
```json
{
    "errors": "Addres not found"
}
```