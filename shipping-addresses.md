# Shipping Addresses

## Fields

| Name | Type | Description |
|------|------|-------------|
| title | string | The title for the shipping address. |
| recipient_name | string | The name of the recipient. |
| address | string | The street portion for the billing address. |
| address2 | string | Additional street information for the billing address. |
| city | string | The city for the billing address. |
| state | string | The state for the billing address. |
| zip | string | The ZIP Code for the billing address. |
| phone | string | The phone number to call for delivery issues. |
| sms_carrier_id | string | ? |
| is_default | boolean | Whether this is the default shipping address for orders. |

## Related Items

* User

## List a User's Shipping Addresses

```http
GET /shipping_addresses HTTP/1.1
Accept: application/vnd.api+json
```

## Get a Shipping Address

```http
GET /shipping_addresses/:shipping_address_id HTTP/1.1
Accept: application/vnd.api+json
```

## Add a Shipping Address

```http
POST /shipping_addresses HTTP/1.1
Content-Type: application/vnd.api+json
Accept: application/vnd.api+json
```

## Update a Shipping Address

```http
PATCH /shipping_addresses/:shipping_address_id HTTP/1.1
Content-Type: application/vnd.api+json
Accept: application/vnd.api+json
```

## Delete a Shipipng Address

```http
DELETE /shipping_addresses/:shipping_address_id HTTP/1.1
Accept: application/vnd.api+json
```
