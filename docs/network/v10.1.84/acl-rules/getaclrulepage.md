---
title: "UniFi API"
source: https://developer.ui.com/network/v10.1.84/getaclrulepage
date: 2026-03-08T18:45:24.819525+00:00
---

# List ACL Rules

```http
GET /v1/sites/{siteId}/acl-rules
```

Retrieve a paginated list of all ACL rules on a site.

### Filterable Properties

| Name | Type | Allowed functions |
| --- | --- | --- |
| `type` | `string` | `eq`, `ne`, `in`, `notIn` |
| `id` | `uuid` | `eq`, `ne`, `in`, `notIn` |
| `enabled` | `boolean` | `eq`, `ne` |
| `name` | `string` | `eq`, `ne`, `in`, `notIn`, `like` |
| `description` | `string` | `isNull`, `isNotNull`, `eq`, `ne`, `in`, `notIn`, `like` |
| `action` | `string` | `eq`, `ne`, `in`, `notIn` |
| `index` | `integer` | `eq`, `ne`, `gt`, `ge`, `lt`, `le`, `in`, `notIn` |
| `protocolFilter` | `set(STRING)` | `isNull`, `isNotNull`, `contains`, `containsAny`, `containsAll`, `containsExactly` |
| `networkId` | `uuid` | `isNull`, `isNotNull`, `eq`, `ne`, `in`, `notIn` |
| `enforcingDeviceFilter.deviceIds` | `set(UUID)` | `isNull`, `isNotNull`, `contains`, `containsAny`, `containsAll`, `containsExactly` |
| `metadata.origin` | `string` | `eq`, `ne`, `in`, `notIn` |
| `sourceFilter.type` | `string` | `isNull`, `isNotNull`, `eq`, `ne`, `in`, `notIn` |
| `sourceFilter.ipAddressesOrSubnets` | `set(STRING)` | `contains`, `containsAny`, `containsAll`, `containsExactly` |
| `sourceFilter.portFilter` | `set(INTEGER)` | `isNull`, `isNotNull`, `contains`, `containsAny`, `containsAll`, `containsExactly` |
| `sourceFilter.networkIds` | `set(UUID)` | `contains`, `containsAny`, `containsAll`, `containsExactly` |
| `sourceFilter.macAddresses` | `set(STRING)` | `contains`, `containsAny`, `containsAll`, `containsExactly` |
| `sourceFilter.prefixLength` | `integer` | `isNull`, `isNotNull`, `eq`, `ne`, `gt`, `ge`, `lt`, `le`, `in`, `notIn` |
| `destinationFilter.type` | `string` | `isNull`, `isNotNull`, `eq`, `ne`, `in`, `notIn` |
| `destinationFilter.ipAddressesOrSubnets` | `set(STRING)` | `contains`, `containsAny`, `containsAll`, `containsExactly` |
| `destinationFilter.portFilter` | `set(INTEGER)` | `isNull`, `isNotNull`, `contains`, `containsAny`, `containsAll`, `containsExactly` |
| `destinationFilter.networkIds` | `set(UUID)` | `contains`, `containsAny`, `containsAll`, `containsExactly` |
| `destinationFilter.macAddresses` | `set(STRING)` | `contains`, `containsAny`, `containsAll`, `containsExactly` |
| `destinationFilter.prefixLength` | `integer` | `isNull`, `isNotNull`, `eq`, `ne`, `gt`, `ge`, `lt`, `le`, `in`, `notIn` |

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
| `dataExpand` | yes | `array<object> (ACL ruleObject)` |
