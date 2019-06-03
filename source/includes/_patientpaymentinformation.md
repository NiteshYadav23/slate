


# Patient Payment Information


## Create Token 

```shell
curl -i -H "Content-Type: application/json" -H "X-Auth-Token:patientuser1@eyecarelive.com:patient:1561784861568:d5171513ed94a5fafb354f6f8688b751" "https://dev.api.cooldoctors.io:8443/PaymentModule/api/token/create" -X POST -d '{ "card":{"number":"4242424242424242","cvcCheck":"779","expMonth":"12","expYear":"2020","name":"nitesh"}}'


```
> The above command returns JSON structured like this:

```json
{
  "id": "tok_FBlSRe8UzE8BDH",
  "object": "token",
  "amount": null,
  "bankAccount": null,
  "card": {
    "id": "card_FBlS4jOwiPwJWH",
    "object": "card",
    "account": null,
    "customer": null,
    "metadata": {
      
    },
    "addressCity": "Pune",
    "addressCountry": null,
    "addressLine1": "Baner",
    "addressLine1Check": null,
    "addressLine2": null,
    "addressState": "GA",
    "addressZip": "12345",
    "addressZipCheck": null,
    "availablePayoutMethods": null,
    "brand": "Visa",
    "country": "US",
    "currency": null,
    "cvcCheck": null,
    "defaultForCurrency": null,
    "dynamicLast4": null,
    "expMonth": 8,
    "expYear": 2022,
    "fingerprint": "KDAfyJ5KSCkzem6v",
    "funding": "credit",
    "last4": "4242",
    "name": "Bhagwant Sangvikar",
    "recipient": null,
    "status": null,
    "threeDSecure": null,
    "tokenizationMethod": null,
    "description": null,
    "iin": null,
    "issuer": null,
    "type": "Visa",
    "instanceURL": null
  },
  "clientIp": "18.211.185.254",
  "created": 1559598177,
  "currency": null,
  "email": null,
  "livemode": false,
  "type": "card",
  "used": false
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
addressLine1 | Address | Required
addressState | State name | Required
addressCity | City name | Required
addressZip | Zipcode | Required

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
curl -i -H "Content-Type: application/json" -H "X-Auth-Token:patientuser1@eyecarelive.com:patient:1561784861568:d5171513ed94a5fafb354f6f8688b751" "https://dev.api.cooldoctors.io:8443/PaymentModule/api/card/create" -X POST -d'{"customer":"cus_FB9sZiGM7eeF2m","token":"tok_FBA2VMl89mJdjP"}'

```
> The above command returns JSON structured like this:

```json
{
  "id": "card_FBA2bVybjiMbzB",
  "object": "card",
  "account": null,
  "customer": "cus_FB9sZiGM7eeF2m",
  "metadata": {
    
  },
  "addressCity": null,
  "addressCountry": null,
  "addressLine1": null,
  "addressLine1Check": null,
  "addressLine2": null,
  "addressState": null,
  "addressZip": null,
  "addressZipCheck": null,
  "availablePayoutMethods": null,
  "brand": "Visa",
  "country": "US",
  "currency": null,
  "cvcCheck": "pass",
  "defaultForCurrency": null,
  "dynamicLast4": null,
  "expMonth": 12,
  "expYear": 2020,
  "fingerprint": "KDAfyJ5KSCkzem6v",
  "funding": "credit",
  "last4": "4242",
  "name": "nitesh",
  "recipient": null,
  "status": null,
  "threeDSecure": null,
  "tokenizationMethod": null,
  "description": null,
  "iin": null,
  "issuer": null,
  "type": "Visa",
  "instanceURL": "https://api.stripe.com/v1/customers/cus_FB9sZiGM7eeF2m/sources/card_FBA2bVybjiMbzB"
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
curl -i -H "Content-Type: application/json" -H "X-Auth-Token:patientuser1@eyecarelive.com:patient:1561784861568:d5171513ed94a5fafb354f6f8688b751" "https://dev.api.cooldoctors.io:8443/PaymentModule/api/customer/create" -X POST -d'{"token":"tok_FAwF3JyKlKIgMN"}'
```
> The above command returns JSON structured like this:

```json
{
  "id": "cus_FAwHi7Rdecx28Q",
  "object": "customer",
  "accountBalance": 0,
  "businessVatId": null,
  "created": 1559407780,
  "currency": null,
  "defaultSource": "card_FAwF2AxsUdq47f",
  "deleted": null,
  "delinquent": false,
  "description": null,
  "discount": null,
  "email": null,
  "livemode": false,
  "metadata": {
    
  },
  "shipping": null,
  "sources": {
    "data": [
      {
        "id": "card_FAwF2AxsUdq47f",
        "object": "card",
        "account": null,
        "customer": "cus_FAwHi7Rdecx28Q",
        "metadata": {
          
        },
        "addressCity": null,
        "addressCountry": null,
        "addressLine1": null,
        "addressLine1Check": null,
        "addressLine2": null,
        "addressState": null,
        "addressZip": null,
        "addressZipCheck": null,
        "availablePayoutMethods": null,
        "brand": "Visa",
        "country": "US",
        "currency": null,
        "cvcCheck": "pass",
        "defaultForCurrency": null,
        "dynamicLast4": null,
        "expMonth": 12,
        "expYear": 2020,
        "fingerprint": "KDAfyJ5KSCkzem6v",
        "funding": "credit",
        "last4": "4242",
        "name": "nitesh",
        "recipient": null,
        "status": null,
        "threeDSecure": null,
        "tokenizationMethod": null,
        "description": null,
        "iin": null,
        "issuer": null,
        "type": "Visa",
        "instanceURL": "https://api.stripe.com/v1/customers/cus_FAwHi7Rdecx28Q/sources/card_FAwF2AxsUdq47f"
      }
    ],
    "totalCount": 1,
    "hasMore": false,
    "requestOptions": null,
    "requestParams": null,
    "url": "/v1/customers/cus_FAwHi7Rdecx28Q/sources",
    "count": 1
  },
  "subscriptions": {
    "data": [
      
    ],
    "totalCount": 0,
    "hasMore": false,
    "requestOptions": null,
    "requestParams": null,
    "url": "/v1/customers/cus_FAwHi7Rdecx28Q/subscriptions",
    "count": 0
  },
  "cards": {
    "data": [
      {
        "id": "card_FAwF2AxsUdq47f",
        "object": "card",
        "account": null,
        "customer": "cus_FAwHi7Rdecx28Q",
        "metadata": {
          
        },
        "addressCity": null,
        "addressCountry": null,
        "addressLine1": null,
        "addressLine1Check": null,
        "addressLine2": null,
        "addressState": null,
        "addressZip": null,
        "addressZipCheck": null,
        "availablePayoutMethods": null,
        "brand": "Visa",
        "country": "US",
        "currency": null,
        "cvcCheck": "pass",
        "defaultForCurrency": null,
        "dynamicLast4": null,
        "expMonth": 12,
        "expYear": 2020,
        "fingerprint": "KDAfyJ5KSCkzem6v",
        "funding": "credit",
        "last4": "4242",
        "name": "nitesh",
        "recipient": null,
        "status": null,
        "threeDSecure": null,
        "tokenizationMethod": null,
        "description": null,
        "iin": null,
        "issuer": null,
        "type": "Visa",
        "instanceURL": "https://api.stripe.com/v1/customers/cus_FAwHi7Rdecx28Q/sources/card_FAwF2AxsUdq47f"
      }
    ],
    "totalCount": 1,
    "hasMore": false,
    "requestOptions": null,
    "requestParams": null,
    "url": "/v1/customers/cus_FAwHi7Rdecx28Q/cards",
    "count": 1
  },
  "defaultCard": "card_FAwF2AxsUdq47f",
  "nextRecurringCharge": null,
  "subscription": null,
  "trialEnd": null
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
Token | Token ID | String | Required


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
curl -i -H "Content-Type:application/json" -H "X-Auth-Token:patientuser1@eyecarelive.com:patient:1561784861568:d5171513ed94a5fafb354f6f8688b751" "https://dev.api.cooldoctors.io:8443/PaymentModule/api/card/retrive/card_16ZLQY2eZvKYlo2CJllR9Hwg/cus_6mvDwopNRvMjcJ"
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

## Get List of card

```shell
curl -i -H "Content-Type:application/json" -H "X-Auth-Token:patientuser1@eyecarelive.com:patient:1561784861568:d5171513ed94a5fafb354f6f8688b751" -X GET "https://dev.api.cooldoctors.io:8443/PaymentModule/api/card/listall/cus_FAwHi7Rdecx28Q/1"
```
> The above command returns JSON structured like this:

```json
{
  "data": [
    {
      "id": "card_FAwF2AxsUdq47f",
      "object": "card",
      "account": null,
      "customer": "cus_FAwHi7Rdecx28Q",
      "metadata": {
        
      },
      "addressCity": null,
      "addressCountry": null,
      "addressLine1": null,
      "addressLine1Check": null,
      "addressLine2": null,
      "addressState": null,
      "addressZip": null,
      "addressZipCheck": null,
      "availablePayoutMethods": null,
      "brand": "Visa",
      "country": "US",
      "currency": null,
      "cvcCheck": "pass",
      "defaultForCurrency": null,
      "dynamicLast4": null,
      "expMonth": 12,
      "expYear": 2020,
      "fingerprint": "KDAfyJ5KSCkzem6v",
      "funding": "credit",
      "last4": "4242",
      "name": "nitesh",
      "recipient": null,
      "status": null,
      "threeDSecure": null,
      "tokenizationMethod": null,
      "description": null,
      "iin": null,
      "issuer": null,
      "type": "Visa",
      "instanceURL": "https://api.stripe.com/v1/customers/cus_FAwHi7Rdecx28Q/sources/card_FAwF2AxsUdq47f"
    }
  ],
  "totalCount": null,
  "hasMore": false,
  "requestOptions": null,
  "requestParams": {
    "limit": "1",
    "object": "card"
  },
  "url": "/v1/customers/cus_FAwHi7Rdecx28Q/sources",
  "count": 1
}
```

> Make sure to replace `X-Auth-Token` with your API key.


### HTTP Request

`DELETE
http://api.endpoint.eyecarelive.com/PaymentModule/api/card/listall/{CustomerID}/1"
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
{CustomerID}/1 | Pass in the URL | String | Required


### Response

Parameter | Description | Type
--------- | ----------- | ----
Deleted | Delete status (true,false) | String
data:[{}] | This will return the array | Integer
totalCount | Object | String
requestOptions | Object | String
hasMore | Object | String
requestParams:[{}] | Object | String
url | Object | String
count | Object | String


`Authorization: X-Auth-Token`

<aside class="notice">
You must replace <code>X-Auth-Token</code> with your personal API key.
</aside>


## Get Customer ID 

```shell
curl -i -H "Content-Type:application/json" -H "X-Auth-Token:patientuser1@eyecarelive.com:patient:1561784861568:d5171513ed94a5fafb354f6f8688b751" -X GET "https://dev.api.cooldoctors.io:8443/DoctorOnDemand/api/patient/user/getstripecustomerid"
```
> The above command returns JSON structured like this:

```json
{
  "customer_id": "cus_FB9sZiGM7eeF2m"
}
```

> Make sure to replace `X-Auth-Token` with your API key.


### HTTP Request

`DELETE
http://api.endpoint.eyecarelive.com/DoctorOnDemand/api/patient/user/getstripecustomerid"
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
URL | Use URL to get this | String | Required


### Response

Parameter | Description | Type
--------- | ----------- | ----
customer_id | Customer ID | Integer


`Authorization: X-Auth-Token`

<aside class="notice">
You must replace <code>X-Auth-Token</code> with your personal API key.
</aside>

## Add Customer ID

```shell
curl -i -H "Content-Type: application/json" -H "X-Auth-Token:patientuser1@eyecarelive.com:patient:1561784861568:d5171513ed94a5fafb354f6f8688b751" "https://dev.api.cooldoctors.io:8443/DoctorOnDemand/api/patient/user/addstripecustomer/cus_FB9sZiGM7eeF2m" -X POST 
```
> The above command returns JSON structured like this:

```json
{
  "success": true
}
```

> Make sure to replace `X-Auth-Token` with your API key.


### HTTP Request

`DELETE
http://api.endpoint.eyecarelive.com/DoctorOnDemand/api/patient/user/addstripecustomer/{CustomerID}"
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
{id} in the URL | to add the customer| String | Required


### Response

Parameter | Description | Type
--------- | ----------- | ----
success | true /false | blooean


`Authorization: X-Auth-Token`

<aside class="notice">
You must replace <code>X-Auth-Token</code> with your personal API key.
</aside>

## Remove Card

```shell
curl -i -H "Content-Type: application/json" -H "X-Auth-Token:patientuser1@eyecarelive.com:patient:1561784861568:d5171513ed94a5fafb354f6f8688b751" "https://dev.api.cooldoctors.io:8443/PaymentModule/api/card/cus_6nJo1fsmsayvtc/card_6nJoOW0jMFfsTE"
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


