---
title: "UniFi API"
source: https://developer.ui.com/network/v10.1.84/getadopteddeviceoverviewpage
date: 2026-03-08T18:44:32.370286+00:00
---

# List Adopted Devices

```http
GET /v1/sites/{siteId}/devices
```

Retrieve a paginated list of all adopted devices on a site, including basic device information.

### Filterable Properties

| Name | Type | Allowed functions |
| --- | --- | --- |
| `id` | `uuid` | `eq`, `ne`, `in`, `notIn` |
| `macAddress` | `string` | `eq`, `ne`, `in`, `notIn` |
| `ipAddress` | `string` | `eq`, `ne`, `in`, `notIn` |
| `name` | `string` | `eq`, `ne`, `in`, `notIn`, `like` |
| `model` | `string` | `eq`, `ne`, `in`, `notIn` |
| `state` | `string` | `eq`, `ne`, `in`, `notIn` |
| `supported` | `boolean` | `eq`, `ne` |
| `firmwareVersion` | `string` | `isNull`, `isNotNull`, `eq`, `ne`, `gt`, `ge`, `lt`, `le`, `like`, `in`, `notIn` |
| `firmwareUpdatable` | `boolean` | `eq`, `ne` |
| `features` | `set(STRING)` | `isEmpty`, `contains`, `containsAny`, `containsAll`, `containsExactly` |
| `interfaces` | `set(STRING)` | `isEmpty`, `contains`, `containsAny`, `containsAll`, `containsExactly` |

### Path Parameters
### Query Parameters
## Responses

### 200

Response schema: `application/json`
