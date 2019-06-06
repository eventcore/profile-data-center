# Create Profile

Create a Profile.

## Overview

**URL** : `/api/Profile/`

**Method** : `POST`

**Auth required** : YES

**Permissions required** : User can create Profiles -- OR -- User has a SuperUser role

**Parameters** : Profile data must be supplied in the request body

***Body***

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

## Success Responses

**Condition** : User is authorized and data is valid

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
    "createdDate": 1234567890,
    "id": "00000000-0000-0000-0000-000000000000"
}
```

## Error Responses

**Condition** : User is authorized, data is invalid

**Code** : `400 BAD REQUEST`

**Content example** :

```json
{}
```

**Condition** : User is authorized, but the profile ID already exists

**Code** : `409 CONFLICT`

**Content example** :

```json
{}
```

**Condition** : User is authorized, but the profile email already exists

**Code** : `409 CONFLICT`

**Content example** :

```json
{}
```

**Condition** : User is authorized, but a credential in the profile is already used

**Code** : `409 CONFLICT`

**Content example** :

```json
{}
```
