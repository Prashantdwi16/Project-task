# Django JWT Authentication

## How to Run

Ensure you have Docker and Docker Compose installed on your system. Then, follow these steps:

1. Clone the repository:
    ```sh
    git clone https://github.com/yourusername/django-jwt-auth.git
    cd django-jwt-auth
    ```

2. Build and start the Docker containers:
    ```sh
    docker-compose up --build
    ```

3. The API will be available at `http://127.0.0.1:8000/`.

## API Endpoints and cURL Commands

### Register a User
```sh
curl -X POST http://127.0.0.1:8000/app1/register/ -H "Content-Type: application/json" -d '{"username": "testuser", "email": "test@example.com", "password": "password123"}'

### Obtain JWT Token:
curl -X POST http://127.0.0.1:8000/app1/token/ -H "Content-Type: application/json" -d "{\"username\": \"testuser\", \"password\": \"password123\"}"

### Access Protected View:
curl -X GET http://127.0.0.1:8000/app1/protected/ -H "Authorization: Bearer <access_token_here>"

#Refresh Token:
curl -X POST http://127.0.0.1:8000/app1/token/refresh/ -H "Content-Type: application/json" -d "{\"refresh\": \"<refresh_token_here>\"}"

#Logout (Revoke Token):
curl -X POST http://127.0.0.1:8000/app1/logout/ -H "Authorization: Bearer <access_token_here>" -H "Content-Type: application/json" -d "{\"refresh\": \"<refresh_token_here>\"}"
