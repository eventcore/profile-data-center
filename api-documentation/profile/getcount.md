# Get Profile Count

Get Profile Count.

## Overview

**URL** : `/api/Profile/$count`

**Method** : `GET`

**Auth required** : ?

**Permissions required** : User can read Profiles  -- OR -- User has a SuperUser role

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
