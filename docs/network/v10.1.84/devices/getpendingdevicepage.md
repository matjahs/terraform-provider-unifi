---
title: "UniFi API"
source: https://developer.ui.com/network/v10.1.84/getpendingdevicepage
date: 2026-03-08T18:44:42.561915+00:00
---

# List Devices Pending Adoption

```http
GET /v1/pending-devices
```

Retrieve a paginated list of devices pending adoption, including basic device information.

### Filterable Properties

| Name | Type | Allowed functions |
| --- | --- | --- |
| `macAddress` | `string` | `eq`, `ne`, `in`, `notIn` |
| `ipAddress` | `string` | `eq`, `ne`, `in`, `notIn` |
| `model` | `string` | `eq`, `ne`, `in`, `notIn` |
| `state` | `string` | `eq`, `ne`, `in`, `notIn` |
| `supported` | `boolean` | `eq`, `ne` |
| `firmwareVersion` | `string` | `isNull`, `isNotNull`, `eq`, `ne`, `gt`, `ge`, `lt`, `le`, `like`, `in`, `notIn` |
| `firmwareUpdatable` | `boolean` | `eq`, `ne` |
| `features` | `set(STRING)` | `isEmpty`, `contains`, `containsAny`, `containsAll`, `containsExactly` |

### Query Parameters
## Responses

### 200

Response schema: `application/json`
