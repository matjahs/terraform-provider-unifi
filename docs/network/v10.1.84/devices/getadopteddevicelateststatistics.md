---
title: "UniFi API"
source: https://developer.ui.com/network/v10.1.84/getadopteddevicelateststatistics
date: 2026-03-08T18:44:41.323013+00:00
---

# Get Latest Adopted Device Statistics

```http
GET /v1/sites/{siteId}/devices/{deviceId}/statistics/latest
```

Retrieve the latest real-time statistics of a specific adopted device, such as uptime, data transmission rates, CPU and memory utilization.

### Path Parameters

| Name | Required | Type |
| --- | --- | --- |
| `siteId` | yes | `string` |
| `deviceId` | yes | `string` |

## Responses

### 200

Response schema: `application/json`

| Field | Required | Type |
| --- | --- | --- |
| `uptimeSec` | no | `integer` |
| `lastHeartbeatAt` | no | `string` |
| `nextHeartbeatAt` | no | `string` |
| `loadAverage1Min` | no | `number` |
| `loadAverage5Min` | no | `number` |
| `loadAverage15Min` | no | `number` |
| `cpuUtilizationPct` | no | `number` |
| `memoryUtilizationPct` | no | `number` |
| `uplinkExpand` | no | `object` |
| `interfacesExpand` | yes | `object` |
