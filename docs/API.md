# API Documentation

## Authentication

### Login
- **Endpoint**: `/api/auth/login`
- **Method**: `POST`
- **Request Example**:
```json
{
  "username": "string",
  "password": "string"
}
```
- **Response Example**:
```json
{
  "token": "string",
  "user": {
    "id": "string",
    "username": "string"
  }
}
```

## User Profiles

### Get User Profile
- **Endpoint**: `/api/user/{id}`
- **Method**: `GET`
- **Response Example**:
```json
{
  "id": "string",
  "username": "string",
  "profile_picture": "string",
  "bio": "string"
}
```

### Update User Profile
- **Endpoint**: `/api/user/{id}`
- **Method**: `PUT`
- **Request Example**:
```json
{
  "bio": "string",
  "profile_picture": "string"
}
```
- **Response Example**:
```json
{
  "success": true
}
```

## Matching

### Get Matches
- **Endpoint**: `/api/matching/matches`
- **Method**: `GET`
- **Response Example**:
```json
[
  {
    "id": "string",
    "username": "string",
    "match_score": "number"
  }
]
```

## Messaging

### Send Message
- **Endpoint**: `/api/messages/send`
- **Method**: `POST`
- **Request Example**:
```json
{
  "recipient_id": "string",
  "message": "string"
}
```
- **Response Example**:
```json
{
  "success": true
}
```

### Get Messages
- **Endpoint**: `/api/messages/{userId}`
- **Method**: `GET`
- **Response Example**:
```json
[
  {
    "sender_id": "string",
    "message": "string",
    "timestamp": "string"
  }
]
```

## AI Assistant

### Get Assistant Response
- **Endpoint**: `/api/ai/assistant`
- **Method**: `POST`
- **Request Example**:
```json
{
  "query": "string"
}
```
- **Response Example**:
```json
{
  "response": "string"
}
```