


# Patient Payment Information


## Create Token 

```shell
curl -i -H "Content-Type: application/json" -H "X-Auth-Token:patientuser@cooldoctors.io:patient:1515429239598:a0e476b75ffbacedd65e555b5304b222" "http://api.endpoint.eyecarelive.com/PaymentModule/api/token/create" -X POST -d '{ "card":{"number":"4242424242424242","cvcCheck":"779","expMonth":"12","expYear":"2016","name":"nitesh"}}'


```
> The above command returns JSON structured like this:

```json
{
  "amount": null,
  "created": 1439470373,
  "currency": null,
  "id": "tok_16ZLCT2eZvKYlo2CV4n8Nfyb",
  "livemode": false,
  "used": false,
  "card": {
    "id": "card_16ZLCT2eZvKYlo2CgetDZAsy",
    "object": "card",
    "customer": null,
    "account": null,
    "status": null,
    "expMonth": 12,
    "expYear": 2016,
    "last4": "4242",
    "dynamicLast4": null,
    "country": "US",
    "type": null,
    "name": "nitesh",
    "recipient": null,
    "addressLine1": null,
    "addressLine2": null,
    "addressZip": null,
    "addressCity": null,
    "addressState": null,
    "addressCountry": null,
    "addressZipCheck": null,
    "addressLine1Check": null,
    "cvcCheck": "unchecked",
    "fingerprint": "Xt5EWLLDS7FJjR1c",
    "brand": "Visa",
    "funding": "credit",
    "metadata": {},
    "instanceURL": null
  }
}
```

> Make sure to replace `X-Auth-Token` with your API key.


### HTTP Request

`POST
http://localhost:8080/PaymentModule/api/token/create
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
 Card | Card for detail  | String | Required
Number | Number of Card | Integer | Required
CVC Check | CVC check number | Integer | Required
Exp Month | Exp Month | Integer | Required
Exp Year | Exp Year | Integer | Required
Name  | Name | String | Required

### Response

Parameter | Description | Type
--------- | ----------- | ----
Amount | Amount of fees | String | 
Created | Created  | String
Currency | Currency | String
ID | ID | Integer
Live mode | Live mode | String
Used | Used| String
Card | Card number | Integer
Exp Month | Exp Month | Integer
Exp Year| Exp Year | Integer
Last4 | Last 4 | String
Country | Country | String
Type | Type | String
Name | Name | String
ID | ID | Integer
Customer | Customer | String
Recipient | Recipient | String
Address Line1 | Address Line1 | String
Address Line2 | Address Line2 | String
Address Zip | Address Zip | String
Address City | Address City | String
Address State | Address State | String
Address Country | Address Country | String
Address Zip Check | Address Zip Check | String
Address Line1 Check | Address Line Check | String
CVC Check | CVC Check | String
Finger print | Finger print | String
Brand | Brand | String
Funding | Funding | String
Instance URL | Instance URL |String



`Authorization: X-Auth-Token`

<aside class="notice">
You must replace <code>X-Auth-Token</code> with your personal API key.
</aside>


## Create Card

```shell
curl -i -H "Content-Type:application/json" -H "X-Auth-Token:patientuser@cooldoctors.io:patient:1515429239598:a0e476b75ffbacedd65e555b5304b222" -X GET "http://api.endpoint.eyecarelive.com/PaymentModule/api/customer/retrive/cus_6mvDwopNRvMjcJ"

```
> The above command returns JSON structured like this:

```json
{
  "created": 1439471030,
  "id": "cus_6mvDwopNRvMjcJ",
  "livemode": false,
  "deleted": null,
  "description": null,
  "defaultCard": null,
  "defaultSource": "card_16ZLMh2eZvKYlo2C0mHJYiDH",
  "email": null,
  "trialEnd": null,
  "discount": null,
  "nextRecurringCharge": null,
  "subscriptions": {
    "data": [],
    "totalCount": 0,
    "hasMore": false,
    "url": "/v1/customers/cus_6mvDwopNRvMjcJ/subscriptions",
    "count": null
  },
  "subscription": null,
  "delinquent": false,
  "accountBalance": 0,
  "currency": null,
  "cards": null,
  "sources": {
    "data": [
      {
        "id": "card_16ZLMh2eZvKYlo2C0mHJYiDH",
        "object": "card",
        "customer": "cus_6mvDwopNRvMjcJ",
        "account": null,
        "status": null,
        "expMonth": 12,
        "expYear": 2016,
        "last4": "4242",
        "dynamicLast4": null,
        "country": "US",
        "type": null,
        "name": "nitesh",
        "recipient": null,
        "addressLine1": null,
        "addressLine2": null,
        "addressZip": null,
        "addressCity": null,
        "addressState": null,
        "addressCountry": null,
        "addressZipCheck": null,
        "addressLine1Check": null,
        "cvcCheck": "pass",
        "fingerprint": "Xt5EWLLDS7FJjR1c",
        "brand": "Visa",
        "funding": "credit",
        "metadata": {},
        "instanceURL": "https://api.stripe.com/v1/customers/cus_6mvDwopNRvMjcJ/sources/card_16ZLMh2eZvKYlo2C0mHJYiDH"
      },
      {
        "id": "card_16ZLQY2eZvKYlo2CJllR9Hwg",
        "object": "card",
        "customer": "cus_6mvDwopNRvMjcJ",
        "account": null,
        "status": null,
        "expMonth": 12,
        "expYear": 2016,
        "last4": "4242",
        "dynamicLast4": null,
        "country": "US",
        "type": null,
        "name": "nitesh",
        "recipient": null,
        "addressLine1": null,
        "addressLine2": null,
        "addressZip": null,
        "addressCity": null,
        "addressState": null,
        "addressCountry": null,
        "addressZipCheck": null,
        "addressLine1Check": null,
        "cvcCheck": "pass",
        "fingerprint": "Xt5EWLLDS7FJjR1c",
        "brand": "Visa",
        "funding": "credit",
        "metadata": {},
        "instanceURL": "https://api.stripe.com/v1/customers/cus_6mvDwopNRvMjcJ/sources/card_16ZLQY2eZvKYlo2CJllR9Hwg"
      }
    ],
    "totalCount": 2,
    "hasMore": false,
    "url": "/v1/customers/cus_6mvDwopNRvMjcJ/sources",
    "count": null
  },
  "metadata": {}
}
```

> Make sure to replace `X-Auth-Token` with your API key.


### HTTP Request

`POST
http://api.endpoint.eyecarelive.com/PaymentModule/api/card/create 
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
Token | Token | String | Required
Customer | Customer | String | Required

### Response

Parameter | Description | Type
--------- | ----------- | ----
ID | ID | Integer 
Object |  Object  | String
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

`Authorization: X-Auth-Token`

<aside class="notice">
You must replace <code>X-Auth-Token</code> with your personal API key.
</aside>


## Create Customer

```shell
curl -i -H "Content-Type: application/json" -H "X-Auth-Token:patientuser@cooldoctors.io:patient:1515429239598:a0e476b75ffbacedd65e555b5304b222" "http://api.endpoint.eyecarelive.com/PaymentModule/api/customer/create" -X POST -d'{"token":"tok_16ZLCT2eZvKYlo2CV4n8Nfyb"}'
```
> The above command returns JSON structured like this:

```json
{
	"success": true
}
```

> Make sure to replace `X-Auth-Token` with your API key.


### HTTP Request

`POST
http://api.endpoint.eyecarelive.com/PaymentModule/api/customer/create
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
Source | Source | String | Required


### Response

Parameter | Description | Type
--------- | ----------- | ----
Object |  Object  | String
Created | Created | String
ID | ID | Integer | 
Live mode | Live mode  | String
Description | Description | String
Email | Email | String
Delinquent | Delinquent | String
Metadata | Metadata | String
Subscriptions:[{}] | Subscriptions | String
Discount | Discount | String
Account_balance | Account balance | String
Currency | Currency | String
Sources | Sources | String
Object |  Object  | String
Total_count | Total count | String
Has_more |  Has more  | String
URL |  URL  | String
Data:[{}] |  Data  | String
Default_source :[{}] |  Default source  | String

`Authorization: X-Auth-Token`

<aside class="notice">
You must replace <code>X-Auth-Token</code> with your personal API key.
</aside>



## Retrieve Card


```shell
curl -i -H "Content-Type:application/json" -H "X-Auth-Token:patientuser@cooldoctors.io:patient:1515429239598:a0e476b75ffbacedd65e555b5304b222" -X GET "http://api.endpoint.eyecarelive.com/PaymentModule/api/card/retrive/card_16ZLQY2eZvKYlo2CJllR9Hwg/cus_6mvDwopNRvMjcJ"
```
> The above command returns JSON structured like this:

```json
{
  "id": "card_16ZLQY2eZvKYlo2CJllR9Hwg",
  "object": "card",
  "customer": "cus_6mvDwopNRvMjcJ",
  "account": null,
  "status": null,
  "expMonth": 12,
  "expYear": 2016,
  "last4": "4242",
  "dynamicLast4": null,
  "country": "US",
  "type": null,
  "name": "nitesh",
  "recipient": null,
  "addressLine1": null,
  "addressLine2": null,
  "addressZip": null,
  "addressCity": null,
  "addressState": null,
  "addressCountry": null,
  "addressZipCheck": null,
  "addressLine1Check": null,
  "cvcCheck": "pass",
  "fingerprint": "Xt5EWLLDS7FJjR1c",
  "brand": "Visa",
  "funding": "credit",
  "metadata": {},
  "instanceURL": "https://api.stripe.com/v1/customers/cus_6mvDwopNRvMjcJ/sources/card_16ZLQY2eZvKYlo2CJllR9Hwg"
}
```

> Make sure to replace `X-Auth-Token` with your API key.


### HTTP Request

`GET
http://api.endpoint.eyecarelive.com/PaymentModule/api/card/retrive/<id>/<customerId>
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
ID | ID | Integer | Required
Customer ID | Customer ID | Integer | Required



### Response

Parameter | Description | Type
--------- | ----------- | ----
ID | ID | Integer 
Object |  Object  | String
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


`Authorization: X-Auth-Token`

<aside class="notice">
You must replace <code>X-Auth-Token</code> with your personal API key.
</aside>


## Delete Card

```shell
curl -i -H "Content-Type: application/json" -H "X-Auth-Token:patientuser@cooldoctors.io:patient:1515429239598:a0e476b75ffbacedd65e555b5304b222" -X DELETE "http://api.endpoint.eyecarelive.com/PaymentModule/api/card/cus_6nJo1fsmsayvtc/card_6nJoOW0jMFfsTE"
```
> The above command returns JSON structured like this:

```json
{
  "id": "card_6nJoOW0jMFfsTE",
  "deleted": true
}
```

> Make sure to replace `X-Auth-Token` with your API key.


### HTTP Request

`DELETE
http://api.endpoint.eyecarelive.com/PaymentModule/api/card/CustomerID/cardID"
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
/PaymentModule/api/card/{id} | For the delete card | String | Required


### Response

Parameter | Description | Type
--------- | ----------- | ----
Deleted | Delete status (true,false) | String
ID | ID | Integer
Object | Object | String


`Authorization: X-Auth-Token`

<aside class="notice">
You must replace <code>X-Auth-Token</code> with your personal API key.
</aside>


