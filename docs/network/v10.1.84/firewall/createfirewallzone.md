---
title: "UniFi API"
source: https://developer.ui.com/network/v10.1.84/createfirewallzone
date: 2026-03-08T18:45:14.145733+00:00
---

# Create Custom Firewall Zone

```http
POST /v1/sites/{siteId}/firewall/zones
```

Create a new custom firewall zone on a site.

### Path Parameters

| Name | Required | Type |
| --- | --- | --- |
| `siteId` | yes | `string` |

### Request Body

| Field | Required | Type |
| --- | --- | --- |
| `name` | yes | `string` |
| `networkIdsExpand` | yes | `array<string>` |

## Responses

### 201

Response schema: `application/json`

| Field | Required | Type |
| --- | --- | --- |
| `id` | yes | `string` |
| `name` | yes | `string` |
| `networkIdsExpand` | yes | `array<string>` |
| `metadataExpand` | yes | `object (User or system defined entity metadata)` |

Notes:

- Name of a firewall zone
- List of Network IDs
- System-defined configurable zones support configuring only attached networks
