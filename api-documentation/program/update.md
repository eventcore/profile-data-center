# Update Program

Update a Program.

## Overview

**URL** : `/api/Program/`

**Method** : `PUT`

**Auth required** : YES

**Permissions required** : User can update Programs -- OR -- User has a SuperUser role

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
    "ProgramToUpdate":
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

```json
{}
```

**Context** : User is authorized, data change references a non-existant event

**Code** : `404 NOT FOUND`

**Content example** :

```json
{}
```

**Context** : User is authorized, data change attempts to rename an event

**Code** : `409 CONFLICT`

**Content example** :

```json
{}
```
