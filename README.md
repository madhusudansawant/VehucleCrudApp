# Vehicle Management Backend

This is the backend API for the Vehicle Management system built using **Django** and **Django REST Framework (DRF)**.  
It provides user authentication, role-based permissions, and CRUD operations for vehicle data.

---

## Features

- User Signup and Login (session-based authentication)
- Role-based permissions: `superadmin`, `admin`, `user`
- Vehicle CRUD (Create, Read, Update, Delete)
- Custom exception handling
- CSRF-exempt session authentication for APIs

---

## Tech Stack

- Python 
- Django 
- Django REST Framework
- SQLite3

---

## Installation

1. **Clone the repository (master branch)**

##API List

Below are the API endpoints with sample payloads.

1. User Signup

POST
http://127.0.0.1:8000/api/signup/

Request Body

{
    "username": "ABC12",
    "email": "abc12@gmail.com",
    "password": "abc@1234",
    "role": "user"
}


2. User Login

POST
http://127.0.0.1:8000/api/login/

Request Body

{
    "username": "ABC12",
    "password": "abc@1234"
}


3. User Logout

POST
http://127.0.0.1:8000/api/logout/


4. Create Vehicle

POST
http://127.0.0.1:8000/api/vehicles/

Request Body

{
    "vehicle_number": "MH12V2512",
    "vehicle_type": "Two",
    "vehicle_model": "Honda Dream Neo",
    "vehicle_description": "Gear Bike, 110cc"
}



5. Get Vehicles
Get All

GET
http://127.0.0.1:8000/api/vehicles/

Get One

GET
http://127.0.0.1:8000/api/vehicles/1/


6. Update Vehicle

PUT
http://127.0.0.1:8000/api/vehicles/1/

Payload Body

{
    "vehicle_number": "MH01Z1110",
    "vehicle_type": "Two",
    "vehicle_model": "Honda Activa",
    "vehicle_description": "Automatic scooter, 110cc"
}



7. Delete Vehicle

DELETE
http://127.0.0.1:8000/api/vehicles/1/
