# Add Credentials

Update a Profile and add credentials.

## Overview

**URL** : `/api/Profile('{id}')`

**Method** : `POST`

**Auth required** : YES

**Permissions required** : User can update Profiles -- OR -- User has a SuperUser role

**Parameters** :

***Querystring***

```json
"id":
{
    "required": true,
    "validation": "[Must be a valid GUID]"
}
```

***Body***: Must be a valid Profile Credential object (in JSON schema format)

```json
{
    "oid": "anoid",
    "provider": "b2c"
}
```

## Success Responses

**Condition** : User is authorized and data is valid

**Code** : `200 OK`

**Content example** :

```json
{
    "oid": "anoid",
    "provider": "b2c"
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
{ "error" : "Cannot modify profile because it has been marked as deleted" }
```

**Condition** : User is authorized, id references a non-existent profile

**Code** : `404 NOT FOUND`

**Content example** :

```json
{}
```

**Condition** : User is authorized, data change attempts to add an already existing credential

**Code** : `409 CONFLICT`

**Content example** :

```json
{}
```
