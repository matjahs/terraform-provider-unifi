---
title: "UniFi API"
source: https://developer.ui.com/network/v10.1.84/getcountries
date: 2026-03-08T18:45:52.357309+00:00
---

# List Countries

```http
GET /v1/countries
```

Returns ISO-standard country codes and names,
used for region-based configuration or regulatory compliance.

### Filterable Properties

| Name | Type | Allowed functions |
| --- | --- | --- |
| `code` | `string` | `eq`, `ne`, `in`, `notIn` |
| `name` | `string` | `eq`, `ne`, `in`, `notIn`, `like` |

### Query Parameters
## Responses

### 200

Response schema: `application/json`
