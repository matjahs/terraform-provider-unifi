---
title: "UniFi API"
source: https://developer.ui.com/network/v10.1.84/getfirewallpolicies
date: 2026-03-08T18:45:15.584378+00:00
---

# List Firewall Policies

```http
GET /v1/sites/{siteId}/firewall/policies
```

Retrieve a list of all firewall policies on a site.

### Filterable Properties

| Name | Type | Allowed functions |
| --- | --- | --- |
| `id` | `uuid` | `eq`, `ne`, `in`, `notIn` |
| `name` | `string` | `eq`, `ne`, `in`, `notIn`, `like` |
| `source.zoneId` | `uuid` | `eq`, `ne`, `in`, `notIn` |
| `destination.zoneId` | `uuid` | `eq`, `ne`, `in`, `notIn` |
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
| `dataExpand` | yes | `array<object> (Firewall policy)` |
