


# Patient User Profile

User’s profile has several important details and includes the following sections:

1. Personal information - Name, Date of birth, Gender
2. Contact information such as phone number, address and email address
3. Lifestyle - basic information such as diet type (For e.g Vegan), Tobacco use, Alcohol consumption (# drinks per week), Contact lens usage and any medical conditions that eye care provider should know
4. Family History - including any serious conditions in the family. User can list as many of these as needed and is usually formed as Condition:Relationship pairs.
5. Medical History - currently taking any medications, supplements, vtamins and has any allergies to medications.
6. Payment Information - User must add at least one credit card
7. Insurance Information - One or more insurance plan information. User has option to provide photos of the insurance cards.
8. Pharmacy - User may optionally provide their preferred pharmacy name. This helps doctors write e-prescriptions. E-prescription is not integrated with Eyecarelive but doctors can use e-prescription from their EMR system.
9. Family members - Primary user can add one or more family members who can be seen by the doctor on the same app. Family members may be primary user’s minor children who may utilize same insurance plan and credit card for payment.


## Get Patient Profile 

```shell
curl -i -H "Content-Type:application/json" -H "X-Auth-Token:patientuser1@eyecarelive.com:patient:1561784861568:d5171513ed94a5fafb354f6f8688b751" -X GET "https://dev.api.cooldoctors.io:8443/DoctorOnDemand/api/patient/user/5ceed13cf893f45b5812b8e1"
```
> The above command returns JSON structured like this:

```json
{
  "id": "5ceed13cf893f45b5812b8e1",
  "email": "patientuser1@eyecarelive.com",
  "pharmacyName": null,
  "pharmacyAddress": null,
  "aboutMe": {
    "id": "5ceed13cf893f45b5812b8de",
    "firstName": "Demo",
    "lastName": "User",
    "birthDate": "",
    "address": "",
    "city": "",
    "country": "",
    "pincode": "",
    "gender": null,
    "languagesSpeak": null,
    "additionalInfo": null,
    "state": "",
    "lat": null,
    "lang": null
  },
  "contactInfo": null,
  "patientInfo": null,
  "doctorInfo": null,
  "role": {
    "id": "551ad2a4e4b0b59ff0ccecc9",
    "name": "patient"
  },
  "timezone": {
    "id": "55f283b4e4b029528c27d0c5",
    "timezone": "Asia/Kolkata",
    "displayName": "India Standard Time"
  },
  "createdAt": "2019-05-29 11:36 AM PDT",
  "forgotPasswordToken": null,
  "familyMembers": null,
  "parentUser": null,
  "parentUserRelation": null,
  "password": null,
  "rating": null,
  "preferredPharmacies": null,
  "oldPassword": null,
  "loginStatus": "Online",
  "stripeCustId": null,
  "profileImagePath": null,
  "isReferredDoctor": null,
  "randomtoken": "BThd5P",
  "isEmailVerified": false,
  "preferredDoctors": null,
  "isAcceptTC": false,
  "insurenceCards": null,
  "notificationSettings": {
    "id": "5ceed13cf893f45b5812b8df",
    "email": true,
    "push": true,
    "sms": true,
    "sendReminderForMedicine": true,
    "addTestreport": true,
    "sentMessage": true,
    "addTreatmentPlan": true,
    "sendReminderForEyeTest": true
  },
  "clinics": null,
  "passCode": null,
  "emrId": null,
  "ssnId": null,
  "clinicInfo": null,
  "ref": null,
  "docOrg": null,
  "doctorsOrg": null,
  "twilioAccessToken": null,
  "bucket": null,
  "repoSub": false,
  "badge": null,
  "preferredEclClinics": null,
  "eclClinicId": null,
  "profileColor": null,
  "addedByCpm": false,
  "activated": true,
  "invited": false,
  "validated": true,
  "pilotDoc": false,
  "managedUser": false
}
```

> Make sure to replace `X-Auth-Token` with your API key.

Get details populated in the patient’s profile. This will return any information that was updated by the patient user after creating new account. If user has not updated any information, only the name and email address will be available in the response.

### HTTP Request

`GET
http://localhost:8080/DoctorOnDemand/api/patient/user/{PatientID}
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
{PatientID} | Pass this PatientID in the URL| String | Required

### Response

Parameter | Description | Type
--------- | ----------- | ----
ID | user id# | Integer | 
Email ID | User’s Email ID  | String
preferredPharmacy[{}] | Pharmacy Details | String
profileImagePath | Profile photo | String
About Me :[{}] | User details | String
Contact Info:[{}] | Contact person Info| String
Patient Info :[{}] | Patient info | String
FamilyMembers:[{}] | All family member details including each member's lifestyle, medical and social history, allergies | String
Doctor Info :[{}]| Doctor info. Deprecated | String
Specialities | Doctor Specialities. Deprecated| String
Report | Report. Deprecated | String
Role | Role id# and name. Always fixed id# and patient as role | String




`Authorization: X-Auth-Token`

<aside class="notice">
You must replace <code>X-Auth-Token</code> with your personal API key.
</aside>


## Update Patient Profile

```shell
curl -i -H "Content-Type:application/json" -H "X-Auth-Token:patientuser1@eyecarelive.com:patient:1561784861568:d5171513ed94a5fafb354f6f8688b751" -X PUT "https://dev.api.cooldoctors.io:8443/DoctorOnDemand/api/patient/user/profile" -d '{"id":"5ceed13cf893f45b5812b8e1","email":"patientuser1@eyecarelive.com","pharmacyName":null,"pharmacyAddress":null,"aboutMe":{"id":"5ceed13cf893f45b5812b8de","firstName":"Demo","lastName":"User","birthDate":null,"address":"","city":"","country":"","pincode":"","gender":null,"languagesSpeak":null,"additionalInfo":null,"state":"","lat":null,"lang":null},"contactInfo":null,"patientInfo":null,"doctorInfo":null,"role":{"id":"551ad2a4e4b0b59ff0ccecc9","name":"patient"},"timezone":{"id":"55f283b4e4b029528c27d0c5","timezone":"Asia/Kolkata","displayName":"India Standard Time"},"createdAt":"2019-05-29 11:36 AM PDT","forgotPasswordToken":null,"familyMembers":null,"parentUser":null,"parentUserRelation":null,"password":null,"rating":null,"preferredPharmacies":null,"oldPassword":null,"loginStatus":"Online","stripeCustId":null,"profileImagePath":null,"isReferredDoctor":null,"randomtoken":"BThd5P","isEmailVerified":false,"preferredDoctors":null,"isAcceptTC":false,"insurenceCards":null,"notificationSettings":{"id":"5ceed13cf893f45b5812b8df","email":true,"push":true,"sms":true,"sendReminderForMedicine":true,"addTestreport":true,"sentMessage":true,"addTreatmentPlan":true,"sendReminderForEyeTest":true},"clinics":null,"passCode":null,"emrId":null,"ssnId":null,"clinicInfo":null,"ref":null,"docOrg":null,"doctorsOrg":null,"twilioAccessToken":null,"bucket":null,"repoSub":false,"badge":null,"preferredEclClinics":null,"eclClinicId":null,"profileColor":null,"addedByCpm":false,"activated":true,"invited":false,"validated":true,"pilotDoc":false,"managedUser":false}'
```
> The above command returns JSON structured like this:

```json
{
	"id": "5a2c0a69e4b0e4fa266e0180",
	"email": "patientuser@cooldoctors.io",
	"pharmacyName": null,
	"pharmacyAddress": null,
	"profileImageId": null,
	"profileImageName": null,
	"aboutMe": {
		"id": "5a2c0a69e4b0e4fa266e017d",
		"firstName": "Patient",
		"lastName": "Name",
		"birthDate": null,
		"address": "Kallam Anji Reddy Campus, Banjara Hills",
		"city": "Hyderabad",
		"country": "India",
		"pincode": "500034",
		"gender": "Female",
		"languagesSpeak": null,
		"additionalInfo": null,
		"state": "Telangana"
	},
	"contactInfo": {
		"id": "5a2c0a69e4b0e4fa266e017f",
		"email": "patientuser@cooldoctors.io",
		"phone": "8806900740",
		"smsNotification": false,
		"countryCode": null,
		"country": null,
		"emlNt": false
	},
	"patientInfo": {
		"id": "5a2e1e23e4b0e4fa266e0805",
		"lifeStyle": {
			"id": "5a2e1e23e4b0e4fa266e0803",
			"medication": "Test",
			"alcoholUse": "yes",
			"allergiesToMedication": "Testing",
			"alcoholDrinksPerWeek": "Do not Drink",
			"medicalCondition": "Cancer",
			"allergies": "Pollen",
			"vitaminSupplements": "Test",
			"smoke": "1",
			"contactlenses": "Soft"
		},
		"familyHistory": {
			"id": "5a2e1e23e4b0e4fa266e0804",
			"description": null,
			"diseaseRelation": [{
				"conditions": "Cataract",
				"relationship": "Aunt"
			}]
		}
	},
	"doctorInfo": null,
	"role": {
		"id": "551ad2a4e4b0b59ff0ccecc9",
		"name": "patient"
	},
	"timezone": {
		"id": "55f283b4e4b029528c27d0c5",
		"timezone": "Asia/Kolkata",
		"displayName": "India Standard Time"
	},
	"createdAt": "2017-12-09 08:08 AM PST",
	"forgotPasswordToken": null,
	"familyMembers": [{
		"id": "5a2c1827e4b0e4fa266e018f",
		"email": "ESa6zdCf@eyecarelive.com",
		"pharmacyName": null,
		"pharmacyAddress": null,
		"profileImageId": "5a2c31a9e4b0e4fa266e01bf",
		"profileImageName": "0-cus-d1-b928632e6fef67a90ca8ecd0121882bb.jpg",
		"aboutMe": {
			"id": "5a2c1827e4b0e4fa266e018d",
			"firstName": "neet",
			"lastName": "yadav",
			"birthDate": null,
			"address": "Pune",
			"city": "Pune",
			"country": "india",
			"pincode": "411039",
			"gender": "male",
			"languagesSpeak": null,
			"additionalInfo": null,
			"state": "MH"
		},
		"contactInfo": {
			"id": "5a2c1827e4b0e4fa266e018e",
			"email": "Neet@gmail.com",
			"phone": "8055802119",
			"smsNotification": false,
			"countryCode": null,
			"country": null,
			"emlNt": false
		},
		"patientInfo": null,
		"doctorInfo": null,
		"role": {
			"id": "551ad2a4e4b0b59ff0ccecc9",
			"name": "patient"
		},
		"timezone": null,
		"createdAt": "2017-12-09 09:06 AM PST",
		"forgotPasswordToken": null,
		"familyMembers": null,
		"parentUser": null,
		"parentUserRelation": "brother",
		"password": null,
		"rating": null,
		"preferredPharmacy": null,
		"kandyUserName": null,
		"kandyUserPassword": null,
		"kandyFullUserId": null,
		"oldPassword": null,
		"loginStatus": null,
		"stripeCustId": null,
		"profileImagePath": null,
		"isReferredDoctor": null,
		"randomtoken": null,
		"isEmailVerified": false,
		"doctorsGroups": null,
		"preferredDoctors": null,
		"isAcceptTC": false,
		"insurenceCards": null,
		"notificationSettings": null,
		"clinics": null,
		"passCode": null,
		"emrId": null,
		"ssnId": null,
		"clinicInfo": null,
		"ref": null,
		"docOrg": null,
		"doctorsOrg": null,
		"twilioAccessToken": null,
		"invited": false,
		"validated": true,
		"activated": true,
		"managedUser": true,
		"addedByCpm": false,
		"pilotDoc": false
	}],
	"parentUser": null,
	"parentUserRelation": null,
	"password": null,
	"rating": null,
	"preferredPharmacy": [{
		"id": "5a2c2efee4b0e4fa266e01b4",
		"name": "Mediplus store",
		"address": "hinjewadi phase-1",
		"email": "niteshy2391@gmail.com",
		"city": "pune",
		"state": "Maharashtra",
		"country": null,
		"zipCode": "411007",
		"phoneNumber": "9423505079",
		"validated": false
	}],
	"kandyUserName": null,
	"kandyUserPassword": null,
	"kandyFullUserId": null,
	"oldPassword": null,
	"loginStatus": "Online",
	"stripeCustId": null,
	"profileImagePath": "https://api.endpoint.eyecarelive/PRDIMAGE/patient/5a2c0a69e4b0e4fa266e0180/ProfileImage/dashboard2.png",
	"isReferredDoctor": null,
	"randomtoken": "5Ys5Ad",
	"isEmailVerified": false,
	"doctorsGroups": null,
	"preferredDoctors": [],
	"isAcceptTC": false,
	"insurenceCards": null,
	"notificationSettings": {
		"id": "5a2c0a69e4b0e4fa266e017e",
		"addTestreport": true,
		"addTreatmentPlan": true,
		"sendReminderForEyeTest": true,
		"sendReminderForMedicine": true,
		"sentMessage": true
	},
	"clinics": null,
	"passCode": null,
	"emrId": null,
	"ssnId": null,
	"clinicInfo": null,
	"ref": null,
	"docOrg": null,
	"doctorsOrg": null,
	"twilioAccessToken": null,
	"invited": false,
	"validated": true,
	"activated": true,
	"managedUser": false,
	"addedByCpm": false,
	"pilotDoc": false
}
```

> Make sure to replace `X-Auth-Token` with your API key.

selectively update information in patient’s profile. This may be useful when updating insurance or payment information, updating address or phone numbers or preferred pharmacy changes.

### HTTP Request

`POST
http://localhost:8080/DoctorOnDemand/api/patient/user/profile
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
FirstName | User’s First Name | String | Required
LastName | User’s Last Name | String | Required
Address | User’s Address | String | Optional
City | City | String | Optional
Country | Country | String | Optional
BirthDate | Date of Birth (MM/DD/YYYY) | String | Optional
Pincode | Zip code | Integer | Optional
Gender | Gender (M,F) | String | Optional
 | **Role** | |
ID | Role (ID) Always use “551ad2a4e4b0b59ff0ccecc9” | Integer | Required
Name | Role Name Always Use “patient” | String | Required
 | **Contact Info** |  |
Email | Contact Email Address | String | Optional
Phone | Contact Number | Integer | Optional


### Response

Parameter | Description | Type
--------- | ----------- | ----
ID | user id# | Integer | 
Email ID | User’s Email ID  | String
preferredPharmacy[{}] | Pharmacy Details | String
profileImagePath | Profile photo | String
About Me :[{}] | User details | String
Contact Info:[{}] | Contact person Info| String
Patient Info :[{}] | Patient info | String
FamilyMembers:[{}] | All family member details including each member's lifestyle, medical and social history, allergies | String
Doctor Info :[{}]| Doctor info. Deprecated | String
Specialities | Doctor Specialities. Deprecated| String
Report | Report. Deprecated | String
Role | Role id# and name. Always fixed id# and patient as role | String




`Authorization: X-Auth-Token`

<aside class="notice">
You must replace <code>X-Auth-Token</code> with your personal API key.
</aside>



## Add User's Profile Photo

```shell
curl -H "X-Auth-Token:patientuser1@eyecarelive.com:patient:1561784861568:d5171513ed94a5fafb354f6f8688b751" -H "Content-Type:multipart/form-data" "https://dev.api.cooldoctors.io:8443/DoctorOnDemand/api/patient/user/profileImageFromFile" -X POST -F file=@/Users/cupertino/Downloads/dashboard2.png

```
> The above command returns JSON structured like this:

```json
{
	"success": true
}
```

> Make sure to replace `X-Auth-Token` with your API key.

Add User’s profile photo. User can upload photo from the app.

### HTTP Request

`POST
http://localhost:8080/DoctorOnDemand/api/patient/user/profileImageFromFile
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
profileImageFromFile | Path to the local file for profile photo | String | Required



### Response

Parameter | Description | Type
--------- | ----------- | ----
“Ok” | ‘Ok’ means this is successfully updated | String 



`Authorization: X-Auth-Token`

<aside class="notice">
You must replace <code>X-Auth-Token</code> with your personal API key.
</aside>


## Add patient's Preferred Pharmacy 

```shell
curl -i -H "Content-Type: application/json" -H "X-Auth-Token:patientuser1@eyecarelive.com:patient:1561784861568:d5171513ed94a5fafb354f6f8688b751" "https://dev.api.cooldoctors.io:8443/DoctorOnDemand/api/patient/pharmacy" -X POST -d '{"email": "niteshy2391@gmail.com","name": "Mediplus store","address":"hinjewadi phase-1","city": "pune","state": "Maharashtra","zipCode": "411007","phoneNumber": "9423505079"}'

```
> The above command returns JSON structured like this:

```json
{
  "id": "5ceed13cf893f45b5812b8e1",
  "email": "patientuser1@eyecarelive.com",
  "pharmacyName": null,
  "pharmacyAddress": null,
  "aboutMe": {
    "id": "5ceed13cf893f45b5812b8de",
    "firstName": "Demo",
    "lastName": "User",
    "birthDate": "",
    "address": "",
    "city": "",
    "country": "",
    "pincode": "",
    "gender": null,
    "languagesSpeak": null,
    "additionalInfo": null,
    "state": "",
    "lat": null,
    "lang": null
  },
  "contactInfo": null,
  "patientInfo": null,
  "doctorInfo": null,
  "role": {
    "id": "551ad2a4e4b0b59ff0ccecc9",
    "name": "patient"
  },
  "timezone": {
    "id": "55f283b4e4b029528c27d0c5",
    "timezone": "Asia/Kolkata",
    "displayName": "India Standard Time"
  },
  "createdAt": "2019-05-29 11:36 AM PDT",
  "forgotPasswordToken": null,
  "familyMembers": [
    {
      "id": "5cef956ef893f467ffa9ffcc",
      "email": "ddJdgVqM@eyecarelive.com",
      "pharmacyName": null,
      "pharmacyAddress": null,
      "aboutMe": {
        "id": "5cef956ef893f467ffa9ffc9",
        "firstName": "Slate",
        "lastName": "Member",
        "birthDate": "",
        "address": "qbNrHbKolNuq9+DQCMrbNw==",
        "city": "28L8jdmZdw/TOE19cYNfyg==",
        "country": "eGcNxOZVnF4jlkABhqaIAQ==",
        "pincode": "Zf6QZAhj9x3iULdEWv9pfA==",
        "gender": "male",
        "languagesSpeak": null,
        "additionalInfo": null,
        "state": "wPCNRzWVjd+MXrn0+dB4Cg==",
        "lat": null,
        "lang": null
      },
      "contactInfo": {
        "id": "5cef956ef893f467ffa9ffca",
        "email": "patientuser1@eyecarelive.com",
        "phone": "X025s2zeUri6K/6HA21+UA==",
        "smsNotification": false,
        "countryCode": null,
        "country": null,
        "emlNt": false
      },
      "patientInfo": null,
      "doctorInfo": null,
      "role": {
        "id": "551ad2a4e4b0b59ff0ccecc9",
        "name": "patient"
      },
      "timezone": null,
      "createdAt": "2019-05-30 01:33 AM PDT",
      "forgotPasswordToken": null,
      "familyMembers": null,
      "parentUser": null,
      "parentUserRelation": "brother",
      "password": null,
      "rating": null,
      "preferredPharmacies": null,
      "oldPassword": null,
      "loginStatus": null,
      "stripeCustId": null,
      "profileImagePath": null,
      "isReferredDoctor": null,
      "randomtoken": null,
      "isEmailVerified": false,
      "preferredDoctors": null,
      "isAcceptTC": false,
      "insurenceCards": null,
      "notificationSettings": null,
      "clinics": null,
      "passCode": null,
      "emrId": null,
      "ssnId": null,
      "clinicInfo": null,
      "ref": null,
      "docOrg": null,
      "doctorsOrg": null,
      "twilioAccessToken": null,
      "bucket": null,
      "repoSub": false,
      "badge": null,
      "preferredEclClinics": null,
      "eclClinicId": null,
      "profileColor": null,
      "addedByCpm": false,
      "activated": true,
      "invited": false,
      "validated": true,
      "pilotDoc": false,
      "managedUser": true
    }
  ],
  "parentUser": null,
  "parentUserRelation": null,
  "password": null,
  "rating": null,
  "preferredPharmacies": [
    {
      "id": "5cefff05f893f4052b1271ec",
      "name": "Mediplus store",
      "address": "hinjewadi phase-1",
      "email": "niteshy2391@gmail.com",
      "city": "pune",
      "state": "Maharashtra",
      "country": null,
      "zipCode": "411007",
      "phoneNumber": "9423505079",
      "validated": false
    }
  ],
  "oldPassword": null,
  "loginStatus": "Online",
  "stripeCustId": null,
  "profileImagePath": null,
  "isReferredDoctor": null,
  "randomtoken": "BThd5P",
  "isEmailVerified": false,
  "preferredDoctors": [
    "56fb7614e4b0d3123cea4925"
  ],
  "isAcceptTC": false,
  "insurenceCards": null,
  "notificationSettings": {
    "id": "5ceed13cf893f45b5812b8df",
    "push": true,
    "sms": true,
    "email": true,
    "sendReminderForMedicine": true,
    "addTestreport": true,
    "sentMessage": true,
    "addTreatmentPlan": true,
    "sendReminderForEyeTest": true
  },
  "clinics": null,
  "passCode": null,
  "emrId": null,
  "ssnId": null,
  "clinicInfo": null,
  "ref": null,
  "docOrg": null,
  "doctorsOrg": null,
  "twilioAccessToken": null,
  "bucket": null,
  "repoSub": false,
  "badge": null,
  "preferredEclClinics": null,
  "eclClinicId": null,
  "profileColor": null,
  "addedByCpm": false,
  "activated": true,
  "invited": false,
  "validated": true,
  "pilotDoc": false,
  "managedUser": false
}```

> Make sure to replace `X-Auth-Token` with your API key.

Add pharmacy information to the user’s profile. This is visible to the doctors.

### HTTP Request

`POST
http://localhost:8080/DoctorOnDemand/api/patient/pharmacy
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
Email Address | User's Email Address | String | Required
Pharmacy Name | Pharmacy name | String | Required
pharmacy Address | Pharmacy address| String | Required
ContactInfo | Pharmacy Phone  number | String | Required




### Response

Parameter | Description | Type
--------- | ----------- | ----
ID | user id# | Integer | 
Email ID | User’s Email ID  | String
preferredPharmacy[{}] | Pharmacy Details | String
profileImagePath | Profile photo | String
About Me :[{}] | User details | String
Contact Info:[{}] | Contact person Info| String
Patient Info :[{}] | Patient info | String
FamilyMembers:[{}] | All family member details including each member's lifestyle, medical and social history, allergies | String
Doctor Info :[{}]| Doctor info. Deprecated | String
Specialities | Doctor Specialities. Deprecated| String
Report | Report. Deprecated | String
Role | Role id# and name. Always fixed id# and patient as role | String


`Authorization: X-Auth-Token`

<aside class="notice">
You must replace <code>X-Auth-Token</code> with your personal API key.
</aside>

## Delete Patient's Preferred pharmacy 

```shell
curl -i -H "Content-Type: application/json" -H "X-Auth-Token:patientuser1@eyecarelive.com:patient:1561784861568:d5171513ed94a5fafb354f6f8688b751" -X DELETE  "https://dev.api.cooldoctors.io:8443/DoctorOnDemand/api/patient/pharmacy/5cefff05f893f4052b1271ec"
```
> The above command returns JSON structured like this:

```json
{
200 ok
}
```

> Make sure to replace `X-Auth-Token` with your API key.

Delete the current preferred pharmacy in user’s profile.

### HTTP Request

`DELETE
http://localhost:8080/DoctorOnDemand/api/patient/pharmacy/{pharmacyId}
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
Pass Pharmacy ID | Pharmacy id# | String | Required




### Response

Parameter | Description | Type
--------- | ----------- | ----
200ok | it means successfully delete | String 



`Authorization: X-Auth-Token`

<aside class="notice">
You must replace <code>X-Auth-Token</code> with your personal API key.
</aside>


## Add Insurance Info

```shell
### Get All Payers for adding insurance for card name

curl -i -H "Content-Type:application/json" -H "X-Auth-Token:patientuser1@eyecarelive.com:patient:1561784861568:d5171513ed94a5fafb354f6f8688b751" -X GET "https://dev.api.cooldoctors.io:8443/DoctorOnDemand/api/patient/eligible/getAllPayers"

### Add Insurance API with card images

curl -H "X-Auth-Token:patientuser1@eyecarelive.com:patient:1561784861568:d5171513ed94a5fafb354f6f8688b751a" -H "Content-Type:multipart/form-data" "https://dev.api.cooldoctors.io:8443/DoctorOnDemand/api/patient/user/insurencecard/Aetna60054/W220/604" -X POST -F file=@/Users/cupertino/Downloads/2_user.png -F file=@/Users/cupertino/Downloads/2_user.png
```
> The above command returns JSON structured like this:

```json
{
	"success": true
}
```

> Make sure to replace `X-Auth-Token` with your API key.

Add pharmacy information to the user’s profile. This is visible to the doctors.

### HTTP Request

`POST
http://localhost:8080/DoctorOnDemand/api/patient/pharmacy
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
{CardName} | Insurance card name | String | Required
{MemberID} | Member ID of insurance| String | Required
{PayerID} | PayerID of insurance| String | Required
-F file=@/FilePath | Add photo after @| String | Required



### Response

Parameter | Description | Type
--------- | ----------- | ----
success | True Or False | String 


`Authorization: X-Auth-Token`

<aside class="notice">
You must replace <code>X-Auth-Token</code> with your personal API key.
</aside>

## Delete Insurance Info

```shell

### Delete insurance information from the user’s profile

#iOS Api

curl -i -H "Content-Type: application/json" -H "X-Auth-Token:patientuser1@eyecarelive.com:patient:1561784861568:d5171513ed94a5fafb354f6f8688b751" -X DELETE  "https://dev.api.cooldoctors.io:8443/DoctorOnDemand/api/patient/user/insurencecard/1512974005984"

```

```shell

#Android Api

curl -i -H "Content-Type: application/json" -H "X-Auth-Token:patientuser1@eyecarelive.com:patient:1561784861568:d5171513ed94a5fafb354f6f8688b751" -X POST "https://dev.api.cooldoctors.io:8443/DoctorOnDemand/api/patient/user/insurencecard/delete/1512974005984"

```
> The above command returns JSON structured like this:

```json
{
	"success": true
}
```

> Make sure to replace `X-Auth-Token` with your API key.

Delete insuranceCard having two API’s for one iOS and one for android. 

### HTTP Request

`POST
http://localhost:8080/DoctorOnDemand/api/patient/insurencecard/{AddInsuranceFiles_ID}"
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
iOS Api{AddInsuranceFiles_ID} | This API only need to pass file ID of added insurance card | String | Required



### Response

Parameter | Description | Type
--------- | ----------- | ----
success | True Or False | String 

### HTTP Request

`POST
http://localhost:8080/DoctorOnDemand/api/patient/insurencecard/delete/{AddInsuranceFiles_ID}"
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
Android API {AddInsuranceFiles_ID} | This API only need to pass file ID of added insurance card | String | Required


### Response

Parameter | Description | Type
--------- | ----------- | ----
success | True Or False | String 


`Authorization: X-Auth-Token`

<aside class="notice">
You must replace <code>X-Auth-Token</code> with your personal API key.
</aside>


## Add Family Member

```shell

curl -i -H "Content-Type: application/json" -H "X-Auth-Token:patientuser1@eyecarelive.com:patient:1561784861568:d5171513ed94a5fafb354f6f8688b751" "https://dev.api.cooldoctors.io:8443/DoctorOnDemand/api/patient/user/familyMember" -X POST -d '{"parentUserRelation":"brother","aboutMe":{"firstName":"Slate","lastName":"Member","address":"America", "city":"Cupertino","state":"CA","country":"USA","pincode":"95014","gender":"male"},"role" :{"id": "551ad2a4e4b0b59ff0ccecc9","name": "patient"},"contactInfo":{"email":"patientuser1@eyecarelive.com","phone":"0000000000"},"timezone":{"id": "551ad2a4e4b0b59ff0ccecc9","timezone": "Asia/Kolkata","displayName": null}}'
```
> The above command returns JSON structured like this:

```json
{
  "id": "5cef956ef893f467ffa9ffcc",
  "email": "ddJdgVqM@eyecarelive.com",
  "pharmacyName": null,
  "pharmacyAddress": null,
  "aboutMe": {
    "id": "5cef956ef893f467ffa9ffc9",
    "firstName": "Slate",
    "lastName": "Member",
    "birthDate": "",
    "address": "qbNrHbKolNuq9+DQCMrbNw==",
    "city": "28L8jdmZdw/TOE19cYNfyg==",
    "country": "eGcNxOZVnF4jlkABhqaIAQ==",
    "pincode": "Zf6QZAhj9x3iULdEWv9pfA==",
    "gender": "male",
    "languagesSpeak": null,
    "additionalInfo": null,
    "state": "wPCNRzWVjd+MXrn0+dB4Cg==",
    "lat": null,
    "lang": null
  },
  "contactInfo": {
    "id": "5cef956ef893f467ffa9ffca",
    "email": "patientuser1@eyecarelive.com",
    "phone": "X025s2zeUri6K/6HA21+UA==",
    "smsNotification": false,
    "countryCode": null,
    "country": null,
    "emlNt": false
  },
  "patientInfo": null,
  "doctorInfo": null,
  "role": {
    "id": "551ad2a4e4b0b59ff0ccecc9",
    "name": "patient"
  },
  "timezone": {
    "id": "551ad2a4e4b0b59ff0ccecc9",
    "timezone": "Asia/Kolkata",
    "displayName": null
  },
  "createdAt": "2019-05-30 01:33 AM PDT",
  "forgotPasswordToken": null,
  "familyMembers": null,
  "parentUser": null,
  "parentUserRelation": "brother",
  "password": null,
  "rating": null,
  "preferredPharmacies": null,
  "oldPassword": null,
  "loginStatus": null,
  "stripeCustId": null,
  "profileImagePath": null,
  "isReferredDoctor": null,
  "randomtoken": null,
  "isEmailVerified": false,
  "preferredDoctors": null,
  "isAcceptTC": false,
  "insurenceCards": null,
  "notificationSettings": null,
  "clinics": null,
  "passCode": null,
  "emrId": null,
  "ssnId": null,
  "clinicInfo": null,
  "ref": null,
  "docOrg": null,
  "doctorsOrg": null,
  "twilioAccessToken": null,
  "bucket": null,
  "repoSub": false,
  "badge": null,
  "preferredEclClinics": null,
  "eclClinicId": null,
  "profileColor": null,
  "activated": true,
  "invited": false,
  "validated": true,
  "pilotDoc": false,
  "managedUser": true,
  "addedByCpm": false
}

```

> Make sure to replace `X-Auth-Token` with your API key.

Add a family member who could be the patient.


### HTTP Request

`POST
http://localhost:8080/DoctorOnDemand/api/patient/user/familyMember
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
Parent User Relation |  user’s relationship to the primary user | String | Required
     | **About Family Member** |   |
First Name | Name of the family member| String | Required
Last Name | Last name of the family member | String | Required
Address | Address of the family member | String | Required
City | City of the family member | Required
Country | Country of the family member | String | Required
Pincode | zincode of the family member | String | Required
Gender | Gender(M,F) of the family member| String | Required
      | **Family Member Contact Info** |   |
Email | External email address for Contact Info | String | Required
Phone | Contact info | String | Required



### Response

Parameter | Description | Type
--------- | ----------- | ----
ID | Database ID of family member | String 
Email | Generated email address from server | String 
aboutMe[{}] | Family member information | String 
contactInfo[{}] | Family member Contact info | String 
Role | Role (ID) Always use “551ad2a4e4b0b59ff0ccecc9” | String 
Deprecated Value | Ignore other parameters | String 



`Authorization: X-Auth-Token`

<aside class="notice">
You must replace <code>X-Auth-Token</code> with your personal API key.
</aside>


## Update Family Member Profile

```shell
 curl -i -H "Content-Type: application/json" -H "X-Auth-Token:patientuser1@eyecarelive.com:patient:1561784861568:d5171513ed94a5fafb354f6f8688b751" "https://dev.api.cooldoctors.io:8443/DoctorOnDemand/api/patient/user/familyMember" -X PUT -d '[{"id":"5a2c1827e4b0e4fa266e018f","email":"ESa6zdCf@eyecarelive.com","pharmacyName":null,"pharmacyAddress":null,"profileImageId":null,"profileImageName":null,"aboutMe":{"id":"5a2c1827e4b0e4fa266e018d","firstName":"neet","lastName":"yadav","birthDate":null,"address":"Pune","city":"Pune","country":"india","pincode":"411039","gender":"male","languagesSpeak":null,"additionalInfo":null,"state":"MH"},"contactInfo":{"id":"5a2c1827e4b0e4fa266e018e","email":"Neet@gmail.com","phone":"8055802119","smsNotification":false,"countryCode":null,"country":null,"emlNt":false},"patientInfo":null,"doctorInfo":null,"role":{"id":"551ad2a4e4b0b59ff0ccecc9","name":"patient"},"timezone":null,"createdAt":"2017-12-09 09:06 AM PST","forgotPasswordToken":null,"familyMembers":null,"parentUser":null,"parentUserRelation":"brother","password":null,"rating":null,"preferredPharmacies":null,"kandyUserName":null,"kandyUserPassword":null,"kandyFullUserId":null,"oldPassword":null,"loginStatus":null,"stripeCustId":null,"profileImagePath":null,"isReferredDoctor":null,"randomtoken":null,"isEmailVerified":false,"doctorsGroups":null,"preferredDoctors":null,"isAcceptTC":false,"insurenceCards":null,"notificationSettings":null,"clinics":null,"passCode":null,"emrId":null,"ssnId":null,"clinicInfo":null,"ref":null,"docOrg":null,"doctorsOrg":null,"twilioAccessToken":null,"invited":false,"validated":true,"activated":true,"managedUser":true,"addedByCpm":false,"pilotDoc":false}]'

```
> The above command returns JSON structured like this:

```json
{
	"success": true
}
```

> Make sure to replace `X-Auth-Token` with your API key.

Update family member’s profile data.


### HTTP Request

`PUT
http://localhost:8080/DoctorOnDemand/api/patient/user/familyMember
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
Email Id |  user’s Email Id | String | Required
Password | Password | String | Required
     | **About Family Member** |   |
First Name | Name of the family member| String | Required
Last Name | Last name of the family member | String | Required
Address | Address of the family member | String | Required
City | City of the family member | Required
Country | Country of the family member | String | Required
Pincode | zincode of the family member | String | Required
Gender | Gender(M,F) of the family member| String | Required
Role | Role | String | Required
      | **Family Member Contact Info** |   |
Email | External email address for Contact Info | String | Required
Phone | Contact info | String | Required
      | **Time Zone** |   |
ID | ID of time zone | Integer | Required
Timezone | Timezone | String | Required
Display Name | Display Name | String | Required
CreatedAt:[{}] | Created At | String | Required


### Response

Parameter | Description | Type
--------- | ----------- | ----
Success | True OR False | String 




`Authorization: X-Auth-Token`

<aside class="notice">
You must replace <code>X-Auth-Token</code> with your personal API key.
</aside>


## Add Family member profile photo

```shell
curl -H "X-Auth-Token:patientuser1@eyecarelive.com:patient:1561784861568:d5171513ed94a5fafb354f6f8688b751" -H "Content-Type:multipart/form-data" "https://dev.api.cooldoctors.io:8443/DoctorOnDemand/api/patient/user/familyMember/file/5a2c1827e4b0e4fa266e018f" -X POST -F file=@/Users/cupertino/Downloads/dashboard2.png


```
> The above command returns JSON structured like this:

```json
{
	200 OK
}
```

> Make sure to replace `X-Auth-Token` with your API key.

Allows user to upload photo of family member

### HTTP Request

`POST
http://localhost:8080/familymember/profileImageFromFile/{familyMemberUserId}
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
file=@/Path| In that give the path| String | Required




### Response

Parameter | Description | Type
--------- | ----------- | ----
200 | Ok| String 


`Authorization: X-Auth-Token`

<aside class="notice">
You must replace <code>X-Auth-Token</code> with your personal API key.
</aside>

## Delete family Member

```shell
 curl -i -H "Content-Type: application/json" -H "X-Auth-Token:patientuser1@eyecarelive.com:patient:1561784861568:d5171513ed94a5fafb354f6f8688b751" "https://dev.api.cooldoctors.io:8443/DoctorOnDemand/api/patient/user/familyMember" -X DELETE -d '{"id":"5a2c19d0e4b0e4fa266e0195"}'

```
> The above command returns JSON structured like this:

```json
{
	"success": true
}
```

> Make sure to replace `X-Auth-Token` with your API key.

Remove family member from the main user’s profile


### HTTP Request

`DELETE
http://localhost:8080/DoctorOnDemand/api/patient/user/familyMember
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
ID |  Family member user id#| String | Required
   


### Response

Parameter | Description | Type
--------- | ----------- | ----
Success | True OR False | String 




`Authorization: X-Auth-Token`

<aside class="notice">
You must replace <code>X-Auth-Token</code> with your personal API key.
</aside>

## Get list of all family members

```shell

curl -i -H "Content-Type: application/json" -H "X-Auth-Token:patientuser1@eyecarelive.com:patient:1561784861568:d5171513ed94a5fafb354f6f8688b751" -X GET "https://dev.api.cooldoctors.io:8443/DoctorOnDemand/api/patient/user/familyMember"

```
> The above command returns JSON structured like this:

```json
[
  {
    "id": "5a2c1827e4b0e4fa266e018f",
    "email": "ESa6zdCf@eyecarelive.com",
    "pharmacyName": null,
    "pharmacyAddress": null,
    "profileImageId": null,
    "profileImageName": null,
    "aboutMe": {
      "id": "5a2c1827e4b0e4fa266e018d",
      "firstName": "neet",
      "lastName": "yadav",
      "birthDate": null,
      "address": "Pune",
      "city": "Pune",
      "country": "india",
      "pincode": "411039",
      "gender": "male",
      "languagesSpeak": null,
      "additionalInfo": null,
      "state": "MH"
    },
    "contactInfo": {
      "id": "5a2c1827e4b0e4fa266e018e",
      "email": "Neet@gmail.com",
      "phone": "8055802119",
      "smsNotification": false,
      "countryCode": null,
      "country": null,
      "emlNt": false
    },
    "patientInfo": null,
    "doctorInfo": null,
    "role": {
      "id": "551ad2a4e4b0b59ff0ccecc9",
      "name": "patient"
    },
    "timezone": null,
    "createdAt": "2017-12-09 09:06 AM PST",
    "forgotPasswordToken": null,
    "familyMembers": null,
    "parentUser": null,
    "parentUserRelation": "brother",
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
    "randomtoken": null,
    "isEmailVerified": false,
    "doctorsGroups": null,
    "preferredDoctors": null,
    "isAcceptTC": false,
    "insurenceCards": null,
    "notificationSettings": null,
    "clinics": null,
    "passCode": null,
    "emrId": null,
    "ssnId": null,
    "clinicInfo": null,
    "ref": null,
    "docOrg": null,
    "doctorsOrg": null,
    "twilioAccessToken": null,
    "invited": false,
    "validated": true,
    "activated": true,
    "managedUser": true,
    "addedByCpm": false,
    "pilotDoc": false
  }
]

```

> Make sure to replace `X-Auth-Token` with your API key.

Add a family member who could be the patient.


### HTTP Request

`GET
http://localhost:8080/DoctorOnDemand/api/patient/user/familyMember
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
No parameter need to pass |  Use the URL for get the family members | String | Required



### Response

Parameter | Description | Type
--------- | ----------- | ----
ID | Database ID of family member | String 
Email | Generated email address from server | String 
aboutMe[{}] | Family member information | String 
contactInfo[{}] | Family member Contact info | String 
Role | Role (ID) Always use “551ad2a4e4b0b59ff0ccecc9” | String 
Deprecated Value | Ignore other parameters | String 



`Authorization: X-Auth-Token`

<aside class="notice">
You must replace <code>X-Auth-Token</code> with your personal API key.
</aside>



## List Doctors By State & Country

```shell

curl -i  -H "Content-Type: application/json" -H "X-Auth-Token:patientuser1@eyecarelive.com:patient:1561784861568:d5171513ed94a5fafb354f6f8688b751" -X GET "https://dev.api.cooldoctors.io:8443/DoctorOnDemand/api/patient/user/doctorsbystate/NY/US"

```
> The above command returns JSON structured like this:

```json
[
  {
    "id": "5c8759f9f893f4062b10e8db",
    "email": "daniel.rosenblum@eyecarelive.com",
    "pharmacyName": null,
    "pharmacyAddress": null,
    "aboutMe": {
      "id": "5c8759f9f893f4062b10e8d8",
      "firstName": "Daniel",
      "lastName": "Richardson",
      "birthDate": "",
      "address": "Lk40VwUOV8MaLCfyuWLKlPaU2MQt33a6zcwXz5a7oBg=",
      "city": "3bsDuinQsrMDcmlBUPjWgA==",
      "country": "Pv8JTz1Cn88WAkRD4ySd5Q==",
      "pincode": "GQf13rmyGwgGfplBGJ4N/g==",
      "gender": "male",
      "languagesSpeak": [
        "English",
        "",
        ""
      ],
      "additionalInfo": null,
      "state": "5OV/dsqTkfF/XjREpxfJKw==",
      "lat": null,
      "lang": null
    },
    "contactInfo": {
      "id": "5c8759f9f893f4062b10e8d9",
      "email": "daniel.rosenblum@eyecarelive.com",
      "phone": "0eFH0lApjmZjUVFFlMWg1A==",
      "smsNotification": false,
      "countryCode": null,
      "country": null,
      "emlNt": true
    },
    "patientInfo": null,
    "doctorInfo": {
      "id": "5c875caaf893f4302afa2e81",
      "educationList": null,
      "hospitalAttachedWithList": null,
      "awardsReceivedList": null,
      "specialities": [
        {
          "id": "55b78065e4b0b393bf91678f",
          "name": "general physician",
          "questionnaire": null
        }
      ],
      "licencedState": [
        {
          "id": "5665a2cb9a87399fa0b9ba37",
          "state": "CA"
        },
        {
          "id": "5665a2cb9a87399fa0b9ba47",
          "state": "MD"
        },
        {
          "id": "5665a2cc9a87399fa0b9ba53",
          "state": "NY"
        }
      ],
      "registrationNumber": "1231313131",
      "whyCoolDoctors": null,
      "bio": null,
      "profession": "Optometrist",
      "availabilityTimeZone": "America/New_York",
      "npi": null,
      "availabilityStatus": null,
      "availabilityMsg": null,
      "passwardChanged": false,
      "consultationFees": null,
      "paymentOptions": null,
      "appCountEmail": false,
      "monthlyCharge": false
    },
    "role": {
      "id": "551ad2ffe4b0b59ff0cceccb",
      "name": "doctor"
    },
    "timezone": {
      "id": "55f283b4e4b029528c27d0c5",
      "timezone": "Asia/Kolkata",
      "displayName": "India Standard Time"
    },
    "createdAt": "2019-03-12 12:04 AM PDT",
    "forgotPasswordToken": null,
    "familyMembers": null,
    "parentUser": null,
    "parentUserRelation": null,
    "password": null,
    "rating": null,
    "preferredPharmacies": null,
    "oldPassword": null,
    "loginStatus": "Online",
    "stripeCustId": null,
    "profileImagePath": null,
    "isReferredDoctor": null,
    "randomtoken": "hgpAY3",
    "isEmailVerified": false,
    "preferredDoctors": null,
    "isAcceptTC": true,
    "insurenceCards": null,
    "notificationSettings": null,
    "clinics": null,
    "passCode": null,
    "emrId": null,
    "ssnId": null,
    "clinicInfo": null,
    "ref": null,
    "docOrg": null,
    "doctorsOrg": null,
    "twilioAccessToken": "eyJjdHkiOiJ0d2lsaW8tZnBhO3Y9MSIsInR5cCI6IkpXVCIsImFsZyI6IkhTMjU2In0.eyJpc3MiOiJTS2EyNzAzZTE0MThmNTY2MDA1NjI3YWJiYTE2ZGI4MmNlIiwiZXhwIjoxNTU4NTcwODk4LCJncmFudHMiOnsiaWRlbnRpdHkiOiI1Yzg3NTlmOWY4OTNmNDA2MmIxMGU4ZGIiLCJ2aWRlbyI6eyJyb29tIjoiNWM4NzU5ZjlmODkzZjQwNjJiMTBlOGRiNWM4N2ZmZTJmODkzZjQzMDJhZWIxMzM4In19LCJqdGkiOiJTS2EyNzAzZTE0MThmNTY2MDA1NjI3YWJiYTE2ZGI4MmNlLTE1NTg1NjcyOTYiLCJzdWIiOiJBQ2M5MGJmNjdhODk0YjA0YjA2NTdkMjJkN2FlOTQ5ZDk3In0.ia6FAQWw8vsoGpHRWU3YGNypWz-D2CnxWMAdCxv1Zqs",
    "invited": false,
    "validated": false,
    "activated": true,
    "managedUser": false,
    "addedByCpm": false,
    "pilotDoc": false,
    "bucket": null,
    "repoSub": false,
    "badge": null,
    "preferredEclClinics": null,
    "eclClinicId": null,
    "profileColor": null
  }
]
```

> Make sure to replace `X-Auth-Token` with your API key.



### HTTP Request

`POST
http://52.7.202.98:8080/DoctorOnDemand/api/patient/user/doctorsbystate/{state}/{country}
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
State |  State  | String | Required
Country | Country | String | Required


### Response

Parameter | Description | Type
--------- | ----------- | ----
ID | User's ID | String 
Email ID | User's Email ID | String
Pharmacy Name | Pharmacy Name | String 
Pharmacy Address | Pharmacy Address | String 
profileImageId | Profile Image Id | Integer
profileImageName | Profile Image Name | .jpg,etc.
aboutMe[{}] | Family member information | String 
contactInfo[{}] | Family member Contact info | String 
patientinfo[{}] | Patients Information | String 
doctorinfo[{}] | Doctors Information | String 
Specialities | Specialities Details | String
Report | Report | String
CreatedAt:[{}] | Created At | String
Role | Role | String 


`Authorization: X-Auth-Token`

<aside class="notice">
You must replace <code>X-Auth-Token</code> with your personal API key.
</aside>




