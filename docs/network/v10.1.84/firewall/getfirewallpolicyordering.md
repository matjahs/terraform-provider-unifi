---
title: "UniFi API"
source: https://developer.ui.com/network/v10.1.84/getfirewallpolicyordering
date: 2026-03-08T18:45:09.531661+00:00
---

# Get User-Defined Firewall Policy Ordering

```http
GET /v1/sites/{siteId}/firewall/policies/ordering
```

Retrieve user-defined firewall policy ordering for a specific source/destination zone pair.

### Path Parameters

| Name | Required | Type |
| --- | --- | --- |
| `siteId` | yes | `string` |

### Query Parameters

| Name | Required | Type |
| --- | --- | --- |
| `sourceFirewallZoneId` | yes | `string` |
| `destinationFirewallZoneId` | yes | `string` |

## Responses

### 200

Response schema: `application/json`

| Field | Required | Type |
| --- | --- | --- |
| `orderedFirewallPolicyIdsExpand` | yes | `object` |
