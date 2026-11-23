---
title: "UniFi API"
source: https://developer.ui.com/network/v10.1.84/createaclrule
date: 2026-03-08T18:45:26.503057+00:00
---

# Create ACL Rule

```http
POST /v1/sites/{siteId}/acl-rules
```

Create a new user defined ACL rule on a site.

### Path Parameters

| Name | Required | Type |
| --- | --- | --- |
| `siteId` | yes | `string` |

### Request Body

| Field | Required | Type |
| --- | --- | --- |
| `type` | yes | `string` |
| `IPV4MAC` | no | - |
| `enabled` | yes | `boolean` |
| `name` | yes | `string` |
| `description` | no | `string` |
| `action` | yes | `string` |
| `enforcingDeviceFilterExpand` | no | `object (ACL rule device filter)` |
| `index` | no | `integer` |
| `sourceFilterExpand` | no | `object (IP ACL rule endpoint)` |
| `destinationFilterExpand` | no | `object (IP ACL rule endpoint)` |
| `protocolFilterExpand` | no | `array<string>` |

## Responses

### 201

Response schema: `application/json`

| Field | Required | Type |
| --- | --- | --- |
| `type` | yes | `string` |
| `id` | yes | `string` |
| `enabled` | yes | `boolean` |
| `name` | yes | `string` |
| `description` | no | `string` |
| `action` | yes | `string` |
| `enforcingDeviceFilterExpand` | no | `object (ACL rule device filter)` |
| `index` | yes | `integer` |
| `sourceFilter` | no | - |
| `any` | no | - |
| `destinationFilter` | no | - |
| `any` | no | - |
| `metadataExpand` | yes | `object (User defined or derived entity metadata)` |
| `protocolFilterExpand` | no | `array<string>` |

Notes:

- IPV4MAC
- ACL rule name
- ACL rule description
- ACL rule action
- IDs of the Switch-capable devices used to enforce the ACL rule. When null, the rule will be provisioned to all switches on the site.
- ACL rule index. Lower index has higher priority
- Traffic source filter
- Traffic destination filter
- Only user-defined rules can be deleted or modified
- Protocols this ACL rule will be applied to. When null, the rule will be applied to all protocols.
