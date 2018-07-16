

# Doctor Authentication

User authentication is implemented by email address and password

## Login - Login as Doctor

```shell
curl -i -H "Content-Type: application/json" "https://api.endpoint.eyecarelive.com/DoctorOnDemand/api/auth/login" -X POST -d '{"email" : "patientuser@cooldoctors.io","password" : "demo1234"}'
```
> The above command returns JSON structured like this:

```json
{
  "id": "5a2c0c91e4b0e4fa266e0181",
  "userId": "5a2c0a69e4b0e4fa266e0180",
  "token": "patientuser@cooldoctors.io:patient:1515428241291:5eb24f92a4160a1864abb7738802e449",
  "dateTime": "2017-12-09 08:17 AM PST"
}
```
### HTTP Request

`POST http://localhost:8080/DoctorOnDemand/api/auth/login
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
Email | Doctor's Email address | String | Required
Password | Doctor’s Password | String | Required

### Response

Parameter |  Description | Type 
--------- | ------------ | ---- 
ID | Internal system id#. Deprecated | Integer 
USER ID | User ID of Patient | Integer
TOKEN | Authentication Token | String
Date Time | User account created date and time | String

<aside class="success">
 Correct Email and Password leads to successful login!
</aside>

## Logout - Doctor logout

```shell
curl -i -H "Content-Type: application/json" -H "X-Auth-Token:patientuser@cooldoctors.io:patient:1515428241291:5eb24f92a4160a1864abb7738802e449" "https://api.endpoint.eyecarelive.com/DoctorOnDemand/api/auth/logout"  -X POST
```
> The above command returns JSON structured like this:

```json
{"success":true}
```
### HTTP Request

`POST http://localhost:8080/DoctorOnDemand/api/auth/logout
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
ID | Doctor’s ID | Integer | Required
Token | Doctor’s authentication token | Integer | Required


### Response

Parameter |  Description | Type
--------- | ------------ | ----
Success | Logout successful True OR False | String

<aside class="notice">
ID and Token are must to be successfully logged out!
</aside>

## Forgot Password

```shell

curl -i -H "Content-Type: application/json" -H "X-Auth-Token:patientuser@cooldoctors.io:patient:1515428241291:5eb24f92a4160a1864abb7738802e449" "https://api.endpoint.eyecarelive.com/DoctorOnDemand/api/auth/forgotpassword"  -X POST -d '{"email":"niteshy2391@gmail.com"}'

```

```shell

curl -i -H "Content-Type: application/json" -H "X-Auth-Token:patientuser@cooldoctors.io:patient:1515428241291:5eb24f92a4160a1864abb7738802e449" "https://api.endpoint.eyecarelive.com/DoctorOnDemand/api/auth/changeforgotpassword"  -X POST -d '{"email":"niteshy2391@gmail.com","forgotPasswordToken":"12313","password":"demo1234"}'

```

> The above command returns JSON structured like this:

```json

{
	"success": true
}

```

> Make sure to replace `X-Auth-Token` with your API key.

First API will generate the security and send on reg. Email address.

Use this API for changing the password

### HTTP Request

`POST
http://localhost:8080/DoctorOnDemand/api/auth/forgotpassword
`

### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
Reg. Email Address | Need to enter Reg. Email address| String | Required


### Response

Parameter | Description | Type
--------- | ----------- | ----
success | True Or False | String 


### HTTP Request

`POST
http://localhost:8080/DoctorOnDemand/api/auth/changeforgotpassword
`

### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
Reg. Email Address | Need to enter Reg. Email address | String | Required
forgotPasswordToken | Forgot password token which will gets on email | String | Required
password | New password | String | Required


### Response

Parameter | Description | Type
--------- | ----------- | ----
success | True Or False | String 


`Authorization: X-Auth-Token`

<aside class="notice">
You must replace <code>X-Auth-Token</code> with your personal API key.
</aside>


## Reset password after Login

```shell

curl -i -H "Content-Type: application/json" -H "X-Auth-Token:patientuser@cooldoctors.io:patient:1515428241291:5eb24f92a4160a1864abb7738802e449" "https://api.endpoint.eyecarelive.com/DoctorOnDemand/api/auth/resetpassword"  -X POST -d '{"email":"niteshy2391@gmail.com"}'

```

```shell

curl -i -H "Content-Type: application/json" -H "X-Auth-Token:patientuser@cooldoctors.io:patient:1515428241291:5eb24f92a4160a1864abb7738802e449" "https://api.endpoint.eyecarelive.com/DoctorOnDemand/api/auth/changepassword"  -X POST -d '{password: "demo1234", forgotPasswordToken: "8393", email: "nitesh.yadav@cooldoctors.io"}'

```

> The above command returns JSON structured like this:

```json

{
	"success": true
}

```

> Make sure to replace `X-Auth-Token` with your API key.

First API will generate the security and send on reg. Email address.

Use this API for changing the password

### HTTP Request

`POST
http://localhost:8080/DoctorOnDemand/api/auth/forgotpassword
`

### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
Reg. Email Address | Need to enter Reg. Email address| String | Required


### Response

Parameter | Description | Type
--------- | ----------- | ----
success | True Or False | String 


### HTTP Request

`POST
http://localhost:8080/DoctorOnDemand/api/auth/changeforgotpassword
`

### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
Reg. Email Address | Need to enter Reg. Email address | String | Required
forgotPasswordToken | Forgot password token which will gets on email | String | Required
password | New password | String | Required


### Response

Parameter | Description | Type
--------- | ----------- | ----
success | True Or False | String 


`Authorization: X-Auth-Token`

<aside class="notice">
You must replace <code>X-Auth-Token</code> with your personal API key.
</aside>



