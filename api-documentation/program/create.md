# Create Program

Adds a new program using the provided program name (Id).

## Overview

**URL** : `/api/Program/`

**Method** : `POST`

**Auth required** : YES

**Permissions required** : User can create Programs -- OR -- User has a SuperUser role

**Parameters** :

***Body***

```json
{
  "displayName": "string",
  "description": "string",
  "id": "string"
}
```

## Success Responses

**Condition** : User is authorized and data is valid

**Code** : `200 OK`

**Content example** :

```json
    "eventToCreate":
    {
        "type": object,
        "properties": {
            ...
        }
    }
```

## Error Responses

**Condition** : User is authorized, data is invalid

**Code** : `400 BAD REQUEST`

**Content example** :

```json
{}
```

**Condition** : User is authorized, but Program name is already used

**Code** : `409 CONFLICT`

**Content example** :

```json
{}
```
