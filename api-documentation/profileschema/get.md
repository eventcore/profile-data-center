# Get Profile Schema

Get the Profile Schema for your program. Requires authorization to the program.

## Overview

**URL** : `/api/ProfileSchema/`

**Method** : `GET`

**Auth required** : YES

**Permissions required** : User can read Profile Schema -- OR -- User has a SuperUser role

## Success Responses

**Condition** : User is authorized.

**Code** : `200 OK`

**Content example** :

```json
{
    "id": "profileSchema",
    "title": "Profile Schema Test",
    "EdmKeyProperties": [
        "id"
    ],
    "type": "object",
    "properties": {
        "identities": {
          ...
        },
        "dossier":{
          ...
        },
        "events":{
          ...
        }
    }
}
```

## Error Responses

**Condition** : User is authorized, but profile schema does not exist

**Code** : `404 NOT FOUND`

**Content example** :

```json
{}
```
