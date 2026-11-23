---
title: "UniFi API"
source: https://developer.ui.com/network/v10.1.84/getwansoverviewpage
date: 2026-03-08T18:45:41.484403+00:00
---

# List WAN Interfaces

```http
GET /v1/sites/{siteId}/wans
```

Returns available WAN interface definitions for a given site,
including identifiers and names. Useful for network and NAT configuration.

### Path Parameters

| Name | Required | Type |
| --- | --- | --- |
| `siteId` | yes | `string` |

### Query Parameters

| Name | Required | Type |
| --- | --- | --- |
| `offset` | no | `integer` |
| `limit` | no | `integer` |

## Responses

### 200

Response schema: `application/json`

| Field | Required | Type |
| --- | --- | --- |
| `offset` | yes | `integer` |
| `limit` | yes | `integer` |
| `count` | yes | `integer` |
| `totalCount` | yes | `integer` |
| `dataExpand` | yes | `array<object> (WAN overview)` |
