

# Charge Patient


## Create Charge

```shell
curl -i -H "Content-Type: application/json" -H "X-Auth-Token:patientuser@cooldoctors.io:patient:1515429239598:a0e476b75ffbacedd65e555b5304b222" "http://api.endpoint.eyecarelive.com/PaymentModule/api/charge/create" -X POST -d '{ "amount": "400","currency": "usd","token":"tok_16ZLt12eZvKYlo2CBJiPnmEV"}'
```
> The above command returns JSON structured like this:

```json
{
  "success": "true"
}
```
### HTTP Request

`POST http://api.endpoint.eyecarelive.com/PaymentModule/api/charge/create
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
Amount | Amount | String | Required
Currency | Currency | String | Required
Source | Source | String | Required

### Response

Parameter |  Description | Type 
--------- | ------------ | ---- 
ID | ID | Integer 
Object | Object | String
Created | Created | String
Live mode | Live mode | String
Paid | Paid | String
Status | Status | String
Amount | Amount | String
Currency | Currency | String
Refunded | Refunded | String
 | Source | 
ID | ID | Integer 
Object | Object | String
Last4 | Last 4 | String
Brand | Brand | String
Funding | Funding | String
Exp Month | Exp Month | Integer
Exp Year| Exp Year | Integer
Finger print | Finger print | String
Country | Country | String
Name | Name | String
Address Line1 | Address Line1 | String
Address Line2 | Address Line2 | String
Address City | Address City | String
Address State | Address State | String
Address Zip | Address Zip | String
Address Country | Address Country | String
CVC Check | CVC Check | String
Address Line1 Check | Address Line Check | String
Address Zip Check | Address Zip Check | String
Dynamic_last4 | Dynamic last | String
Customer | Customer | String
Captured | Captured | String
Balance_transaction | Balance transaction | String
Failure_message | Failure message | String
Failure_code | Failure code | String
Amount_refunded | Amount refunded | String
Customer | Customer | String
Invoice | Invoice | String
Description | Description | String
Dispute | Dispute | String
Metadata | Metadata | String
Statement_descriptor | Statement descriptor | String
Fraud_details | Fraud details | String
Receipt_email | Receipt email | String
Receipt_number | Receipt number | String
Shipping | Shipping | String
Refunds:[{}] | Refunds | String

<aside class="notice">
 Correct Email and Password leads to successful login!
</aside>


