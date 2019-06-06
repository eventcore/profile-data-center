# Update Tag Schema

Replaces the existing tag schema with the schema posted in the request body.

## Overview

**URL** : `/api/TagSchema/`

**Method** : `PUT`

**Auth required** : YES

**Permissions required** : User can update Tag Schema -- OR -- User has a SuperUser role

**Parameters** :

***Body***

```json
{
  "tags": {
    "additionalProp1": [
      "string"
    ],
    "additionalProp2": [
      "string"
    ],
    "additionalProp3": [
      "string"
    ]
  }
}
```

## Success Responses

**Condition** : User is authorized.

**Code** : `200 OK`

**Content example** :

```json
{
  "tags": {
    "additionalProp1": [
      "string"
    ],
    "additionalProp2": [
      "string"
    ],
    "additionalProp3": [
      "string"
    ]
  }
}
```
