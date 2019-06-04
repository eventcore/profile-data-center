# Create Profile

Create a Profile.

## Overview

**URL** : `/api/Profile/`

**Method** : `POST`

**Auth required** : YES

**Permissions required** : User can create Profiles -- OR -- User has a SuperUser role

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

**Context** : User is authorized, but event name is already used

**Code** : `409 CONFLICT`

**Content example** :

```
{}
```