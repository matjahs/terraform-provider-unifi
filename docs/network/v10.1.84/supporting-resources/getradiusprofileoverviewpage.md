---
title: "UniFi API"
source: https://developer.ui.com/network/v10.1.84/getradiusprofileoverviewpage
date: 2026-03-08T18:45:46.119824+00:00
---

# List Radius Profiles

```http
GET /v1/sites/{siteId}/radius/profiles
```

Returns available RADIUS authentication profiles, including configuration origin metadata.

### Filterable Properties

| Name | Type | Allowed functions |
| --- | --- | --- |
| `id` | `uuid` | `eq`, `ne`, `in`, `notIn` |
| `name` | `string` | `eq`, `ne`, `in`, `notIn`, `like` |
| `metadata.origin` | `string` | `eq`, `ne`, `in`, `notIn` |

### Path Parameters

| Name | Required | Type |
| --- | --- | --- |
| `siteId` | yes | `string` |

### Query Parameters

| Name | Required | Type |
| --- | --- | --- |
| `offset` | no | `integer` |
| `limit` | no | `integer` |
| `filter` | no | `string` |

## Responses

### 200

Response schema: `application/json`

| Field | Required | Type |
| --- | --- | --- |
| `offset` | yes | `integer` |
| `limit` | yes | `integer` |
| `count` | yes | `integer` |
| `totalCount` | yes | `integer` |
| `dataExpand` | yes | `array<object> (Radius Profile Overview)` |
