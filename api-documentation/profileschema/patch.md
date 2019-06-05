# Patch Profile Schema

Patch Profile Schema.

## Overview

**URL** : `/api/ProfileSchema/`

**Method** : `PATCH`

**Auth required** : YES

**Permissions required** : User can update Profile Schema -- OR -- User has a SuperUser role

**Parameters** :

```json
{
  "schema":{
      "type":"object",
      "properties":{
          ...
      }
  }
}
```

## Success Responses

**Condition** : User is authorized.

**Code** : `200 OK`

**Content example** :

```json
{
  "schema":{
      "type":"object",
      "properties":{
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
