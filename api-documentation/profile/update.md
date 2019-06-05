# Update Profile

Update a Profile.

## Overview

**URL** : `/api/Profile/`

**Method** : `PUT`

**Auth required** : YES

**Permissions required** : User can update Profiles -- OR -- User has a SuperUser role

**Parameters** :

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

**Condition** : User is authorized, but profile is marked for deletion

**Code** : `400 BAD REQUEST`

**Content example** :

```json
{ "message" : "Cannot modify profile because it has been marked as deleted" }
```

**Condition** : User is authorized, data change attempts to update profile ID to value which does not exist

**Code** : `404 NOT FOUND`

**Content example** :

```json
{}
```

**Condition** : User is authorized, data change attempts to update email to a value which already exists

**Code** : `409 CONFLICT`

**Content example** :

```json
{}
```

**Condition** : User is authorized, data change attempts to update an already migrated profile. Response contains a verification token to resubmit the request.

**Code** : `409 CONFLICT`

**Content example** :

```json
{
    "message": "Profile with id '<Id>' has been migrated! Verify that you want to apply these updates to the profile by resending the request with the attached verification token in a querystring parameter 'verificationToken'",
    "verificationToken": "..."
}
```
