# Promotion Codes

## Fields

| Name | Type | Description |
|------|------|-------------|
| promotion_code | string | The promotion code. |
| promotion_code_type_id | number | The type of promotion. |
| discount_amount | number | The USD value of the discount. |
| description | string | A description of the promotion. |
| start_date | date | The date the promotion code becomes valid. |
| end_date | date | The date the promotion code becomes invalid. |
| max_per_customer | number | The maximum number of times a customer may use this promotion code. |
| email_required | boolean | ? |
| allow_mobile | boolean | Whether the promotion code is allowed to be used on mobile devices. |
| allow_web | boolean | Whether the promotion code is allowed to be used on localflavor.com. |

## Get a Promotion Code

```http
GET /promotion_codes/:promotion_code HTTP/1.1
Accept: application/vnd.api+json
```

### Example

Determine if "flair" is a valid promotion code and get the details if it is.

```http
GET /promotion_codes/flair HTTP/1.1
Accept: application/vnd.api+json
```
