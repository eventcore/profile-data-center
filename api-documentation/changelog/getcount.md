# Get Changelog Count

Get a count of all changelog records within a program.

## Overview

**URL** : `/api/Changelog/$count`

**Method** : `GET`

**Auth required** : YES

**Permissions required** : User can read Changelogs  -- OR -- User has a SuperUser role

**Parameters** :

```json
{
    "$count":
    {
        "required": true,
        "validation": "[Must be the explicit value $count]"
    }
}
```

## Success Responses

**Condition** : User is authorized

**Code** : `200 OK`

**Content example** :

```json
12345
```
