# Get Profile Metadata

Get Profile Metadata.

## Overview

**URL** : `/api/Profile/$metadata`

**Method** : `GET`

**Auth required** : YES

**Permissions required** : User can read Profiles -- OR -- User has a SuperUser role

## Success Responses

**Condition** : User is authorized

**Code** : `200 OK`

**Content example** :

```xml
<?xml version="1.0" encoding="utf-16"?>
<edmx:Edmx Version="4.0" xmlns:edmx="http://docs.oasis-open.org/odata/ns/edmx">
    <edmx:DataServices>
        <Schema Namespace="PDC" xmlns="http://docs.oasis-open.org/odata/ns/edm">
            <EntityType Name="Profile">
                <Key>
                    <PropertyRef Name="id" />
                </Key>
                <Property Name="_ts" Type="Edm.Int64" />
                <Property Name="id" Type="Edm.String" />
                ...
            </EntityType>
        </Schema>
    </edmx:DataServices>
</edmx:Edmx>
```
