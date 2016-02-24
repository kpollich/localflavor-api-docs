# Cart Items

## Fields

| Name | Type | Description |
|------|------|-------------|
| quantity | number | The quantity of the item in the cart. |
| unit_price | number | The price for one unit of the item. |
| is_gift| boolean | Whether the item is a gift for someone else. |
| gift_recipient | string | The name of the recipient if this item is a gift. |
| send_to_phone | boolean | Whether the certificate for this item will be sent to the user's phone upon purchase. |
| opt_in | boolean | Whether the user has opted in to receive notifications about future deals from the business. |

## Related Items

* Cart
* Deal
* Coupon
* Merchandise Deal
* Business Location
* Shipping Address

## Get a User's Cart

```http
GET /cart HTTP/1.1
Accept: application/vnd.api+json
```
