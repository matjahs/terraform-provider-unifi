---
title: "UniFi API"
source: https://developer.ui.com/network/v10.1.84/getfirewallzones
date: 2026-03-08T18:45:12.562554+00:00
---

# List Firewall Zones

```http
GET /v1/sites/{siteId}/firewall/zones
```

Retrieve a list of all firewall zones on a site.

### Filterable Properties

| Name | Type | Allowed functions |
| --- | --- | --- |
| `id` | `uuid` | `eq`, `ne`, `in`, `notIn` |
| `name` | `string` | `eq`, `ne`, `in`, `notIn`, `like` |
| `metadata.origin` | `string` | `eq`, `ne`, `in`, `notIn` |
| `metadata.configurable` | `boolean` | `eq`, `ne`, `isNull`, `isNotNull` |

### Path Parameters
### Query Parameters
## Responses

### 200

Response schema: `application/json`
