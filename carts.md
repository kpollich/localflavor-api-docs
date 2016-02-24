# Carts

Each user always has exactly one active cart. Carts can not be created or deleted through the API; a new cart is automatically created when the current cart is purchased.

## Fields

| Name | Type | Description |
|------|------|-------------|
| purchase_date | date | The date the order was purchased. |

## Related Items

* Cart Items
* User

## Get a User's Cart

```http
GET /cart HTTP/1.1
Accept: application/vnd.api+json
```

## Update a User's Cart

Because carts don't contain any attributes that can be directly manipulated, editing a cart directly is limited to removing cart items via the cart's `relationships`. Most cart updates will instead occur through operations on the cart items.

Assuming the user's cart currently contains cart items 201, 202, and 203, the following request would remove cart item 202 from the cart:

```http
PATCH /cart
Content-Type: application/vnd.api+json
Accept: application/vnd.api+json

{
	"data": {
		"type": "carts",
		"id": "25",
		"relationships": {
			"cart_items": {
				"data": [
					{ "type": "cart_items", "id": "201" },
					{ "type": "cart_items", "id": "203" },
				]
			}
		}
	}
}
```
