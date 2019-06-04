# Update Event

Update an Event.

## Overview

**URL** : `/api/Event/`

**Method** : `PUT`

**Auth required** : YES

**Permissions required** : User can update Events -- OR -- User has a SuperUser role

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