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
