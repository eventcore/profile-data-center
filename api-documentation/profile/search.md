# Search Profiles

Search Profiles.

## Overview

**URL** : `/api/Profile/`

**Method** : `GET`

**Auth required** : YES

**Permissions required** : User can read Profiles -- OR -- User has a SuperUser role

**Parameters** :

```json
{
    "id":
    {
        "required": true,
        "validation": "[Must be a valid GUID]"
    },
    "subpath":
    {
        "required": false,
        "validation":"[Must be a valid sub-path of this schema]"
    }
}
```

## Success Responses

**Condition** : User requests an ID which exists i.e. `/api/Profile?$filter=valid`

**Code** : `200 OK`

**Content example** :

```json
{
  "additionalProp1": {},
  "additionalProp2": {},
  "additionalProp3": {}
}
```

**Context** : User requests an ID which does not exist i.e. `/api/Profile?$filter=invalid`

**Code** : `204 NO CONTENT`

**Content example** :
```
Returns No Content if there is no Profile found by the search.
```
