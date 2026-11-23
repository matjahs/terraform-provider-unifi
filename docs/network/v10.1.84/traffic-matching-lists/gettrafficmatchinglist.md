---
title: "UniFi API"
source: https://developer.ui.com/network/v10.1.84/gettrafficmatchinglist
date: 2026-03-08T18:45:35.159179+00:00
---

# Get Traffic Matching List

```http
GET /v1/sites/{siteId}/traffic-matching-lists/{trafficMatchingListId}
```

Get an exist traffic matching list on a site.

### Path Parameters

| Name | Required | Type |
| --- | --- | --- |
| `trafficMatchingListId` | yes | `string` |
| `siteId` | yes | `string` |

## Responses

### 200

Response schema: `application/json`

| Field | Required | Type |
| --- | --- | --- |
| `type` | yes | `string` |
| `id` | yes | `string` |
| `name` | yes | `string` |
| `itemsExpand` | no | `array<object> (Port matching)` |

Notes:

- Allowed value: `PORTSIPV4\_ADDRESSESIPV6\_ADDRESSES`
