---
title: "UniFi API"
source: https://developer.ui.com/network/v10.1.84/updatewifibroadcast
date: 2026-03-08T18:44:55.916655+00:00
---

# Update WiFi Broadcast

```http
PUT /v1/sites/{siteId}/wifi/broadcasts/{wifiBroadcastId}
```

Update an existing WiFi Broadcast on the specified site.

### Path Parameters

| Name | Required | Type |
| --- | --- | --- |
| `wifiBroadcastId` | yes | `string` |
| `siteId` | yes | `string` |

### Request Body

| Field | Required | Type |
| --- | --- | --- |
| `type` | yes | `string` |
| `name` | yes | `string` |
| `networkExpand` | no | `object (WiFi network reference)` |
| `enabled` | yes | `boolean` |
| `securityConfigurationExpand` | yes | `object` |
| `broadcastingDeviceFilterExpand` | no | `object (Broadcasting device filter)` |
| `mdnsProxyConfigurationExpand` | no | `object (mDNS filtering configuration)` |
| `multicastFilteringPolicyExpand` | no | `object (Multicast filtering policy)` |
| `multicastToUnicastConversionEnabled` | yes | `boolean` |
| `clientIsolationEnabled` | yes | `boolean` |
| `hideName` | yes | `boolean` |
| `uapsdEnabled` | yes | `boolean` |
| `basicDataRateKbpsByFrequencyGHzExpand` | no | `object` |
| `clientFilteringPolicyExpand` | no | `object` |
| `blackoutScheduleConfigurationExpand` | no | `object` |
| `broadcastingFrequenciesGHzExpand` | no | `array<number>` |
| `hotspotConfigurationExpand` | no | `object (WiFi hotspot configuration)` |
| `mloEnabled` | no | `boolean` |
| `bandSteeringEnabled` | no | `boolean` |
| `arpProxyEnabled` | no | `boolean` |
| `bssTransitionEnabled` | no | `boolean` |
| `advertiseDeviceName` | no | `boolean` |
| `dtimPeriodByFrequencyGHzOverrideExpand` | no | `object` |

## Responses

### 200

Response schema: `application/json`

| Field | Required | Type |
| --- | --- | --- |
| `type` | yes | `string` |
| `id` | yes | `string` |
| `name` | yes | `string` |
| `metadataExpand` | yes | `object (User or derived or orchestrated entity metadata)` |
| `enabled` | yes | `boolean` |
| `networkExpand` | no | `object (WiFi network reference)` |
| `securityConfigurationExpand` | yes | `object` |
| `broadcastingDeviceFilterExpand` | no | `object (Broadcasting device filter)` |
| `mdnsProxyConfigurationExpand` | no | `object (mDNS filtering configuration)` |
| `multicastFilteringPolicyExpand` | no | `object (Multicast filtering policy)` |
| `multicastToUnicastConversionEnabled` | yes | `boolean` |
| `clientIsolationEnabled` | yes | `boolean` |
| `hideName` | yes | `boolean` |
| `uapsdEnabled` | yes | `boolean` |
| `basicDataRateKbpsByFrequencyGHzExpand` | no | `object` |
| `clientFilteringPolicyExpand` | no | `object` |
| `blackoutScheduleConfigurationExpand` | no | `object` |
| `broadcastingFrequenciesGHzExpand` | no | `array<number>` |
| `hotspotConfigurationExpand` | no | `object (WiFi hotspot configuration)` |
| `mloEnabled` | no | `boolean` |
| `bandSteeringEnabled` | no | `boolean` |
| `arpProxyEnabled` | no | `boolean` |
| `bssTransitionEnabled` | no | `boolean` |
| `advertiseDeviceName` | no | `boolean` |
| `dtimPeriodByFrequencyGHzOverrideExpand` | no | `object` |

Notes:

- Allowed value: `STANDARDIOT\_OPTIMIZED`
- Defines the custom scope of devices that will broadcast this WiFi network. If null, the WiFi network will be broadcast by all Access Point capable devices.
- Indicates whether Unscheduled Automatic Power Save Delivery (U-APSD) is enabled
- Client connection filtering policy. Allow/restrict access to the WiFi network based on client device MAC addresses.
- Indicates whether the device name is advertised in beacon frames.
