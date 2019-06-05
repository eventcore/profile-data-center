# Migrate Profile

Migrate a Profile from one ID value to another.

## Overview

**URL** : `/api/Profile/`

**Method** : `PUT`

**Auth required** : YES

**Permissions required** : User can migrate Profiles -- OR -- User has a SuperUser role

**Parameters** :

```json
"fromId":
{
    "required":true,
    "type": "string",
    "validation": "No fromId was provided. Please provide a fromId in the request."
},
"toId":
{
    "required":true,
    "type": "string",
    "validation": "No toId was provided. Please provide a toId in the request."
}
```

## Success Responses

**Condition** : User is authorized and data is valid

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

**Condition** : User is authorized, but profile in either fromId or toId does not exist

**Code** : `404 NOT FOUND`

**Content example** :

```json
{}
```

**Condition** : User is authorized, but profile in either fromId or toId has been marked as deleted

**Code** : `400 BAD REQUEST`

**Content example** :

```json
{}
```
