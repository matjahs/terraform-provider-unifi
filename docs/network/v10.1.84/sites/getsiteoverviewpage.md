---
title: "UniFi API"
source: https://developer.ui.com/network/v10.1.84/getsiteoverviewpage
date: 2026-03-08T18:44:30.819767+00:00
---

# List Local Sites

```http
GET /v1/sites
```

Retrieve a paginated list of local sites managed by this Network application.
Site ID is required for other UniFi Network API calls.

### Filterable Properties

| Name | Type | Allowed functions |
| --- | --- | --- |
| `id` | `uuid` | `eq`, `ne`, `in`, `notIn` |
| `internalReference` | `string` | `eq`, `ne`, `in`, `notIn` |
| `name` | `string` | `eq`, `ne`, `in`, `notIn` |

### Query Parameters
## Responses

### 200

Response schema: `application/json`
