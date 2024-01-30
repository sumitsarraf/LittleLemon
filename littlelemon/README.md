# Meta Backend Capstone
This is a capstone project for the Meta Back-End Development course

# Commands

``` bash
# to create venv
python -m venv backend-capstone

# to activate venv
backend-capstone\Scripts\activate

# To install django
pip install django

# create a django project
django-admin startproject littlelemon

# run development server
cd littlelemon
python manage.py runserver

# create a django app 
python manage.py startapp restaurant

# install mysqlclient
pip3 install mysqlclient
```

```sql
create database littlelemon;
use littlelemon;

```

```bash
python manage.py makemigrations

python manage.py migrate 

# to create a user
python manage.py createsuperuser

#user:django_superuser
#email: django_superuser@gmail.com
#password: 123
pip3 install djangorestframework
```

GET in 
http://localhost:8000/api/menu/1

```json
{
    "id": 1,
    "title": "Grilled fish",
    "price": "123.00",
    "inventory": 4
}
```
GET in 
http://localhost:8000/api/menu

- Get all menus

POST http://localhost:8000/api/menu/

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
http://localhost:8000/api/booking/tables

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
POST http://localhost:8000/api/api-token-auth/
```json
{
    "token": "a9d2XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXc974"
}
```

Add authorization to the endpoints, so you have to send a header in the request with the Authorization title: Token [VALUE]

```bash
pip install djoser
```

navigate to http://127.0.0.1:8000/auth/token/login/ to get the token  
```
user: "django_superuser  
password: "123"
```

use http://127.0.0.1:8000/auth/token/logout/ to logout with the token in the header


Utilize this path to verify that the web application is serving static HTML content, inclusive of images and styling.
/restaurant

For testing, you can make use of the following API endpoints with Insomnia or Postman clients.
Alternatively, feel free to explore them through your browser of choice.

DJOSER endpoint, for instance, to perform a POST request and register a new user.
/auth/users/

To log in and obtain an authentication token.
/api-token-auth/

To log in using the DJOSER endpoint.
/auth/token/login

Menu items
/api/menu/
/api/menu/{menuItemId}

Table reservations
/api/booking/tables/
/api/booking/tables/{bookingId}


