# Get Profile Schema

Get Profile Schema.

## Overview

**URL** : `/api/ProfileSchema/`

**Method** : `GET`

**Auth required** : YES

**Permissions required** : User can read Profile Schema -- OR -- User has a SuperUser role

**Parameters** :

```json
N/A
```

## Success Responses

**Condition** : User is authorized.

**Code** : `200 OK`

**Content example** :

```json
{
    "id": "profileSchema",
    "$schema": "http://json-schema.org/draft-07/schema",
    "$id": "http://eventcore.com/schemas/json#profileSchema",
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
