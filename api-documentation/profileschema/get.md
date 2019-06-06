# Get Profile Schema

Returns a JSON schema for the profile of the current PDC-Program. This schema defines all the fields and field restrictions for profiles in the current program.

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
