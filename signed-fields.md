# Signed Fields

These are the properties required to POST a potential transaction to CyberSource for validation. These fields are derived primarily from the
## Fields

| Name | Type | Description |
|------|------|-------------|
| transaction_type | string | CyberSource methods being used |
| payment_method | string | How the transaction is being paid |
| update_payment_token | boolean | Indicates whether the customer can update the billing, shipping, and payment information on the order review page |
| currency | string | Type of currency being paid. USD, etc |
| locale | string | Language code |
| bill_to_email | string | Email address of the user associated with the transaction |
| access_key | string | Key for authenticating to CyberSource |
| profile_id | string | ID for authenticating to CyberSource |
| merchant_defined_data1 | string | Custom data for tracking, analytics - see [this confluence page](https://clipperdigital.atlassian.net/wiki/display/LF/Cyber+Source+Merchant+Defined+Data) for more info|
| merchant_defined_data2 | string | "" |
| merchant_defined_data3 | string | "" |
| merchant_defined_data4 | string | "" |
| bill_to_address_country | string | Country for the billing address on the user's card |
| unsigned_field_names | array | Array of all fields submitted that _are not_ signed with the CyberSource private key |
| signed_field_names | array | Array of all fields that _are_ signed with the private key |
| signature | string | Base64 string created from the set of signed fields and our CyberSource private key |
| transaction_uuid | guid | Unique identifier for this transaction |
| reference_number | string | CyberSource identifier for this transaction. |
| amount | decimal | Total for the cart being purchased |
| signed_date_time | datetime | Timestamp for when this set of signed fields was created |


## List signed fields

```http
GET /signed-fields HTTP/1.1
Accept: application/vnd.api+json
```
