# Cart Items

## Fields

| Name | Type | Description |
|------|------|-------------|
| quantity | number | **Required**. The quantity of the item in the cart. |
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

## Get a User's Cart Items

```http
GET /cart_items HTTP/1.1
Accept: application/vnd.api+json
```

## Add an Item to a User's Cart

```http
POST /cart_items
Content-Type: application/vnd.api+json
Accept: application/vnd.api+json
```

### Example

```http
POST /cart_items
Content-Type: application/vnd.api+json
Accept: application/vnd.api+json

{
	"data": {
		"type": "cart_items",
		"attributes": {
			"quantity": 1
		},
		"relationships": {
			"deal": {
				"data": { "type": "deals", "id": "20" }
		}
	}
}
```

## Update an Item in a User's Cart

```http
PATCH /cart_items/:cart_item_id
Content-Type: application/vnd.api+json
Accept: application/vnd.api+json
```

### Example

```http
PATCH /cart_items/25
Content-Type: application/vnd.api+json
Accept: application/vnd.api+json

{
	"data": {
		"type": "cart_items",
		"id": "25",
		"attributes": {
			"quantity": 2
		}
	}
}
```

## Remove an Item from the User's Cart

```http
DELETE /cart_items/:cart_item_id
Accept: application/vnd.api+json
```
