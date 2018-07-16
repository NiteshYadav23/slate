


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


## Add New Patient Information 

```shell
curl -i -H "Content-Type: application/json" -H "X-Auth-Token:patientuser@cooldoctors.io:patient:1515429239598:a0e476b75ffbacedd65e555b5304b222" "https://api.endpoint.eyecarelive.com/DoctorOnDemand/api/patient/patientinfo" -X POST -d '{"lifeStyle":{"smoke":"1","vitaminSupplements":"Test","allergies":"Pollen","alcoholDrinksPerWeek":"Do not Drink","medicalCondition":"Cancer","contactlenses":"Soft","medication":"Test","alcoholUse":"yes","allergiesToMedication":"Testing"},"familyHistory":{"diseaseRelation":[{"conditions":"Cataract","relationship":"Aunt"}]}}'

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

Add information to the patient’s profile. Patient’s full or partial profile may be created. Other than the name, date of birth, gender and email address, most of the information is optional but good to have for doctors.

### HTTP Request

`POST
http://localhost:8080/DoctorOnDemand/api/patient/patientinfo
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
Alcohol Use | Yes or No | String. Options Drinks per week (Do Not Drink, 1-6, 7-14, More than 14) | Optional
Medical Condition | Select values from list | "String Glaucoma","Cataracts","Macular Degeneration","Eye Injury","Retina Disease","Other Disease","Blindness","Strabismus","Amblyopia","Diabetes","Cancer","Heart Disease","Hypertension","High Cholesterol","Kidney Disease","Stroke","Other" | Optional
Allergies | Select value | String. Fish, Peanuts, Pollen, Other | Optional
Contact Lenses | Select value | String. Soft, Hard, Other | Optional
Smoke Use | Yes or No | String. (Yes/No)  | Optional
Medications | Yes or No | String Type | Optional
Allergic to Medications  | Yes or No| String Type | Optional
Vitamins or Supplements | Yes or No| String Type | Optional
Conditions:Relation | One or more Conditions: relationship pairs | String | Optional

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
FamilyMembers:[{}] | All family member details including each members lifestyle, medical and social history, allergies | String
Doctor Info :[{}]| Doctor info. Deprecated | String
Specialities | Doctor Specialities. Deprecated| String
Report | Report. Deprecated | String
Role | Role id# and name. Always fixed id# and patient as role | String




`Authorization: X-Auth-Token`

<aside class="notice">
You must replace <code>X-Auth-Token</code> with your personal API key.
</aside>


## Get Patient Profile 

```shell
curl -i -H "Content-Type:application/json" -H "X-Auth-Token:patientuser@cooldoctors.io:patient:1515429239598:a0e476b75ffbacedd65e555b5304b222" -X GET "https://api.endpoint.eyecarelive.com/DoctorOnDemand/api/patient/user/5a2c0a69e4b0e4fa266e0180"
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
    "email": "hiral@lvpei.org",
    "phone": "610-469-4012",
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
    "id": "55f283b4e4b029528c27d0c5",
    "timezone": "Asia/Kolkata",
    "displayName": "India Standard Time"
  },
  "createdAt": "2017-12-09 08:08 AM PST",
  "forgotPasswordToken": null,
  "familyMembers": null,
  "parentUser": null,
  "parentUserRelation": null,
  "password": null,
  "rating": null,
  "preferredPharmacy": null,
  "kandyUserName": null,
  "kandyUserPassword": null,
  "kandyFullUserId": null,
  "oldPassword": null,
  "loginStatus": "Online",
  "stripeCustId": null,
  "profileImagePath": null,
  "isReferredDoctor": null,
  "randomtoken": "5Ys5Ad",
  "isEmailVerified": false,
  "doctorsGroups": null,
  "preferredDoctors": null,
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
curl -i -H "Content-Type:application/json" -H "X-Auth-Token:patientuser@cooldoctors.io:patient:1515429239598:a0e476b75ffbacedd65e555b5304b222" -X PUT "https://api.endpoint.eyecarelive.com/DoctorOnDemand/api/patient/user/profile" -d '{"id":"5a2c0a69e4b0e4fa266e0180","email":"patientuser@cooldoctors.io","pharmacyName":null,"pharmacyAddress":null,"profileImageId":null,"profileImageName":null,"aboutMe":{"id":"5a2c0a69e4b0e4fa266e017d","firstName":"Patient","lastName":"Name","birthDate":null,"address":"Kallam Anji Reddy Campus, Banjara Hills","city":"Hyderabad","country":"India","pincode":"500034","gender":"Female","languagesSpeak":null,"additionalInfo":null,"state":"Telangana"},"contactInfo":{"id":"5a2c0a69e4b0e4fa266e017f","email":"patientuser@cooldoctors.io","phone":"8806900740","smsNotification":false,"countryCode":null,"country":null,"emlNt":false},"patientInfo":{"id":"5a2e1e23e4b0e4fa266e0805","lifeStyle":{"id":"5a2e1e23e4b0e4fa266e0803","medication":"Test","alcoholUse":"yes","allergiesToMedication":"Testing","alcoholDrinksPerWeek":"Do not Drink","medicalCondition":"Cancer","allergies":"Pollen","vitaminSupplements":"Test","smoke":"1","contactlenses":"Soft"},"familyHistory":{"id":"5a2e1e23e4b0e4fa266e0804","description":null,"diseaseRelation":[{"conditions":"Cataract","relationship":"Aunt"}]}},"doctorInfo":null,"role":{"id":"551ad2a4e4b0b59ff0ccecc9","name":"patient"},"timezone":{"id":"55f283b4e4b029528c27d0c5","timezone":"Asia/Kolkata","displayName":"India Standard Time"},"createdAt":"2017-12-09 08:08 AM PST","forgotPasswordToken":null,"familyMembers":[{"id":"5a2c1827e4b0e4fa266e018f","email":"ESa6zdCf@eyecarelive.com","pharmacyName":null,"pharmacyAddress":null,"profileImageId":"5a2c31a9e4b0e4fa266e01bf","profileImageName":"0-cus-d1-b928632e6fef67a90ca8ecd0121882bb.jpg","aboutMe":{"id":"5a2c1827e4b0e4fa266e018d","firstName":"neet","lastName":"yadav","birthDate":null,"address":"Pune","city":"Pune","country":"india","pincode":"411039","gender":"male","languagesSpeak":null,"additionalInfo":null,"state":"MH"},"contactInfo":{"id":"5a2c1827e4b0e4fa266e018e","email":"Neet@gmail.com","phone":"8055802119","smsNotification":false,"countryCode":null,"country":null,"emlNt":false},"patientInfo":null,"doctorInfo":null,"role":{"id":"551ad2a4e4b0b59ff0ccecc9","name":"patient"},"timezone":null,"createdAt":"2017-12-09 09:06 AM PST","forgotPasswordToken":null,"familyMembers":null,"parentUser":null,"parentUserRelation":"brother","password":null,"rating":null,"preferredPharmacy":null,"kandyUserName":null,"kandyUserPassword":null,"kandyFullUserId":null,"oldPassword":null,"loginStatus":null,"stripeCustId":null,"profileImagePath":null,"isReferredDoctor":null,"randomtoken":null,"isEmailVerified":false,"doctorsGroups":null,"preferredDoctors":null,"isAcceptTC":false,"insurenceCards":null,"notificationSettings":null,"clinics":null,"passCode":null,"emrId":null,"ssnId":null,"clinicInfo":null,"ref":null,"docOrg":null,"doctorsOrg":null,"twilioAccessToken":null,"invited":false,"validated":true,"activated":true,"managedUser":true,"addedByCpm":false,"pilotDoc":false}],"parentUser":null,"parentUserRelation":null,"password":null,"rating":null,"preferredPharmacy":[{"id":"5a2c2efee4b0e4fa266e01b4","name":"Mediplus store","address":"hinjewadi phase-1","email":"niteshy2391@gmail.com","city":"pune","state":"Maharashtra","country":null,"zipCode":"411007","phoneNumber":"9423505079","validated":false}],"kandyUserName":null,"kandyUserPassword":null,"kandyFullUserId":null,"oldPassword":null,"loginStatus":"Online","stripeCustId":null,"profileImagePath":"https://api.endpoint.eyecarelive/PRDIMAGE/patient/5a2c0a69e4b0e4fa266e0180/ProfileImage/dashboard2.png","isReferredDoctor":null,"randomtoken":"5Ys5Ad","isEmailVerified":false,"doctorsGroups":null,"preferredDoctors":[],"isAcceptTC":false,"insurenceCards":null,"notificationSettings":{"id":"5a2c0a69e4b0e4fa266e017e","addTestreport":true,"addTreatmentPlan":true,"sendReminderForEyeTest":true,"sendReminderForMedicine":true,"sentMessage":true},"clinics":null,"passCode":null,"emrId":null,"ssnId":null,"clinicInfo":null,"ref":null,"docOrg":null,"doctorsOrg":null,"twilioAccessToken":null,"invited":false,"validated":true,"activated":true,"managedUser":false,"addedByCpm":false,"pilotDoc":false}'
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
curl -H "X-Auth-Token:patientuser@cooldoctors.io:patient:1515429239598:a0e476b75ffbacedd65e555b5304b222" -H "Content-Type:multipart/form-data" "https://api.endpoint.eyecarelive.com/DoctorOnDemand/api/patient/user/profileImageFromFile" -X POST -F file=@/Users/cupertino/Downloads/dashboard2.png
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
Success | True OR False | String 



`Authorization: X-Auth-Token`

<aside class="notice">
You must replace <code>X-Auth-Token</code> with your personal API key.
</aside>


## Add patient's Preferred Pharmacy 

```shell
curl -i -H "Content-Type: application/json" -H "X-Auth-Token:patientuser@cooldoctors.io:patient:1515429239598:a0e476b75ffbacedd65e555b5304b222" "https://api.endpoint.eyecarelive.com/DoctorOnDemand/api/patient/pharmacy" -X POST -d '{"name": "Mediplus store","address":"hinjewadi phase-1","city": "pune","state": "Maharashtra","zipCode": "411007","phoneNumber": "9423505079"}'
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
	}, {
		"id": "5a2e22fce4b0e4fa266e09ec",
		"name": "Mediplus store",
		"address": "hinjewadi phase-1",
		"email": null,
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

Add pharmacy information to the user’s profile. This is visible to the doctors.

### HTTP Request

`POST
http://localhost:8080/DoctorOnDemand/api/patient/pharmacy
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
Pharmacy Name | Pharmacy name | String | Required
pharmacy Address | Pharmacy address| String | Required
city | Pharmacy Phone  number| String | Required
state | State of pharmacy| String | Required
zipCode | Zipcode of pharmacy | String | Required
phoneNumber | Phone number of pharmacy | String | Required




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
curl -i -H "Content-Type: application/json" -H "X-Auth-Token:patientuser@cooldoctors.io:patient:1515429239598:a0e476b75ffbacedd65e555b5304b222" -X DELETE  "https://api.endpoint.eyecarelive.com/DoctorOnDemand/api/patient/pharmacy/5a2c2efee4b0e4fa266e01b4"
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
200ok | it means successfully delete | String | 



`Authorization: X-Auth-Token`

<aside class="notice">
You must replace <code>X-Auth-Token</code> with your personal API key.
</aside>


## Add Insurance Info

```shell
### Get All Payers for adding insurance for card name

curl -i -H "Content-Type:application/json" -H "X-Auth-Token:patientuser@cooldoctors.io:patient:1515429239598:a0e476b75ffbacedd65e555b5304b222" -X GET "https://api.endpoint.eyecarelive.com/DoctorOnDemand/api/patient/eligible/getAllPayers"

### Add Insurance API with card images

curl -H "X-Auth-Token:patientuser@cooldoctors.io:patient:1515429239598:a0e476b75ffbacedd65e555b5304b222" -H "Content-Type:multipart/form-data" "https://api.endpoint.eyecarelive.com/DoctorOnDemand/api/patient/user/insurencecard/Aetna60054/W220/604" -X POST -F file=@/Users/cupertino/Downloads/2_user.png -F file=@/Users/cupertino/Downloads/2_user.png
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

curl -i -H "Content-Type: application/json" -H "X-Auth-Token:patientuser@cooldoctors.io:patient:1515429239598:a0e476b75ffbacedd65e555b5304b222" -X DELETE  "https://api.endpoint.eyecarelive.com/DoctorOnDemand/api/patient/user/insurencecard/1512974005984"

```

```shell

#Android Api

curl -i -H "Content-Type: application/json" -H "X-Auth-Token:patientuser@cooldoctors.io:patient:1515429239598:a0e476b75ffbacedd65e555b5304b222" -X POST "https://api.endpoint.eyecarelive.com/DoctorOnDemand/api/patient/user/insurencecard/delete/1512974005984"

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

curl -i -H "Content-Type: application/json" -H "X-Auth-Token:patientuser@cooldoctors.io:patient:1515429239598:a0e476b75ffbacedd65e555b5304b222" "https://api.endpoint.eyecarelive.com/DoctorOnDemand/api/patient/user/familyMember" -X POST -d '{"parentUserRelation":"brother","aboutMe":{"firstName":"neet","lastName":"yadav","address":"Pune", "city":"Pune","state":"MH","country":"india","pincode":"411039","gender":"male"},"role" :{"id": "551ad2a4e4b0b59ff0ccecc9","name": "patient"},"contactInfo":{"email":"Neet@gmail.com","phone":"8055802119"}}'

```
> The above command returns JSON structured like this:

```json
{
	"id": "5a2e4470e4b0e4fa266e0efe",
	"email": "8BQH25JS@eyecarelive.com",
	"pharmacyName": null,
	"pharmacyAddress": null,
	"profileImageId": null,
	"profileImageName": null,
	"aboutMe": {
		"id": "5a2e4470e4b0e4fa266e0efc",
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
		"id": "5a2e4470e4b0e4fa266e0efd",
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
	"createdAt": "2017-12-11 12:40 AM PST",
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

## Add Family Member information

```shell

curl -i -H "Content-Type:application/json" -H "X-Auth-Token:patientuser@cooldoctors.io:patient:1515429239598:a0e476b75ffbacedd65e555b5304b222" -X POST "https://api.endpoint.eyecarelive.com/DoctorOnDemand/api/patient/patientinfo/familyMember/5a2e4470e4b0e4fa266e0efe" -d '{"lifeStyle":{"smoke":"1","vitaminSupplements":"Test","allergies":"Pollen","alcoholDrinksPerWeek":"Do not Drink","medicalCondition":"Cancer","contactlenses":"Soft","medication":"Test","alcoholUse":"yes","allergiesToMedication":"Testing"},"familyHistory":{"diseaseRelation":[{"conditions":"Cataract","relationship":"Aunt"}]}}'

```
> The above command returns JSON structured like this:

```json
{
	"id": "5a2e4470e4b0e4fa266e0efe",
	"email": "8BQH25JS@eyecarelive.com",
	"pharmacyName": null,
	"pharmacyAddress": null,
	"profileImageId": null,
	"profileImageName": null,
	"aboutMe": {
		"id": "5a2e4470e4b0e4fa266e0efc",
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
		"id": "5a2e4470e4b0e4fa266e0efd",
		"email": "Neet@gmail.com",
		"phone": "8055802119",
		"smsNotification": false,
		"countryCode": null,
		"country": null,
		"emlNt": false
	},
	"patientInfo": {
		"id": "5a2e4a36e4b0e4fa266e0f7b",
		"lifeStyle": {
			"id": "5a2e4a36e4b0e4fa266e0f79",
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
			"id": "5a2e4a36e4b0e4fa266e0f7a",
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
	"timezone": null,
	"createdAt": "2017-12-11 12:40 AM PST",
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
}

```

> Make sure to replace `X-Auth-Token` with your API key.

Add family member’s profile information including medical history, social history, lifestyle information

### HTTP Request

`POST
http://localhost:8080/DoctorOnDemand/api/patient/patientinfo/familyMember/{FamilyMemberID}
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
Alcohol Use | Yes or No | String. Options Drinks per week (Do Not Drink, 1-6, 7-14, More than 14) | Optional
Medical Condition | Select values from list | String Glaucoma","Cataracts","Macular Degeneration","Eye Injury","Retina Disease","Other Disease","Blindness","Strabismus","Amblyopia","Diabetes","Cancer","Heart Disease","Hypertension","High Cholesterol","Kidney Disease","Stroke","Other" | Optional
Allergies | Select value | String. Fish, Peanuts, Pollen, Other | Optional
Contact Lenses | Select value | String. Soft, Hard, Other | Optional
Smoke Use | Yes or No | String. (Yes/No)  | Optional
Medications | Yes or No | String Type | Optional
Allergic to Medications  | Yes or No| String Type | Optional
Vitamins or Supplements | Yes or No| String Type | Optional
Conditions:Relation | One or more Conditions: relationship pairs | String | Optional

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


## Update Family Member Profile

```shell
curl -H "X-Auth-Token:patientuser@cooldoctors.io:patient:1515429239598:a0e476b75ffbacedd65e555b5304b222" -H "Content-Type:multipart/form-data" "https://api.endpoint.eyecarelive.com/DoctorOnDemand/api/patient/user//familymember/profileImageFromFile/5a2c1827e4b0e4fa266e018f" -X POST -F file=@/Users/cupertino/Downloads/dashboard2.png

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
Success | True OR False | String 




`Authorization: X-Auth-Token`

<aside class="notice">
You must replace <code>X-Auth-Token</code> with your personal API key.
</aside>


## Add Family member profile photo

```shell
curl -H "X-Auth-Token:patientuser@cooldoctors.io:patient:1515429239598:a0e476b75ffbacedd65e555b5304b222" -H "Content-Type:multipart/form-data" "https://api.endpoint.eyecarelive.com/DoctorOnDemand/api/patient/user//familymember/profileImageFromFile/5a2c1827e4b0e4fa266e018f" -X POST -F file=@/Users/cupertino/Downloads/dashboard2.png

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
 curl -i -H "Content-Type: application/json" -H "X-Auth-Token:patientuser@cooldoctors.io:patient:1515429239598:a0e476b75ffbacedd65e555b5304b222" "https://api.endpoint.eyecarelive.com/DoctorOnDemand/api/patient/user/familyMember" -X DELETE -d '{"id":"5a2c19d0e4b0e4fa266e0195"}'

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

curl -i -H "Content-Type: application/json" -H "X-Auth-Token:patientuser@cooldoctors.io:patient:1515429239598:a0e476b75ffbacedd65e555b5304b222" -X GET "https://api.endpoint.eyecarelive.com/DoctorOnDemand/api/patient/user/familyMember"

```
> The above command returns JSON structured like this:

```json
[{
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
}]

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











