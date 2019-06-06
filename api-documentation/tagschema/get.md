# Get Tag Schema

Returns a JSON schema for the tags of the current PDC-Program. This schema defines all the fields and field restrictions for tags in the current program.

## Overview

**URL** : `/api/TagSchema/`

**Method** : `GET`

**Auth required** : YES

**Permissions required** : User can read Tag Schema -- OR -- User has a SuperUser role

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
