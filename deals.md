# Deals

## Fields

| Name | Type | Description |
|------|------|-------------|
| certificate_valid_for_days | integer | Number of days for which the certificate is valid after the date of purchase |
| original_price | decimal | Pre-discount price |
| offer_price | decimal | Post-discount price |
| buck_rebate | decimal | Amount of gift bucks earned for purchasing the deal |
| max_quantity | integer | Maximum deals available for purchase |
| total_quantity_sold | integer | How many total deals have been sold |
| max_quantity_per_customer | integer | Maximum deals purchasable per customer |
| max_gift_quantity_per_customer | integer | Maximum deals available for gifting per customer |
| split | integer | Factor by which to split the deal into cheaper deals |
| slug | string | Partial URL for the deal |
| title | string | Primary title for the deal |
| use_now | boolean | Whether the deal can be used immediately |
| no_affiliate | boolean | ? |
| is_national_deal | boolean | Whether the deal runs at a national (not local) level |
| requires_shipping_information | boolean | Whether the deal requires shipping information to purchase |
| is_discoverable | boolean | Whether the deal is displayed in categories and search results. |
| show_remaining_quantity | boolean | Whether the deal displays the number of deals remaining that are available for purchase |
| hide_from_site | boolean | Whether the deal is hidden from the site |
| start_date | date | The date at which the deal is first available for purchase |
| affiliate_start_date | date | ? |
| end_date | date | The date at which the deal is no longer available for purchase |
| close_date | date | The date at which the deal no longer appears on the site |
| certificate_expiration_date | date | The date at which the deal may no longer be redeemed |
| deal_title | string | ? |
| cert_title | string | ? |
| highlights | string | ? |
| highlights_title | string | ? |
| certificate_details | string | ? |
| certificate_fine_print | string | Legal information printed on the certificate |
| details | string | ? |
| deal_instructions | string | ? |
| use_merchant_cert_codes | boolean | ? |

## List Deals

```http
GET /deals HTTP/1.1
Accept: application/vnd.api+json
```

## Retrieve a Deal by ID

```http
GET /deals/:deal_id HTTP/1.1
Accept: application/vnd.api+json
```
