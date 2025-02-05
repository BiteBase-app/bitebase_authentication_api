# Bitebase Authentication API

## Overview
The Bitebase Authentication API provides endpoints for user authentication and authorization. This includes user registration, login, password management, and token handling.

## Base URL
```
https://api.bitebase.com/v1
```

## Endpoints

### User Registration
**POST** `/auth/register`

#### Request
```json
{
  "username": "string",
  "email": "string",
  "password": "string"
}
```

#### Response
```json
{
  "id": "string",
  "username": "string",
  "email": "string",
  "createdAt": "string"
}
```

### User Login
**POST** `/auth/login`

#### Request
```json
{
  "email": "string",
  "password": "string"
}
```

#### Response
```json
{
  "token": "string",
  "expiresIn": "number"
}
```

### Password Reset Request
**POST** `/auth/password-reset-request`

#### Request
```json
{
  "email": "string"
}
```

#### Response
```json
{
  "message": "string"
}
```

### Password Reset
**POST** `/auth/password-reset`

#### Request
```json
{
  "token": "string",
  "newPassword": "string"
}
```

#### Response
```json
{
  "message": "string"
}
```

### Token Refresh
**POST** `/auth/token-refresh`

#### Request
```json
{
  "refreshToken": "string"
}
```

#### Response
```json
{
  "token": "string",
  "expiresIn": "number"
}
```

## Error Handling
All error responses follow the structure below:

#### Response
```json
{
  "error": "string",
  "message": "string"
}
```

## Contact
For any questions or support, please contact [support@bitebase.com](mailto:support@bitebase.com).