# Get Event Metadata

Get Event Metadata.

## Overview

**URL** : `/api/Event/$metadata`

**Method** : `GET`

**Auth required** : YES

**Permissions required** : User can read Events -- OR -- User has a SuperUser role

## Success Responses

**Condition** : User is authorized

**Code** : `200 OK`

**Content example** :

```xml
<?xml version="1.0" encoding="utf-16"?>
<edmx:Edmx Version="4.0" xmlns:edmx="http://docs.oasis-open.org/odata/ns/edmx">
    <edmx:DataServices>
        <Schema Namespace="PDC" xmlns="http://docs.oasis-open.org/odata/ns/edm">
            <EntityType Name="Event">
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
