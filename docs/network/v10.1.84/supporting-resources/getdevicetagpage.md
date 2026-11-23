---
title: "UniFi API"
source: https://developer.ui.com/network/v10.1.84/getdevicetagpage
date: 2026-03-08T18:45:47.475517+00:00
---

# List Device Tags

```http
GET /v1/sites/{siteId}/device-tags
```

Returns all device tags defined within a site, which can be used for WiFi Broadcast assignments.

### Filterable Properties

| Name | Type | Allowed functions |
| --- | --- | --- |
| `id` | `uuid` | `eq`, `ne`, `in`, `notIn` |
| `name` | `string` | `eq`, `ne`, `in`, `notIn`, `like` |
| `deviceIds` | `set(UUID)` | `contains`, `containsAny`, `containsAll`, `containsExactly` |

### Path Parameters
### Query Parameters
## Responses

### 200

Response schema: `application/json`
