---
title: "UniFi API"
source: https://developer.ui.com/network/v10.1.84/getvpnserverpage
date: 2026-03-08T18:45:44.520198+00:00
---

# List VPN Servers

```http
GET /v1/sites/{siteId}/vpn/servers
```

Retrieve a paginated list of all VPN servers on a site.

### Filterable Properties

| Name | Type | Allowed functions |
| --- | --- | --- |
| `type` | `string` | `eq`, `ne`, `in`, `notIn` |
| `id` | `uuid` | `eq`, `ne`, `in`, `notIn` |
| `name` | `string` | `eq`, `ne`, `in`, `notIn`, `like` |
| `enabled` | `boolean` | `eq`, `ne` |
| `metadata.origin` | `string` | `eq`, `ne`, `in`, `notIn` |

### Path Parameters
### Query Parameters
## Responses

### 200

Response schema: `application/json`
