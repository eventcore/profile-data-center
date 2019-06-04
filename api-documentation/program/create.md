# Create Program

Create a Program.

## Overview

**URL** : `/api/Program/`

**Method** : `POST`

**Auth required** : YES

**Permissions required** : User can create Programs -- OR -- User has a SuperUser role

**Parameters** :

```json
{
    "eventToCreate":
    {
        "type": object,
        "properties": {
            ...
        }
    }
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

**Context** : User is authorized, data is invalid

**Code** : `400 BAD REQUEST`

**Content example** :

```
{}
```

**Context** : User is authorized, but Program name is already used

**Code** : `409 CONFLICT`

**Content example** :

```
{}
```