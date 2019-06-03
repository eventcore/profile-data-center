# Get Changelog by ID

Get a Changelog by ID.

## Overview

**URL** : `/api/Changelog('{id}')/{subpath}`

**Method** : `GET`

**Auth required** : YES

**Permissions required** : User can read Changelogs -- OR -- User has a SuperUser role

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

**Condition** : User requests changelog by an ID  which exists i.e. `/api/Changelog(00000000-0000-0000-0000-000000000000)`

**Code** : `200 OK`

**Content example** :

```json
{
  "additionalProp1": {},
  "additionalProp2": {},
  "additionalProp3": {}
}
```

**Context** : User requests an ID which does not exist i.e. `/api/Profile(00000000-0000-0000-0000-000000000001)`

**Code** : `204 NO CONTENT`

**Content example** :
```
Returns No Content if there is no Changelog found by the search.
```
