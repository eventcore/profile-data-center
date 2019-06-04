# Update Profile Schema

Update Profile Schema.

## Overview

**URL** : `/api/ProfileSchema/`

**Method** : `PUT`

**Auth required** : YES

**Permissions required** : User can update Profile Schema -- OR -- User has a SuperUser role

**Parameters** :

```json
{
  "schema":{
      "type":"object",
      "properties":{
          ...
      }
  }
}
```

## Success Responses

**Condition** : User is authorized.

**Code** : `200 OK`

**Content example** :

```json
{
  "schema":{
      "type":"object",
      "properties":{
          ...
      }
  }
}
```
