# Update Event

Update an Event. Replace the contents/properties of the event

## Overview

**URL** : `/api/Event/`

**Method** : `PUT`

**Auth required** : YES

**Permissions required** : User can update Events -- OR -- User has a SuperUser role

**Parameters** : Event data must be supplied in the request body

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

**Condition** : User is authorized, data change references a non-existent event.

**Code** : `404 NOT FOUND`

**Content example** :

```json
{}
```

**Condition** : User is authorized, data change attempts to rename an event to a name which already exists.

**Code** : `409 CONFLICT`

**Content example** :

```json
{}
```
