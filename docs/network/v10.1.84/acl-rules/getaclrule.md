---
title: "UniFi API"
source: https://developer.ui.com/network/v10.1.84/getaclrule
date: 2026-03-08T18:45:17.211227+00:00
---

# Get ACL Rule

```http
GET /v1/sites/{siteId}/acl-rules/{aclRuleId}
```
### Path Parameters

| Name | Required | Type |
| --- | --- | --- |
| `aclRuleId` | yes | `string` |
| `siteId` | yes | `string` |

## Responses

### 200

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
