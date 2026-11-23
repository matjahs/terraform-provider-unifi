---
title: "UniFi API"
source: https://developer.ui.com/network/v10.1.84/getwifibroadcastpage
date: 2026-03-08T18:44:57.452101+00:00
---

# List WiFi Broadcasts

```http
GET /v1/sites/{siteId}/wifi/broadcasts
```

Retrieve a paginated list of all WiFi Broadcasts on a site.

### Filterable Properties

| Name | Type | Allowed functions |
| --- | --- | --- |
| `type` | `string` | `eq`, `ne`, `in`, `notIn` |
| `id` | `uuid` | `eq`, `ne`, `in`, `notIn` |
| `enabled` | `boolean` | `eq`, `ne` |
| `name` | `string` | `eq`, `ne`, `in`, `notIn`, `like` |
| `broadcastingFrequenciesGHz` | `set(DECIMAL)` | `contains`, `containsAny`, `containsAll`, `containsExactly` |
| `metadata.origin` | `string` | `eq`, `ne`, `in`, `notIn` |
| `network.type` | `string` | `eq`, `ne`, `in`, `notIn`, `isNull`, `isNotNull` |
| `network.networkId` | `uuid` | `eq`, `ne`, `in`, `notIn` |
| `securityConfiguration.type` | `string` | `eq`, `ne`, `in`, `notIn` |
| `broadcastingDeviceFilter.type` | `string` | `eq`, `ne`, `in`, `notIn`, `isNull`, `isNotNull` |
| `broadcastingDeviceFilter.deviceIds` | `set(UUID)` | `contains`, `containsAny`, `containsAll`, `containsExactly` |
| `broadcastingDeviceFilter.deviceTagIds` | `set(UUID)` | `contains`, `containsAny`, `containsAll`, `containsExactly` |
| `hotspotConfiguration.type` | `string` | `eq`, `ne`, `in`, `notIn` |

### Path Parameters

| Name | Required | Type |
| --- | --- | --- |
| `siteId` | yes | `string` |

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
| `dataExpand` | yes | `array<object> (WiFi broadcast overview)` |
