# Patch Profile External Schema Section

A PATCH endpoint intened to allow third party developers to define their own properties on the Profile schema and share data with other third parth vendors without eventcore's involvement.

These properties are specific to the event they are created in.  The full path to these properties on the Profile will be 'events.{eventName}._externalprovider.{property}'.

## Overview

**URL** : `/api/ProfileSchema/{eventName}`

**Method** : `PATCH`

**Auth required** : YES

**Permissions required** : User can update Profile Schema -- OR -- User has a SuperUser role

**Parameters** :

***Querystring***

```json
"eventName": {
  "required": true,
  "type": "string"
}
```

***Header***

```json
"verificationToken": {
  "required": false,
  "type": "string"
}
```

***Body***: Accepts a collection of JSON Patch objects

```json
[
  {
    "value": {},
    "path": "string",
    "op": "string",
    "from": "string"
  }
]
```

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

**Condition** : User is authorized, but edits to profile schema will generate data conflicts. Summary of conflicts and verification token is presented in the response.

**Code** : `409 CONFLICT`

**Content example** :

```json
{
  "message": "There are changes to this schema that would affect data!",
  "schemaChanges": [...],
  "verificationToken": "..."
}
```
