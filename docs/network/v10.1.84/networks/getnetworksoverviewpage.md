---
title: "UniFi API"
source: https://developer.ui.com/network/v10.1.84/getnetworksoverviewpage
date: 2026-03-08T18:44:51.536401+00:00
---

# List Networks

```http
GET /v1/sites/{siteId}/networks
```

Retrieve a paginated list of all Networks on a site.

### Filterable Properties

| Name | Type | Allowed functions |
| --- | --- | --- |
| `management` | `string` | `eq`, `ne`, `in`, `notIn` |
| `id` | `uuid` | `eq`, `ne`, `in`, `notIn` |
| `name` | `string` | `eq`, `ne`, `in`, `notIn`, `like` |
| `enabled` | `boolean` | `eq`, `ne` |
| `vlanId` | `integer` | `eq`, `ne`, `gt`, `ge`, `lt`, `le`, `in`, `notIn` |
| `deviceId` | `uuid` | `eq`, `ne`, `in`, `notIn`, `isNull`, `isNotNull` |
| `metadata.origin` | `string` | `eq`, `ne`, `in`, `notIn` |

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
| `dataExpand` | yes | `array<object> (Network overview)` |
