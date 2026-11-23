---
title: "UniFi API"
source: https://developer.ui.com/network/v10.1.84/getdpiapplicationcategories
date: 2026-03-08T18:45:49.077399+00:00
---

# List DPI Application Categories

```http
GET /v1/dpi/categories
```

Returns predefined Deep Packet Inspection (DPI) application categories used for traffic identification and filtering.

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
| `dataExpand` | yes | `array<object> (DPI category)` |
