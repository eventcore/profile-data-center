# Search Profiles

Search Profiles.

## Overview

**URL** : `/api/Profile/`

**Method** : `GET`

**Auth required** : YES

**Permissions required** : User can read Profiles -- OR -- User has a SuperUser role

**Parameters** : OData search parameters are supported - [OData - Basic Querying Tutorial](https://www.odata.org/getting-started/basic-tutorial/#queryData)

## Success Responses

**Condition** : User requests an ID which exists i.e. `/api/Profile?$filter=valid`

**Code** : `200 OK`

**Content example** :

```json
{
  "additionalProp1": {},
  "additionalProp2": {},
  "additionalProp3": {}
}
```

**Condition** : User requests an ID which does not exist i.e. `/api/Profile?$filter=invalid`

**Code** : `204 NO CONTENT`

**Content example** :

```json
{}
```
