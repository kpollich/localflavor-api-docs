# Businesses

## Fields

| Name | Type | Description |
|------|------|-------------|
| name | string | Name of the business |
| slug | string | Formerly "SEOUrl" - the url partial for the business |
| is_vanity | boolean | Whether this business is only a customer for TLS custom apps |
| esp | integer | Billing account ID number for the business |
| hours | string | Daily hours for the business |
| website | string | The external website for the business |
| description | string | Paragraph of details/information about the business |
| email | string | Contact email for the business |
| view_count | integer | Number of times users have viewed the business |
| display_multiple_locations | boolean | Whether to show all locations for the business |

## Related Items

* Business Locations
* Merchandise Deals (?)

## List Businesses

```http
GET /businesses HTTP/1.1
Accept: application/vnd.api+json
```

### Filters

Note: Consult [JSON API's documentation](http://jsonapi.org/format/#fetching-filtering) for more information about filtering

| Filter | Description | 
|--------|-------------|
| latitude | Decimal value for the latitude of the point around which to search for businesses |
| longitude | Decimal value for the longitude of the point around which to search for businesses |

### Example

You can use the latitude and longitude filters to retrieve a list of businesses around a center point.

```http
GET /businesses?filters[latitude]=-40.054&filters[longitude]=76.531 HTTP/1.1
Accept: application/vnd.api+json
```

This call will return businesses within a given radius (TODO: determine radius) around the provided latitude and longitude. The latitude and longitude filters are ONLY supported in conjuction, and providing one without the other will result in that filter being ignored.

## Retrieve a Business by ID

```http
GET /businesses/:business_id HTTP/1.1
Accept: application/vnd.api+json
```
