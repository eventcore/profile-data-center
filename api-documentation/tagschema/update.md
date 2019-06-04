# Update Tag Schema

Update Tag Schema.

## Overview

**URL** : `/api/TagSchema/`

**Method** : `PUT`

**Auth required** : YES

**Permissions required** : User can update Tag Schema -- OR -- User has a SuperUser role

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
