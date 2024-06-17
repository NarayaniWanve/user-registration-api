# Spring Boot User API

This is a simple Spring Boot application that provides a RESTful API for user registration and fetching user details.

## Running the Application

### Prerequisites

- Java 17
- Maven

### Steps to Run

1. Clone the repository:
    ```bash
    git clone https://github.com/your-username/spring-boot-user-api.git
    cd spring-boot-user-api
    ```

2. Run the application using Maven:
    ```bash
    mvn spring-boot:run
    ```

The application will start on `http://localhost:8080`.

## API Endpoints

### Register User

- **URL**: `/api/user/register`
- **Method**: `POST`
- **Request Body**:
    ```json
    {
        "username": "testuser",
        "email": "testuser@example.com",
        "password": "password"
    }
    ```

- **Curl Command**:
    ```bash
    curl -X POST http://localhost:8080/api/user/register \
    -H "Content-Type: application/json" \
    -d '{"username":"testuser", "email":"testuser@example.com", "password":"password"}'
    ```

### Fetch User

- **URL**: `/api/user/fetch`
- **Method**: `GET`
- **Query Parameter**: `username`
- **Curl Command**:
    ```bash
    curl -X GET "http://localhost:8080/api/user/fetch?username=testuser"
    ```

