# Delete Profile

Delete Profile.

## Overview

**URL** : `/api/Profile('{id}')`

**Method** : `GET`

**Auth required** : ?

**Permissions required** : User can delete Profiles  -- OR -- User has a SuperUser role

**Parameters** :

```json
{
    "id":
    {
        "required": true,
        "validation": "[Must be a valid GUID]"
    },
    "reason":
    {
        "required": true,
        "validation":"[Must be a valid string - a reason must be provided in the request]"
    }
}
```

## Success Responses

**Code** : `200 OK`

**Content example** :

```json
{
  "value": {
      12345
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

**Context** : User is authorized, but provided ID does not exist

**Code** : `404 NOT FOUND`

**Content example** :

```json
{}
```
