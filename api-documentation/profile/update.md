# Update Profile

Update a Profile.

## Overview

**URL** : `/api/Profile/`

**Method** : `PUT`

**Auth required** : YES

**Permissions required** : User can update Profiles -- OR -- User has a SuperUser role

**Parameters** :

```json
{
    "eventToUpdate":
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
    "eventToUpdate":
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

**Context** : User is authorized, data change references a non-existant event

**Code** : `404 NOT FOUND`

**Content example** :

```
{}
```

**Context** : User is authorized, data change attempts to rename an event

**Code** : `409 CONFLICT`

**Content example** :

```
{}
```