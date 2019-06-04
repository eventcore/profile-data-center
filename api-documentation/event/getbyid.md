# Get Event by ID

Get a Event by ID value.

## Overview

**URL** : `/api/Event('{id}')/{subpath}`

**Method** : `GET`

**Auth required** : YES

**Permissions required** : User can read Events -- OR -- User has a SuperUser role

**Parameters** :

```json
"id":
{
    "required": true,
    "type":"string",
    "validation": "[Must be a valid Event ID]"
},
"subpath":
{
    "required": false,
    "validation":"[Must be a valid sub-path of this schema]"
}
```

## Success Responses

**Condition** : User requests event by an ID  which exists i.e. `/api/Event(12345)`

**Code** : `200 OK`

**Content example** :

```json
{
    "documentType": "RegistrationEvent",
    "id": "12345",
    "eventName": "testEvent12345",
    "startDate": "2019-05-03",
    "endDate": "2019-05-25",
    "description": "A Registration Event",
    "_ts": 1558020704
}
```

**Condition** : User requests an Event By ID which does not exist i.e. `/api/Event(00000)`

**Code** : `204 NO CONTENT`

**Content example** :

```json
{}
```
