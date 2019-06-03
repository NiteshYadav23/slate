

# Doctors

## List doctors by state and country

```shell
curl -i  -H "Content-Type: application/json" -H "X-Auth-Token:patientuser@cooldoctors.io:patient:1515429239598:a0e476b75ffbacedd65e555b5304b222" -X GET "https://dev.api.cooldoctors.io:8443/DoctorOnDemand/api/patient/user/doctorsbystate/NY/US"

```
> The above command returns JSON structured like this:

```json
[{
	"id": "58e2268be4b0b3b8e551c825",
	"email": "doctor@cooldoctors.io",
	"pharmacyName": null,
	"pharmacyAddress": null,
	"profileImageId": null,
	"profileImageName": null,
	"aboutMe": {
		"id": "58e2268be4b0b3b8e551c823",
		"firstName": "Raj",
		"lastName": "R",
		"birthDate": "04/16/2017",
		"address": "1010 W Fremont Ave",
		"city": "Sunnyvale",
		"country": "USA",
		"pincode": "95014",
		"gender": " Male",
		"languagesSpeak": ["English", "", ""],
		"additionalInfo": null,
		"state": "CA"
	},
	"contactInfo": {
		"id": "58e2268be4b0b3b8e551c824",
		"email": "doctor@cooldoctors.io",
		"phone": "408-836-0196",
		"smsNotification": true,
		"countryCode": null,
		"country": null,
		"emlNt": false
	},
	"patientInfo": null,
	"doctorInfo": {
		"id": "59816f67e4b0de21cd3e5b9b",
		"educationList": null,
		"hospitalAttachedWithList": null,
		"awardsReceivedList": null,
		"specialities": [{
			"id": "55b78065e4b0b393bf91678f",
			"name": "general physician",
			"questionnaire": null,
			"report": null
		}],
		"licencedState": [{
			"id": "5665a2cc9a87399fa0b9ba53",
			"state": "NY"
		}],
		"registrationNumber": "23232",
		"whyCoolDoctors": null,
		"bio": "Test",
		"profession": "Optometrist",
		"availabilityTimeZone": "America/Los_Angeles",
		"npi": ""
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
	"createdAt": "2017-04-03 12:40 PM CEST",
	"forgotPasswordToken": "x6xf7d",
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
	"profileImagePath": "https://dev.api.cooldoctors.io:8443/PRDIMAGE/doctor/58e2268be4b0b3b8e551c825/ProfileImage/Careers-after-MBA-for-doctor.jpg",
	"isReferredDoctor": null,
	"randomtoken": "Qrx9Fz",
	"isEmailVerified": false,
	"doctorsGroups": null,
	"preferredDoctors": ["56fb7614e4b0d3123cea4925"],
	"isAcceptTC": true,
	"insurenceCards": null,
	"notificationSettings": null,
	"clinics": ["58e24d29e4b03eb392b1d5b3", "58f9d4a7e4b07023de8c0d64"],
	"passCode": null,
	"emrId": null,
	"ssnId": null,
	"clinicInfo": null,
	"ref": null,
	"docOrg": null,
	"doctorsOrg": {
		"id": "59cb542de4b0fa09b42591b5",
		"orgName": "EyecareLive"
	},
	"twilioAccessToken": null,
	"invited": false,
	"validated": true,
	"activated": true,
	"managedUser": false,
	"addedByCpm": false,
	"pilotDoc": true
}]

```

> Make sure to replace `X-Auth-Token` with your API key.

Add a family member who could be the patient.


### HTTP Request

`GET
http://localhost:8080/DoctorOnDemand/api/patient/user/doctorsbystate/{state}/{country} 
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
{state}/{country} |  State and Country | String | Required



### Response

Parameter | Description | Type
--------- | ----------- | ----
ID | Database ID of family member | String 
Email | Generated email address from server | String 
aboutMe[{}] | Family member information | String 
contactInfo[{}] | Family member Contact info | String 
 role| Role (ID) Always use “551ad2a4e4b0b59ff0ccecc9” | String 
Doctor Info :[{}]| Ignore other parameters | String 
CreatedAt:[{}] | Role (ID) Always use “551ad2a4e4b0b59ff0ccecc9” | String 
Patient Info :[{}]| Ignore other parameters | String 


`Authorization: X-Auth-Token`

<aside class="notice">
You must replace <code>X-Auth-Token</code> with your personal API key.
</aside>

## Add Preferred doctor

```shell
curl -i  -H "Content-Type: application/json" -H "X-Auth-Token:patientuser@cooldoctors.io:patient:1515429239598:a0e476b75ffbacedd65e555b5304b222" -X POST "https://dev.api.cooldoctors.io:8443/DoctorOnDemand/api/patient/user/markPreferredDoctor/58e2268be4b0b3b8e551c825"

```
> The above command returns JSON structured like this:

```json
{
	"success": true
}

```

> Make sure to replace `X-Auth-Token` with your API key.

Mark a doctor as preferred doctor. User can default to the preferred doctor for follow-up care or new virtual visits and not be asked to choose doctor each time.

### HTTP Request

`POST
http://localhost:8080/DoctorOnDemand/api/patient/user/markPreferredDoctor/{DoctorID}
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
{state}/{country} |  State and Country | String | Required



### Response

Parameter | Description | Type
--------- | ----------- | ----
ID | Database ID of family member | String 
Email | Generated email address from server | String 
aboutMe[{}] | Family member information | String 
contactInfo[{}] | Family member Contact info | String 
 role| Role (ID) Always use “551ad2a4e4b0b59ff0ccecc9” | String 
Doctor Info :[{}]| Ignore other parameters | String 
CreatedAt:[{}] | Role (ID) Always use “551ad2a4e4b0b59ff0ccecc9” | String 
Patient Info :[{}]| Ignore other parameters | String 


`Authorization: X-Auth-Token`

<aside class="notice">
You must replace <code>X-Auth-Token</code> with your personal API key.
</aside>

## Get Preferred doctor

```shell

curl -i  -H "Content-Type: application/json" -H "X-Auth-Token:patientuser@cooldoctors.io:patient:1515429239598:a0e476b75ffbacedd65e555b5304b222" -X GET "https://dev.api.cooldoctors.io:8443/DoctorOnDemand/api/patient/user/getPreferredDoctors"

```
> The above command returns JSON structured like this:

```json
[{
	"id": "58e2268be4b0b3b8e551c825",
	"email": "doctor@cooldoctors.io",
	"pharmacyName": null,
	"pharmacyAddress": null,
	"profileImageId": null,
	"profileImageName": null,
	"aboutMe": {
		"id": "58e2268be4b0b3b8e551c823",
		"firstName": "Raj",
		"lastName": "R",
		"birthDate": "04/16/2017",
		"address": "1010 W Fremont Ave",
		"city": "Sunnyvale",
		"country": "USA",
		"pincode": "95014",
		"gender": " Male",
		"languagesSpeak": ["English", "", ""],
		"additionalInfo": null,
		"state": "CA"
	},
	"contactInfo": {
		"id": "58e2268be4b0b3b8e551c824",
		"email": "doctor@cooldoctors.io",
		"phone": "408-836-0196",
		"smsNotification": true,
		"countryCode": null,
		"country": null,
		"emlNt": false
	},
	"patientInfo": null,
	"doctorInfo": {
		"id": "59816f67e4b0de21cd3e5b9b",
		"educationList": null,
		"hospitalAttachedWithList": null,
		"awardsReceivedList": null,
		"specialities": [{
			"id": "55b78065e4b0b393bf91678f",
			"name": "general physician",
			"questionnaire": null,
			"report": null
		}],
		"licencedState": [{
			"id": "5665a2cc9a87399fa0b9ba53",
			"state": "NY"
		}],
		"registrationNumber": "23232",
		"whyCoolDoctors": null,
		"bio": "Test",
		"profession": "Optometrist",
		"availabilityTimeZone": "America/Los_Angeles",
		"npi": ""
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
	"createdAt": "2017-04-03 12:40 PM CEST",
	"forgotPasswordToken": "x6xf7d",
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
	"profileImagePath": "https://dev.api.cooldoctors.io:8443/PRDIMAGE/doctor/58e2268be4b0b3b8e551c825/ProfileImage/Careers-after-MBA-for-doctor.jpg",
	"isReferredDoctor": null,
	"randomtoken": "Qrx9Fz",
	"isEmailVerified": false,
	"doctorsGroups": null,
	"preferredDoctors": ["56fb7614e4b0d3123cea4925"],
	"isAcceptTC": true,
	"insurenceCards": null,
	"notificationSettings": null,
	"clinics": ["58e24d29e4b03eb392b1d5b3", "58f9d4a7e4b07023de8c0d64"],
	"passCode": null,
	"emrId": null,
	"ssnId": null,
	"clinicInfo": null,
	"ref": null,
	"docOrg": null,
	"doctorsOrg": {
		"id": "59cb542de4b0fa09b42591b5",
		"orgName": "EyecareLive"
	},
	"twilioAccessToken": null,
	"invited": false,
	"validated": true,
	"activated": true,
	"managedUser": false,
	"addedByCpm": false,
	"pilotDoc": true
}]

```

> Make sure to replace `X-Auth-Token` with your API key.

List patient’s list of preferred doctors

### HTTP Request

`GET
http://localhost:8080/DoctorOnDemand/api/patient/user/getPreferredDoctors
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
getPreferredDoctor | URL will give all doctors| String | Required



### Response

Parameter | Description | Type
--------- | ----------- | ----
ID | Database ID of family member | String 
Email | Generated email address from server | String 
aboutMe[{}] | Family member information | String 
contactInfo[{}] | Family member Contact info | String 
 role| Role (ID) Always use “551ad2a4e4b0b59ff0ccecc9” | String 
Doctor Info :[{}]| Ignore other parameters | String 
CreatedAt:[{}] | Role (ID) Always use “551ad2a4e4b0b59ff0ccecc9” | String 
Patient Info :[{}]| Ignore other parameters | String 


`Authorization: X-Auth-Token`

<aside class="notice">
You must replace <code>X-Auth-Token</code> with your personal API key.
</aside>





## Delete family Members

```shell

 curl -i  -H "Content-Type: application/json" -H "X-Auth-Token:patientuser@cooldoctors.io:patient:1515429239598:a0e476b75ffbacedd65e555b5304b222" -X POST "https://dev.api.cooldoctors.io:8443/DoctorOnDemand/api/patient/user/unmarkPreferredDoctor/58e2268be4b0b3b8e551c825"

```
> The above command returns JSON structured like this:

```json
{
	"success": true
}
```

> Make sure to replace `X-Auth-Token` with your API key.

Unmark the doctor as preferred doctor in the user’s profile. This will require user to choose a doctor from the list of doctors in that state for new virtual visits.

### HTTP Request

`POST
http://localhost:8080/DoctorOnDemand/api/patient/user/unmarkPreferredDoctor/{DoctorID}
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
{DoctorID} |  Pass doctor ID | String | Required
   


### Response

Parameter | Description | Type
--------- | ----------- | ----
Success | True OR False | String 




`Authorization: X-Auth-Token`

<aside class="notice">
You must replace <code>X-Auth-Token</code> with your personal API key.
</aside>

## Show doctor’s availability for current week

```shell
curl -i -H "Content-Type:application/json" -H "X-Auth-Token:patientuser@cooldoctors.io:patient:1515429239598:a0e476b75ffbacedd65e555b5304b222" "https://dev.api.cooldoctors.io:8443/DoctorOnDemand/api/patient/appointment/getAvailabilityOfCurrentWeek/56fb7614e4b0d3123cea4925" -X POST -d '{"timezone":"Asia/Kolkata"}'
```
> The above command returns JSON structured like this:

```json
[
  {
    "id": "5a2e54cfe4b0e4fa266e12e7",
    "startTime": "18",
    "sTime": "2017-12-12 11:30 PM IST",
    "eTime": "2017-12-12 06:10 PM UTC",
    "slotNumber": "0",
    "patient": null,
    "visitType": null,
    "appointmentId": null,
    "status": "enable",
    "booked": false
  },
  {
    "id": "5a2e54cfe4b0e4fa266e12e8",
    "startTime": "18",
    "sTime": "2017-12-12 11:40 PM IST",
    "eTime": "2017-12-12 06:20 PM UTC",
    "slotNumber": "1",
    "patient": null,
    "visitType": null,
    "appointmentId": null,
    "status": "enable",
    "booked": false
  },
  {
    "id": "5a2e54cfe4b0e4fa266e12e9",
    "startTime": "18",
    "sTime": "2017-12-12 11:50 PM IST",
    "eTime": "2017-12-12 06:30 PM UTC",
    "slotNumber": "2",
    "patient": null,
    "visitType": null,
    "appointmentId": null,
    "status": "enable",
    "booked": false
  },
  {
    "id": "5a2e54cfe4b0e4fa266e12ea",
    "startTime": "18",
    "sTime": "2017-12-13 12:00 AM IST",
    "eTime": "2017-12-12 06:40 PM UTC",
    "slotNumber": "3",
    "patient": null,
    "visitType": null,
    "appointmentId": null,
    "status": "enable",
    "booked": false
  },
  {
    "id": "5a2e54cfe4b0e4fa266e12eb",
    "startTime": "18",
    "sTime": "2017-12-13 12:10 AM IST",
    "eTime": "2017-12-12 06:50 PM UTC",
    "slotNumber": "4",
    "patient": null,
    "visitType": null,
    "appointmentId": null,
    "status": "enable",
    "booked": false
  },
  {
    "id": "5a2e54cfe4b0e4fa266e12ec",
    "startTime": "18",
    "sTime": "2017-12-13 12:20 AM IST",
    "eTime": "2017-12-12 07:00 PM UTC",
    "slotNumber": "5",
    "patient": null,
    "visitType": null,
    "appointmentId": null,
    "status": "enable",
    "booked": false
  },
  {
    "id": "5a2e54cfe4b0e4fa266e12e1",
    "startTime": "19",
    "sTime": "2017-12-13 12:30 AM IST",
    "eTime": "2017-12-12 07:10 PM UTC",
    "slotNumber": "0",
    "patient": null,
    "visitType": null,
    "appointmentId": null,
    "status": "enable",
    "booked": false
  },
  {
    "id": "5a2e54cfe4b0e4fa266e12e2",
    "startTime": "19",
    "sTime": "2017-12-13 12:40 AM IST",
    "eTime": "2017-12-12 07:20 PM UTC",
    "slotNumber": "1",
    "patient": null,
    "visitType": null,
    "appointmentId": null,
    "status": "enable",
    "booked": false
  },
  {
    "id": "5a2e54cfe4b0e4fa266e12e3",
    "startTime": "19",
    "sTime": "2017-12-13 12:50 AM IST",
    "eTime": "2017-12-12 07:30 PM UTC",
    "slotNumber": "2",
    "patient": null,
    "visitType": null,
    "appointmentId": null,
    "status": "enable",
    "booked": false
  },
  {
    "id": "5a2e54cfe4b0e4fa266e12e4",
    "startTime": "19",
    "sTime": "2017-12-13 01:00 AM IST",
    "eTime": "2017-12-12 07:40 PM UTC",
    "slotNumber": "3",
    "patient": null,
    "visitType": null,
    "appointmentId": null,
    "status": "enable",
    "booked": false
  },
  {
    "id": "5a2e54cfe4b0e4fa266e12e5",
    "startTime": "19",
    "sTime": "2017-12-13 01:10 AM IST",
    "eTime": "2017-12-12 07:50 PM UTC",
    "slotNumber": "4",
    "patient": null,
    "visitType": null,
    "appointmentId": null,
    "status": "enable",
    "booked": false
  },
  {
    "id": "5a2e54cfe4b0e4fa266e12e6",
    "startTime": "19",
    "sTime": "2017-12-13 01:20 AM IST",
    "eTime": "2017-12-12 08:00 PM UTC",
    "slotNumber": "5",
    "patient": null,
    "visitType": null,
    "appointmentId": null,
    "status": "enable",
    "booked": false
  }
]
```

> Make sure to replace `X-Auth-Token` with your API key.

Show availability calendar of the doctor chosen or preferred doctor. User can select a time slot available on the calendar or select an option to choose another doctor in the same clinic group if the preferred doctor is unavailable at the desired time.


### HTTP Request

`POST
http://localhost:8080/DoctorOnDemand/api/patient/appointment/getAvailabilityOfCurrentWeek/{DoctorID}
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
{DoctorID} |  Pass doctor ID | String | Required
timezone | Pass local time of user Like this {"timezone":"Asia/Kolkata"} | String | Required
   


### Response

Parameter | Description | Type
--------- | ----------- | ----
id | Availability Book slot  time ID | String 
startTime sTime | sTime is start time| String 
eTime | eTime is End time  | String 
slotNumber | This will be slot number as per selected for time | String 
patient | Deprecated parameter | String 
visitType | Deprecated parameter | String 
appointmentId | Deprecated parameter | String 
status | Deprecated parameter | String 
booked | Deprecated parameter | String 
   |Same all the array is coming for multiple slots| |


`Authorization: X-Auth-Token`

<aside class="notice">
You must replace <code>X-Auth-Token</code> with your personal API key.
</aside>

## Show doctor’s availability for next week

```shell

curl -i -H "Content-Type:application/json" -H "X-Auth-Token:patientuser@cooldoctors.io:patient:1515429239598:a0e476b75ffbacedd65e555b5304b222" "https://dev.api.cooldoctors.io:8443/DoctorOnDemand/api/patient/appointment/getAvailabilityOfNextWeek/56fb7614e4b0d3123cea4925"  -X POST -d '{"Asia/Kolkata"}'

```
> The above command returns JSON structured like this:

```json

[{
	"id": "5a2e5bdce4b0e4fa266e167d",
	"startTime": "12",
	"sTime": "2017-12-17 05:30 PM IST",
	"eTime": "2017-12-17 12:10 PM UTC",
	"slotNumber": "0",
	"patient": null,
	"visitType": null,
	"appointmentId": null,
	"status": "enable",
	"booked": false
}, {
	"id": "5a2e5bdce4b0e4fa266e167e",
	"startTime": "12",
	"sTime": "2017-12-17 05:40 PM IST",
	"eTime": "2017-12-17 12:20 PM UTC",
	"slotNumber": "1",
	"patient": null,
	"visitType": null,
	"appointmentId": null,
	"status": "enable",
	"booked": false
}, {
	"id": "5a2e5bdce4b0e4fa266e167f",
	"startTime": "12",
	"sTime": "2017-12-17 05:50 PM IST",
	"eTime": "2017-12-17 12:30 PM UTC",
	"slotNumber": "2",
	"patient": null,
	"visitType": null,
	"appointmentId": null,
	"status": "enable",
	"booked": false
}, {
	"id": "5a2e5bdce4b0e4fa266e1680",
	"startTime": "12",
	"sTime": "2017-12-17 06:00 PM IST",
	"eTime": "2017-12-17 12:40 PM UTC",
	"slotNumber": "3",
	"patient": null,
	"visitType": null,
	"appointmentId": null,
	"status": "enable",
	"booked": false
}, {
	"id": "5a2e5bdce4b0e4fa266e1681",
	"startTime": "12",
	"sTime": "2017-12-17 06:10 PM IST",
	"eTime": "2017-12-17 12:50 PM UTC",
	"slotNumber": "4",
	"patient": null,
	"visitType": null,
	"appointmentId": null,
	"status": "enable",
	"booked": false
}, {
	"id": "5a2e5bdce4b0e4fa266e1682",
	"startTime": "12",
	"sTime": "2017-12-17 06:20 PM IST",
	"eTime": "2017-12-17 01:00 PM UTC",
	"slotNumber": "5",
	"patient": null,
	"visitType": null,
	"appointmentId": null,
	"status": "enable",
	"booked": false
}]

```

> Make sure to replace `X-Auth-Token` with your API key.

Show chosen doctor’s availability calendar for next week

### HTTP Request

`POST
http://localhost:8080/DoctorOnDemand/api/patient/appointment/getAvailabilityOfNextWeek/{DoctorID}
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
{DoctorID} |  Pass doctor ID | String | Required
timezone | Pass local time of user Like this {"timezone":"Asia/Kolkata"} | String | Required
   


### Response

Parameter | Description | Type
--------- | ----------- | ----
id | Availability Book slot  time ID | String 
startTime sTime | sTime is start time| String 
eTime | eTime is End time  | String 
slotNumber | This will be slot number as per selected for time | String 
patient | Deprecated parameter | String 
visitType | Deprecated parameter | String 
appointmentId | Deprecated parameter | String 
status | Deprecated parameter | String 
booked | Deprecated parameter | String 

   |Same all the array is coming for multiple slots| |


`Authorization: X-Auth-Token`

<aside class="notice">
You must replace <code>X-Auth-Token</code> with your personal API key.
</aside>










