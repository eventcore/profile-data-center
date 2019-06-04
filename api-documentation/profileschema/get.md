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
  "schema":{
      "type":"object",
      "properties":{
          ...
      }
  }
}
```
