

# Reset password

## Reset password after log in

```shell
curl -i -H "Content-Type:application/json" -H "x-auth-token:patientuser1@eyecarelive.com:patient:1561784861568:d5171513ed94a5fafb354f6f8688b751" "https://dev.api.cooldoctors.io:8443/DoctorOnDemand/api/auth/forgotpassword" -X POST -d '{"email":"nitesh.yadav@cooldoctors.io"}'
```
> The above command returns JSON structured like this:

```json
{
  "success": "true"
}
```
### HTTP Request

`http://localhost:8080/DoctorOnDemand/api/auth/resetpassword/
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
Email | Patient Email address | String | Required

### Response

Parameter |  Description | Type 
--------- | ------------ | ---- 
Success | True | boolean 


<aside class="notice">
 Correct Email and Password leads to successful login!
</aside>


## Change password.

```shell
 curl -i -H "Content-Type: application/json" -H "x-auth-token:patientuser1@eyecarelive.com:patient:1561784861568:d5171513ed94a5fafb354f6f8688b751" "https://dev.api.cooldoctors.io:8443/DoctorOnDemand/api/auth/changepassword" -X POST -d '{"password":"demo1234","forgotPasswordToken":"5391"}'
```
> The above command returns JSON structured like this:

```json
{
  "success": "true"
}
```
### HTTP Request

`http://localhost:8080/DoctorOnDemand/api/auth/changepassword/
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
Email | Patient Email address | String | Required
Password | Patient Password | String | Required
forgotPasswordToken | security token | Required

### Response

Parameter |  Description | Type 
--------- | ------------ | ---- 
Success | True | boolean 


<aside class="notice">
 Correct Email and Password leads to successful login!
</aside>