---
title: "UniFi API"
source: https://developer.ui.com/network/v10.1.84/getsitetositevpntunnelpage
date: 2026-03-08T18:45:43.055630+00:00
---

# List Site-To-Site VPN Tunnels

```http
GET /v1/sites/{siteId}/vpn/site-to-site-tunnels
```

Retrieve a paginated list of all site-to-site VPN tunnels on a site.

### Filterable Properties

| Name | Type | Allowed functions |
| --- | --- | --- |
| `type` | `string` | `eq`, `ne`, `in`, `notIn` |
| `id` | `uuid` | `eq`, `ne`, `in`, `notIn` |
| `name` | `string` | `eq`, `ne`, `in`, `notIn`, `like` |
| `metadata.origin` | `string` | `eq`, `ne`, `in`, `notIn` |
| `metadata.source` | `string` | `eq`, `ne`, `in`, `notIn`, `isNull`, `isNotNull` |

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
| `dataExpand` | yes | `array<object> (Site-to-site VPN tunnel overview)` |
