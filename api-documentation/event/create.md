# Create Event

Create a new Event within a program.

## Overview

**URL** : `/api/Event/`

**Method** : `POST`

**Auth required** : YES - User must be authenticated to the Program.

**Permissions required** : User can create Events -- OR -- User has a SuperUser role

**Parameters** :

```json
{
    "documentType": "RegistrationEvent",
    "id": "12345",
    "eventName": "testEvent",
    "startDate": "2019-05-03",
    "endDate": "2019-05-25",
    "description": "A Test Event",
}
```

## Success Responses

**Condition** : User is authorized and data is valid

**Code** : `200 OK`

**Content example** :

```json
{
    "documentType": "RegistrationEvent",
    "id": "12345",
    "eventName": "testEvent",
    "startDate": "2019-05-03",
    "endDate": "2019-05-25",
    "description": "A Test Event",
    "_rid": "2MQgAMkBvuoGAAAAAAAAAA==",
    "_ts": 1558020704
}
```

## Error Responses

**Condition** : User is authorized, data is invalid.

**Code** : `400 BAD REQUEST`

**Content example** :

```json
{}
```

**Condition** : User is authorized, but event name already exists.

**Code** : `409 CONFLICT`

**Content example** :

```json
{}
```
