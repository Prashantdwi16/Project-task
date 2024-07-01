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
curl -X POST http://127.0.0.1:8000/register/ -H "Content-Type: application/json" -d '{"username": "testuser", "email": "test@example.com", "password": "password123"}'


