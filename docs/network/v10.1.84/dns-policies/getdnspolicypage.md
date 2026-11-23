---
title: "UniFi API"
source: https://developer.ui.com/network/v10.1.84/getdnspolicypage
date: 2026-03-08T18:45:32.254491+00:00
---

# List DNS Policies

```http
GET /v1/sites/{siteId}/dns/policies
```

Retrieve a paginated list of all DNS policies on a site.

### Filterable Properties

| Name | Type | Allowed functions |
| --- | --- | --- |
| `type` | `string` | `eq`, `ne`, `in`, `notIn` |
| `id` | `uuid` | `eq`, `ne`, `in`, `notIn` |
| `enabled` | `boolean` | `eq`, `ne` |
| `domain` | `string` | `eq`, `ne`, `in`, `notIn`, `like` |
| `ipv4Address` | `string` | `eq`, `ne`, `in`, `notIn`, `like` |
| `ipv6Address` | `string` | `eq`, `ne`, `in`, `notIn`, `like` |
| `targetDomain` | `string` | `eq`, `ne`, `in`, `notIn`, `like` |
| `mailServerDomain` | `string` | `eq`, `ne`, `in`, `notIn`, `like` |
| `text` | `string` | `eq`, `ne`, `in`, `notIn`, `like` |
| `serverDomain` | `string` | `eq`, `ne`, `in`, `notIn`, `like` |
| `ipAddress` | `string` | `eq`, `ne`, `in`, `notIn`, `like` |
| `ttlSeconds` | `integer` | `eq`, `ne`, `gt`, `ge`, `lt`, `le`, `in`, `notIn` |
| `priority` | `integer` | `eq`, `ne`, `gt`, `ge`, `lt`, `le`, `in`, `notIn` |
| `service` | `string` | `eq`, `ne`, `in`, `notIn` |
| `protocol` | `string` | `eq`, `ne`, `in`, `notIn` |
| `port` | `integer` | `eq`, `ne`, `gt`, `ge`, `lt`, `le`, `in`, `notIn` |
| `weight` | `integer` | `eq`, `ne`, `gt`, `ge`, `lt`, `le`, `in`, `notIn` |

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
| `dataExpand` | yes | `array<object> (DNS policy)` |
