# Get Profile by ID

Get a Profile by ID.

## Overview

**URL** : `/api/Profile('{id}')/{subpath}`

**Method** : `GET`

**Auth required** : YES

**Permissions required** : User can read Profiles  -- OR -- User has a SuperUser role

**Parameters** :

```json
{
    "id":
    {
        "required": true,
        "validation": "[Must be a valid GUID]"
    },
    "subpath":
    {
        "required": false,
        "validation":"[Must be a valid sub-path of this schema]"
    }
}
```

## Success Responses

**Condition** : User requests profile by an ID  which exists i.e. `/api/Profile(00000000-0000-0000-0000-000000000000)`

**Code** : `200 OK`

**Content example** :

```json
{
  "identities": [
    {
      "oid": "string",
      "provider": "string",
      "loginEmail": "string"
    }
  ],
  "_ts": 0,
  "id": "00000000-0000-0000-0000-000000000000",
  "email": "string",
  "dossier": {
    "firstName": "string",
    "lastName": "string",
    "badgeFirstName": "string",
    "jobTitle": "string",
    "companyName": "string",
    "mobilePhone": "string",
    "websiteURL": "string",
    "region": "string",
    "countryName": "string",
    "area": "string"
  },
  "events": {
    "inspire2019": {
      "eventProfile": {
        "biography": "string",
        "photoURL": "string",
        "mpnID": "string",
        "attendeeMessaging": true,
        "meetingScheduler": true,
        "eventsPreviouslyAttended": [
          "Microsoft Build"
        ],
        "priorityContentAreas": [
          "Application & Infrastructure"
        ],
        "titleThatDescribesYou": "Executive Management",
        "jobFunction": "Alliances",
        "jobFunctionOther": "string",
        "customerSegment": [
          "Enterprise"
        ],
        "businessFocus": "string",
        "industryFocus": [
          "Cross Industry"
        ],
        "msProductsAlign": "string",
        "msFunctionsAlign": "string",
        "fieldCorp": "string"
      },
      "registrantStatus": "Registered",
      "registrantType": "Partner - All Access",
      "classificationName": "Microsoft",
      "inspireLogin": true,
      "displaySessions": true,
      "displayProfileToPublic": true
    }
  }
}
```
**Context** : User requests an ID which does not exist i.e. `/api/Profile(00000000-0000-0000-0000-000000000001)`

**Code** : `204 NO CONTENT`

**Content example** : 
```json
{}
```