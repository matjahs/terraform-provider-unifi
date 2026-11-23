---
title: "UniFi API"
source: https://developer.ui.com/network/v10.1.84/updatetrafficmatchinglist
date: 2026-03-08T18:45:36.971329+00:00
---

# Update Traffic Matching List

```http
PUT /v1/sites/{siteId}/traffic-matching-lists/{trafficMatchingListId}
```

Update an exist traffic matching list on a site.

### Path Parameters

| Name | Required | Type |
| --- | --- | --- |
| `trafficMatchingListId` | yes | `string` |
| `siteId` | yes | `string` |

### Request Body

| Field | Required | Type |
| --- | --- | --- |
| `type` | yes | `string` |
| `name` | yes | `string` |
| `itemsExpand` | no | `array<object> (Port matching)` |

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
