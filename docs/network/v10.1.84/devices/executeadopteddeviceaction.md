---
title: "UniFi API"
source: https://developer.ui.com/network/v10.1.84/executeadopteddeviceaction
date: 2026-03-08T18:44:36.817690+00:00
---

# Execute Adopted Device Action

```http
POST /v1/sites/{siteId}/devices/{deviceId}/actions
```

Perform an action on an specific adopted device. The request body must include the action name and any applicable input arguments.

### Path Parameters

| Name | Required | Type |
| --- | --- | --- |
| `siteId` | yes | `string` |
| `deviceId` | yes | `string` |

### Request Body

| Field | Required | Type |
| --- | --- | --- |
| `action` | yes | `string` |
| `RESTART` | no | - |

## Responses

### 200

- Response 200: No schema content available
