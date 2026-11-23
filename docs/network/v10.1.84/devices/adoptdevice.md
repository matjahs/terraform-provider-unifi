---
title: "UniFi API"
source: https://developer.ui.com/network/v10.1.84/adoptdevice
date: 2026-03-08T18:44:33.980866+00:00
---

# Adopt Devices

```http
POST /v1/sites/{siteId}/devices
```

Adopt a device to a site.

### Path Parameters

| Name | Required | Type |
| --- | --- | --- |
| `siteId` | yes | `string` |

### Request Body

| Field | Required | Type |
| --- | --- | --- |
| `macAddress` | yes | `string` |
| `ignoreDeviceLimit` | yes | `boolean` |

## Responses

### 200

Response schema: `application/json`

| Field | Required | Type |
| --- | --- | --- |
| `id` | yes | `string` |
| `macAddress` | yes | `string` |
| `ipAddress` | yes | `string` |
| `name` | yes | `string` |
| `model` | yes | `string` |
| `supported` | yes | `boolean` |
| `state` | yes | `string` |
| `firmwareVersion` | no | `string` |
| `firmwareUpdatable` | yes | `boolean` |
| `adoptedAt` | no | `string` |
| `provisionedAt` | no | `string` |
| `configurationId` | yes | `string` |
| `uplinkExpand` | no | `object` |
| `featuresExpand` | yes | `object` |
| `interfacesExpand` | yes | `object` |

Notes:

- Uplink interface is device's connection to the parent device in the network topology
