# Get Changelog Count

Get Changelog Count.

## Overview

**URL** : `/api/Changelog/$count`

**Method** : `GET`

**Auth required** : ?

**Permissions required** : User can read Changelogs  -- OR -- User has a SuperUser role

**Parameters** :

```json
{
    "count":
    {
        "required": true,
        "validation": "[Must be the explicit value $count]"
    }
}
```

## Success Responses

**Code** : `200 OK`

**Content example** :

```json
{
  "value": {
      12345
  }
} 
```
