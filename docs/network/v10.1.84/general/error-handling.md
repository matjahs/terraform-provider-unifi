---
title: "UniFi API"
source: https://developer.ui.com/network/v10.1.84/error-handling
date: 2026-03-08T18:44:28.859657+00:00
---

Describes the standard API error response structure, including error codes,
status names, and troubleshooting guidance.

## Related Schemas

### Error Message

| Field | Type | Format | Description | Example |
| --- | --- | --- | --- | --- |
| `code` | `string` | - | - | `api.authentication.missing-credentials` |
| `message` | `string` | - | - | `Missing credentials` |
| `requestId` | `string` | uuid | In case of Internal Server Error (core = 500), request ID can be used to track down the error in the server log | `3fa85f64-5717-4562-b3fc-2c963f66afa6` |
| `requestPath` | `string` | - | - | `/integration/v1/sites/123` |
| `statusCode` | `integer` | int32 | - | `400` |
| `statusName` | `string` | - | - | `UNAUTHORIZED` |
| `timestamp` | `string` | date-time | - | `2024-11-27T08:13:46.966Z` |
