# Migrate Profile

Migrate a Profile.

## Overview

**URL** : `/api/Profile/`

**Method** : `PUT`

**Auth required** : YES

**Permissions required** : User can migrate Profiles -- OR -- User has a SuperUser role

**Parameters** :

```json
{
    "fromId":
    {
        "required":true,
        "type": "string",
        "validation": "No fromId was provided. Please provide a fromId in the request."
    },
    "toId":
    {
        "required":true,
        "type": "string",
        "validation": "No toId was provided. Please provide a toId in the request."
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

**Condition** : User is authorized, data is invalid

**Code** : `400 BAD REQUEST`

**Content example** :

```json
{}
```

**Condition** : User is authorized, but profile in either fromId or toId does not exist

**Code** : `404 NOT FOUND`

**Content example** :

```json
{}
```

**Condition** : User is authorized, but profile in either fromId or toId has been marked as deleted

**Code** : `400 BAD REQUEST`

**Content example** :

```json
{}
```
