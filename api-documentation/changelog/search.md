# Search Changelogs

Search Changelog records using OData query options.

## Overview

**URL** : `/api/Changelog/`

**Method** : `GET`

**Auth required** : YES

**Permissions required** : User can read Changelogs -- OR -- User has a SuperUser role

**Parameters** : OData search parameters are supported - [OData - Basic Querying Tutorial](https://www.odata.org/getting-started/basic-tutorial/#queryData)

## Success Responses

**Condition** : User provides search parameters which match records i.e. `/api/Changelog?$filter=valid`

**Code** : `200 OK`

**Content example** :

```json
{
  "additionalProp1": {},
  "additionalProp2": {},
  "additionalProp3": {}
}
```

**Condition** : User provides search parameters which do not match records i.e. `/api/Changelog?$filter=invalid`

**Code** : `204 NO CONTENT`

**Content example** :

```json
{}
```
