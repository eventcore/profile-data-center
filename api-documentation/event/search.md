# Search Events

Search Events records using OData query options.

## Overview

**URL** : `/api/Event/`

**Method** : `GET`

**Auth required** : YES

**Permissions required** : User can read Events -- OR -- User has a SuperUser role

**Parameters** : OData search parameters are supported - [OData - Basic Querying Tutorial](https://www.odata.org/getting-started/basic-tutorial/#queryData)

## Success Responses

**Condition** : User provides search parameters which match records i.e. `/api/Event?$filter=[valid]`

**Code** : `200 OK`

**Content example** :

```json
{
  "additionalProp1": {},
  "additionalProp2": {},
  "additionalProp3": {}
}
```

**Condition** : User provides search parameters which do not match records i.e. `/api/Event?$filter=[invalid]`

**Code** : `204 NO CONTENT`

**Content example** :

```json
{}
```
