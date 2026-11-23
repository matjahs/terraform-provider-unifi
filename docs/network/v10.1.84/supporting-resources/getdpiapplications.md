---
title: "UniFi API"
source: https://developer.ui.com/network/v10.1.84/getdpiapplications
date: 2026-03-08T18:45:50.870097+00:00
---

# List DPI Applications

```http
GET /v1/dpi/applications
```

Lists DPI-recognized applications grouped under categories. Useful for firewall or traffic analytics integration.

### Filterable Properties

| Name | Type | Allowed functions |
| --- | --- | --- |
| `id` | `integer` | `eq`, `ne`, `in`, `notIn` |
| `name` | `string` | `eq`, `ne`, `in`, `notIn`, `like` |

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
| `dataExpand` | yes | `array<object> (DPI application)` |
