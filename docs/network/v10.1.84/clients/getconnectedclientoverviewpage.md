---
title: "UniFi API"
source: https://developer.ui.com/network/v10.1.84/getconnectedclientoverviewpage
date: 2026-03-08T18:44:44.346726+00:00
---

# List Connected Clients

```http
GET /v1/sites/{siteId}/clients
```

Retrieve a paginated list of all connected clients on a site, including physical devices (computers, smartphones) and active VPN connections.

### Filterable Properties

| Name | Type | Allowed functions |
| --- | --- | --- |
| `id` | `uuid` | `eq`, `ne`, `in`, `notIn` |
| `type` | `string` | `eq`, `ne`, `in`, `notIn` |
| `macAddress` | `string` | `isNull`, `isNotNull`, `eq`, `ne`, `in`, `notIn` |
| `ipAddress` | `string` | `isNull`, `isNotNull`, `eq`, `ne`, `in`, `notIn` |
| `connectedAt` | `timestamp` | `isNull`, `isNotNull`, `eq`, `ne`, `gt`, `ge`, `lt`, `le` |
| `access.type` | `string` | `eq`, `ne`, `in`, `notIn` |
| `access.authorized` | `boolean` | `isNull`, `isNotNull`, `eq`, `ne` |

### Path Parameters
### Query Parameters
## Responses

### 200

Response schema: `application/json`
