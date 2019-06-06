# Patch Profile Schema

Patch a program's Profile Schema.

## Overview

**URL** : `/api/ProfileSchema/`

**Method** : `PATCH`

**Auth required** : YES

**Permissions required** : User can update Profile Schema -- OR -- User has a SuperUser role

**Parameters** :

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

**Condition** : User is authorized, edits to profile schema will not generate data conflicts.

**Code** : `200 OK`

**Content example** :

```json
{}
```

## Error Responses

**Condition** : User is authorized, but edits to profile schema will generate data conflicts.

**Result** : Summary of conflicts and verification token is presented in the response. *OVERRIDE: Request can be resubmitted with the verification token value in the header*

**Code** : `409 CONFLICT`

**Content example** :

```json
{
  "message": "There are changes to this schema that would affect data!",
  "schemaChanges": [...],
  "verificationToken": "..."

}
```
