# Devices

## Fields

| Name | Type | Description |
|------|------|-------------|
| uuid | string | Unique identifier for the device. |
| device_notification_identifier | string | ? |
| os_version | string | The version of the OS currently installed on the device. |
| platform_id | string | The OS platform installed on the device. |
| app_version | string | ? |
| num_failed_sends | number | ? |
| enable_push_notification | boolean | Whether push notifications are enabled for the device. |

## Related Items

* User

## List Devices

```http
GET /devices HTTP/1.1
Accept: application/vnd.api+json
```

## Add a Device

```http
POST /devices HTTP/1.1
Content-Type: application/vnd.api+json
Accept: application/vnd.api+json
```
