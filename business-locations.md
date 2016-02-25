# Business Locations

## Fields

| Name | Type | Descriptions |
|------|------|--------------|
| latitude | decimal | The location's latitude in degrees |
| longitude | decimal | The location's longitude in degrees |
| slug | string | The URL partial for the location |
| address | string | Street address for the location |
| address2 | string | Additional address field for the location |
| city | string | City field for the location's address |
| state | string | State field for the location's address |
| zip | string | Zip Code for the location's address |
| phone | string | Phone number for the location |
| hide_location | boolean | Whether the location is displayed |  
| hide_location_text | string | Text to display in place of the location when hidden |

## Related Items

* Deals
* Coupons
* Image

## List Business Locations

```http
GET /business-locations HTTP/1.1
Accept: application/vnd.api+json
```

## Retrieve a Business Location by ID

```http
GET /business-locations/:business_location_id HTTP/1.1
Accept: applicaton/vnd.api+json
```

