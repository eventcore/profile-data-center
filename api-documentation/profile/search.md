# Search Profiles

Search Profile records using OData query options.

## Overview

**URL** : `/api/Profile/`

**Method** : `GET`

**Auth required** : YES

**Permissions required** : User can read Profiles -- OR -- User has a SuperUser role

**Parameters** : OData search parameters are supported - [OData - Basic Querying Tutorial](https://www.odata.org/getting-started/basic-tutorial/#queryData)

## Success Responses

**Condition** : User requests an ID which exists i.e. `/api/Profile?$filter=[valid]`

**Code** : `200 OK`

**Content example** :

```json
{
    "identities": [
        ...
    ],
    "dossier": {
        "firstName": "fn",
        "lastName": "ln",
        ...
    },
    "email": "email@domain.com",
    "events": {
        "ev1": {
            ...
        }
    },
    "documentType": "profile",
    "id": "00000000-0000-0000-0000-000000000000"
}
```

**Condition** : User requests an ID which does not exist i.e. `/api/Profile?$filter=[invalid]`

**Code** : `204 NO CONTENT`

**Content example** :

```json
{}
```

## Error Responses

**Condition** : User is authorized, data is invalid

**Code** : `400 BAD REQUEST`

**Content example** :

```json
{}
```
