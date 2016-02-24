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
