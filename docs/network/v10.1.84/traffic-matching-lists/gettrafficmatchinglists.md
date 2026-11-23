---
title: "UniFi API"
source: https://developer.ui.com/network/v10.1.84/gettrafficmatchinglists
date: 2026-03-08T18:45:39.797124+00:00
---

# List Traffic Matching Lists

```http
GET /v1/sites/{siteId}/traffic-matching-lists
```

Retrieve all traffic matching lists on a site.

### Filterable Properties

| Name | Type | Allowed functions |
| --- | --- | --- |
| `id` | `uuid` | `eq`, `ne`, `in`, `notIn` |
| `name` | `string` | `eq`, `ne`, `in`, `notIn`, `like` |

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
| `dataExpand` | yes | `array<object> (Traffic matching list)` |
