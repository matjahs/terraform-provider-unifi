---
title: "UniFi API"
source: https://developer.ui.com/network/v10.1.84/updatenetwork
date: 2026-03-08T18:44:47.730721+00:00
---

# Update Network

```http
PUT /v1/sites/{siteId}/networks/{networkId}
```

Update an existing network on a site.

### Path Parameters

| Name | Required | Type |
| --- | --- | --- |
| `networkId` | yes | `string` |
| `siteId` | yes | `string` |

### Request Body

| Field | Required | Type |
| --- | --- | --- |
| `management` | yes | `string` |
| `UNMANAGEDGATEWAYSWITCH` | no | - |
| `name` | yes | `string` |
| `enabled` | yes | `boolean` |
| `vlanId` | yes | `integer` |
| `dhcpGuardingExpand` | no | `object` |

## Responses

### 200

Response schema: `application/json`

| Field | Required | Type |
| --- | --- | --- |
| `management` | yes | `string` |
| `id` | yes | `string` |
| `name` | yes | `string` |
| `enabled` | yes | `boolean` |
| `vlanId` | yes | `integer` |
| `metadataExpand` | yes | `object (User or system defined or orchestrated entity metadata)` |
| `dhcpGuardingExpand` | no | `object` |
| `default` | yes | `boolean` |

Notes:

- UNMANAGEDGATEWAYSWITCH
- VLAN ID. Must be 1 for the default network and >= 2 for additional networks.
- Orchestrated or System-defined configurable network support
- DHCP Guarding settings for this Network. If this field is omitted or null, the feature is disabled
