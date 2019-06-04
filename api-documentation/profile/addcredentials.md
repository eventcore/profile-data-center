# Add Credentials

Update a Profile & add credentials.

## Overview

**URL** : `/api/Profile('{id}')`

**Method** : `POST`

**Auth required** : YES

**Permissions required** : User can update Profiles -- OR -- User has a SuperUser role

**Parameters** :

```json
{
    "querystring":{
        "id":
        {
            "required": true,
            "validation": "[Must be a valid GUID]"
        }
    },
    "body":
    {
        "oid": "anoid",
        "provider": "b2c"
    }
}
```

## Success Responses

**Condition** : User is authorized and data is valid

**Code** : `200 OK`

**Content example** :

```json
    {
        "oid": "anoid",
        "provider": "b2c"
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