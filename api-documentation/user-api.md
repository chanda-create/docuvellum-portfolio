# 🟦 User API Documentation

## 1. Overview
This API provides access to user data, including personal details, address, and company information.

## 2. Base URL
BAll API requests should be made to the following base URL:

https://jsonplaceholder.typicode.com

## 3. Endpoint
### Get all users
This endpoint retrieves a list of all users from the system.
```http
GET https://jsonplaceholder.typicode.com/users
```

## 4. Request Example
### Using HTTP
```http
GET https://jsonplaceholder.typicode.com/users
```
### Using cURL
```bash
curl -X GET https://jsonplaceholder.typicode.com/users
```
## 5. Response Example
### 200 OK
The request was successful and user information has been retrieved.
```json
    {
        "id": 1,
        "name": "Leanne Graham",
        "username": "Bret",
        "email": "Sincere@april.biz",
        "address": {
            "street": "Kulas Light",
            "suite": "Apt. 556",
            "city": "Gwenborough",
            "zipcode": "92998-3874",
            "geo": {
                "lat": "-37.3159",
                "lng": "81.1496"
            }
        },
        "phone": "1-770-736-8031 x56442",
        "website": "hildegard.org",
        "company": {
            "name": "Romaguera-Crona",
            "catchPhrase": "Multi-layered client-server neural-net",
            "bs": "harness real-time e-markets"
        }
    }
```

## 6. Field Description 
|Field      | Description                |
|-----------|----------------------------|
| id        | Unique identifier for user |
| name      | Full name of the user      |
| username  | User Name                  | 
| email     | User's Email address       |
| address   | User’s Location details    |
| phone     | User's Phone number        |
| website   | User's Website             |
| company   | Organization details       |

## 7. Error Handling
### 404 Not Found
Returned when the requested user ID does not exist.
```json
{
  "error": "User not found"
}
```
### 400 Bad Request
Returned when the request is invalid.
```json
{
  "error": "Invalid request parameter"
}
```
### 500 Internal Server Error
Returned when something goes wrong on the server.
```json
{
  "error": "Internal server error"
}
```
### 8. Status Codes
- 200 OK – Request successful
- 404 Not Found – User not found
- 400 Bad Request – Invalid request parameter
- 500 Internal Server Error – Internal server error
