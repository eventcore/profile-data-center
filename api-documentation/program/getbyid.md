# Get Program by ID

Get a Program by ID.

## Overview

**URL** : `/api/Program('{id}')/{subpath}`

**Method** : `GET`

**Auth required** : YES

**Permissions required** : User can read Programs -- OR -- User has a SuperUser role

**Parameters** :

```json
{
    "id":
    {
        "required": true,
        "type": "string",
        "validation": "[Must be a valid Program ID - 3 to 40 alphanumeric characters with no spaces]"
    },
    "subpath":
    {
        "required": false,
        "validation":"[Must be a valid sub-path of this schema]"
    }
}
```

## Success Responses

**Condition** : User requests an ID which exists i.e. `/api/Program(RealProgram)`

**Code** : `200 OK`

**Content example** :

```json
{
    "description": "Real Program",
    "id": "RealProgram",
    "_ts": 1558478289
}
```

## Error Responses

**Condition** : User requests an ID which does not exist i.e. `/api/Program(NotReal)`

**Code** : `404 NOT FOUND`

**Content example** :

```json
{}
```
