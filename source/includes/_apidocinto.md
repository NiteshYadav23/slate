

# Doctor API Introduction


# Create Doctor

## Sign Up

```shell
curl -i -H "Content-Type: application/json" "http://api.endpoint.eyecarelive.com/DoctorToDoctor/api/auth/signup" -X POST -d '{"email":"newsignupapi@eyecarelive.com","password":"demo1234","aboutMe":{"firstName":"NewSignUp","lastName":"API","address":"350 5th Ave","city":"New York","state":"NY","country":"US","pincode":"60015","gender":"male","languagesSpeak" : ["English","",""]},"role":{"id":"551ad2ffe4b0b59ff0cceccb","name":"doctor"},"contactInfo":{"email":"dpress@nsvc.com","phone":"847.412.0311"}, "doctorInfo" : {"educationList":[{"degree":"OD","university":"University of Houston","yearOfPasssing":""},{"degree":"OD Doctor of Optometry ","university":"University of Houston","yearOfPasssing":""}],"hospitalAttachedWithList":[{"name":"Eyesite optometric group paul super O.D.","city":"Brentwood Los Angeles,","country":"USA"}],"awardsReceivedList":[{"name":"Better Vision Award","description":"Eye Care","date":""}],"availabilityTimeZone":"Asia/Kolkata","specialities":[{"id":"55b7802be4b0b393bf91678e"}],"registrationNumber":"22222","licencedState":[{"state":"CA"},{"state":"CA"}]}}'
 
```
> The above command returns JSON structured like this:

```json
{
  "id": "55de9c50e4b0c34612e032ee",
  "email": "niteshy2391@gmail.com",
  "pharmacyName": null,
  "pharmacyAddress": null,
  "profileImageId": null,
  "profileImageName": null,
  "aboutMe": {
    "id": "55de9c50e4b0c34612e032ec",
    "firstName": "Nitesh",
    "lastName": "Yadav",
    "birthDate": null,
    "address": "Pune",
    "city": "Pune",
    "country": "india",
    "pincode": "411045",
    "gender": "female",
    "languagesSpeak": null,
    "additionalInfo": null,
    "state": "Maharashtra"
  },
  "contactInfo": {
    "id": "55de9c50e4b0c34612e032ed",
    "email": "niteshy2391@gmail.com",
    "phone": "1111111111"
  },
  "patientInfo": null,
  "doctorInfo": null,
  "role": {
    "id": "551ad2ffe4b0b59ff0cceccb",
    "name": "doctor"
  },
  "timezone": {
    "id": "54d9a31744aefa00c1d23342",
    "timezone": "Asia/Kolkata",
    "displayName": null
  },
  "createdAt": "2015-08-27 08:12 AM IDT",
  "forgotPasswordToken": null,
  "familyMembers": null,
  "parentUser": null,
  "parentUserRelation": null,
  "password": null,
  "rating": null,
  "preferredPharmacies": null,
  "kandyUserName": null,
  "kandyUserPassword": null,
  "kandyFullUserId": null,
  "oldPassword": null,
  "loginStatus": null,
  "stripeCustId": null,
  "profileImagePath": null,
  "isReferredDoctor": null,
  "randomtoken": "ZnwMJq",
  "isEmailVerified": false,
  "invited": false,
  "validated": false,
  "activated": false,
  "managedUser": false
}
```

In sign up API for Doctor, Need to pass ROLE parameter in API which is need to be fixed. Always in sign up API this parameter  ID and name of ROLE should be fix. Please check below ID and Name.


### HTTP Request

`POST
http://localhost:8080/DoctorOnDemand/api/auth/signup
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
FirstName | Doctor’s First Name | String | Required
LastName | Doctor’s Last Name | String | Required
Email | Doctor’s Email address | String | Required
Password | Doctor’s Password | String | Required
Pincode | Pincode of Doctor's Area |Integer | Optional
Address | Doctor’s Address | String | Optional
City | City | String | Optional
State | Name of State | String | Optional
Country | Country | String | Optional
BirthDate | Date of Birth (MM/DD/YYYY) | String | Optional
Gender | Gender (M,F) | String | Required
Role(ID,NAME) | Role (ID and Name) | String | Required
ContactInfo[{}] | ContactInfo Details | String | Optional
 | **Doctor Info** |  |
educationList | Doctor's Education details | String | Optional
hospitalAttachedWithList | List of Hospitals teid up with Doctors | String | Optional
awardsReceivedList | Awards Received by the Doctor | String | Optional
availabilityTimeZone | Time zone opted by Doctor | String | Optional
specialities[{}] | Specialities of Doctor | String | Optional
registrationNumber | Registration Number of Doctor| String | Optional
licencedState | Licensed State of Doctor | String | Required

### Response

Parameter | Description | Type 
--------- | ----------- | ----
ID |ID of Doctor | Integer
Email ID | Doctor's Email ID | String
Pharmacy Name | Pharmacy name | String
pharmacy Address | pharmacy Address | String
profile Image Id | Profile image ID | Integer
profile Image Name | Profile image Name | .jpg,etc
About Me :[{}] | About me info for the Doctor | String
Contact Info:[{}] | Contact person Info | String
Patient Info :[{}] | Patient info | String
Time zone | Time zone | String
Created At:[{}] | Date and Time Created at | String


<aside class="info">
Remember - To pass all the required parameters correctly !!
</aside>

## Activate Doctor

```shell
curl -i -H "Content-Type:application/json" -H "X-Auth-Token:patilnak88@gmail.com:admin:1515516167302:73eee16ab9e185d0fbfb21f0fba9ad25" -X POST "http://api.endpoint.eyecarelive.com/DoctorOnDemand/api/admin/user/activate/5a2d64f4e4b02c0a7433f43f"

 
```
> The above command returns JSON structured like this:

```json
{
  "success": true
}
```
> Make sure to replace `X-Auth-Token` with your API key.

In sign up API for Doctor, Need to pass ROLE parameter in API which is need to be fixed. Always in sign up API this parameter  ID and name of ROLE should be fix. Please check below ID and Name.


### HTTP Request

`POST
http://localhost:8080//DoctorOnDemand/api/admin/user/activate/ID
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
/DoctorOnDemand/api/admin/user/activate/ID | Valid ID for Activate Doctor | Integer | Required

### Response

Parameter | Description | Type 
--------- | ----------- | ----
{“success”:”True”} | {“success”:”True”} it Means successful Response | String


<aside class="info">
Remember - The Doctor account is created only when Admin activates Doctor !!
</aside>



