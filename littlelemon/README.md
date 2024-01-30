# Meta Backend Capstone
This is a capstone project for the Meta Back-End Development course

# Commands

#user:django_superuser
#email: django_superuser@gmail.com
#password: 123
pip3 install djangorestframework
```

GET in 
http://localhost:5700/api/menu/1

```json
{
    "id": 1,
    "title": "Grilled fish",
    "price": "123.00",
    "inventory": 4
}
```
GET in 
http://localhost:5700/api/menu

- Get all menus

POST http://localhost:5700/api/menu/

BODY
```json
{
    "title": "Chicken tikka",
    "price": "123.00",
    "inventory": 3
}
```
RESULT
```json
{
    "id": 2,
    "title": "Chicken tikka",
    "price": "123.00",
    "inventory": 3
}
```


GET in 
http://localhost:5700/api/booking/tables

```json
[
    {
        "id": 1,
        "name": "Tommy's Birthday",
        "number_of_guests": 6,
        "booking_date": "2023-06-06T17:41:53Z"
    }
]
```
POST http://localhost:5700/api/api-token-auth/
```json
{
    "token": "a9d2XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXc974"
}
```

navigate to http://127.0.0.1:5700/auth/token/login/ to get the token  
```
user: "django_superuser  
password: "123"
```

use http://127.0.0.1:5700/auth/token/logout/ to logout with the token in the header

