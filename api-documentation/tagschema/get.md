# Get Tag Schema

Get Tag Schema.

## Overview

**URL** : `/api/TagSchema/`

**Method** : `GET`

**Auth required** : YES

**Permissions required** : User can read Tag Schema -- OR -- User has a SuperUser role

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
