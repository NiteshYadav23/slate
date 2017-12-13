
# Messaging

## Get list of Users for Messaging

```shell
curl -i -H "Content-Type: application/image" -H "X-Auth-Token:patientuser@cooldoctors.io:patient:1515429239598:a0e476b75ffbacedd65e555b5304b222" -X GET "https://api.endpoint.eyecarelive.com/DoctorOnDemand/api/patient/user/doctors"

```
> The above command returns JSON structured like this:

```json
[{
	"id": "56fb7614e4b0d3123cea4925",
	"email": "nitesh.yadav@cupertinosoft.com",
	"pharmacyName": null,
	"pharmacyAddress": null,
	"profileImageId": null,
	"profileImageName": null,
	"aboutMe": {
		"id": "56fb7614e4b0d3123cea4923",
		"firstName": "Paul",
		"lastName": "Super",
		"birthDate": "03/22/2016",
		"address": "1010 W Fremont Ave # 200",
		"city": "Sunnyvale",
		"country": "United States",
		"pincode": "94087",
		"gender": " Male",
		"languagesSpeak": ["English", "", ""],
		"additionalInfo": null,
		"state": "ca"
	},
	"contactInfo": {
		"id": "56fb7614e4b0d3123cea4924",
		"email": "nitesh.yadav@cupertinosoft.com",
		"phone": "8055802119",
		"smsNotification": false,
		"countryCode": "+91",
		"country": "USA",
		"emlNt": false
	},
	"patientInfo": null,
	"doctorInfo": {
		"id": "5823018fe4b0242bf4219c2d",
		"educationList": [{
			"id": "59e09cbce4b0a70b0de5b0c3",
			"degree": "    Bca",
			"university": "   un",
			"yearOfPasssing": "   88778"
		}],
		"hospitalAttachedWithList": [{
			"id": "59e09cbce4b0a70b0de5b0c4",
			"name": "   ng tt",
			"city": "    Pune",
			"country": "   India"
		}],
		"awardsReceivedList": [{
			"id": "59e09cbce4b0a70b0de5b0c5",
			"name": "q",
			"description": "    • • • • • • •  •  •  •  Description",
			"date": "11/11/1991"
		}],
		"specialities": [{
			"id": "55b78065e4b0b393bf91678f",
			"name": "general physician",
			"questionnaire": null,
			"report": null
		}],
		"licencedState": [{
			"id": "5665a2cb9a87399fa0b9ba33",
			"state": "AL"
		}, {
			"id": "5665a2cb9a87399fa0b9ba34",
			"state": "AK"
		}, {
			"id": "5665a2cb9a87399fa0b9ba35",
			"state": "AZ"
		}, {
			"id": "5665a2cb9a87399fa0b9ba40",
			"state": "IL"
		}, {
			"id": "5665a2cb9a87399fa0b9ba41",
			"state": "IN"
		}, {
			"id": "5665a2cb9a87399fa0b9ba42",
			"state": "IA"
		}],
		"registrationNumber": "22222",
		"whyCoolDoctors": null,
		"profession": "Optometrist",
		"availabilityTimeZone": "America/Los_Angeles",
		"npi": "0123456789778"
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
	"createdAt": "2016-03-29 11:45 PM PDT",
	"forgotPasswordToken": "4691",
	"familyMembers": null,
	"parentUser": null,
	"parentUserRelation": null,
	"password": null,
	"rating": null,
	"preferredPharmacy": null,
	"kandyUserName": "dcrqfv5ku3",
	"kandyUserPassword": "11a5221883d440",
	"kandyFullUserId": "dcrqfv5ku3@cmobrtctest.com",
	"oldPassword": null,
	"loginStatus": "Online",
	"stripeCustId": null,
	"profileImagePath": "https://api.endpoint.eyecarelive.com/PRDIMAGE/doctor/56fb7614e4b0d3123cea4925/ProfileImage/paulsuper.png",
	"isReferredDoctor": null,
	"randomtoken": "esnckN",
	"isEmailVerified": false,
	"doctorsGroups": [{
		"id": "56d01388e4b0cd1739f0e076",
		"groupName": "Silicon Valley Eye Physicians"
	}],
	"preferredDoctors": ["56fbd63de4b0777c5a04f540", "595a0d97e4b0c065c25684ea"],
	"isAcceptTC": true,
	"insurenceCards": null,
	"notificationSettings": null,
	"clinics": ["58f9d4a7e4b07023de8c0d64"],
	"passCode": null,
	"emrId": null,
	"ssnId": null,
	"clinicInfo": null,
	"ref": null,
	"docOrg": null,
	"doctorsOrg": {
		"id": "59cb5445e4b0fa09b42591b7",
		"orgName": "Paragon"
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

Get list of all doctors for messaging. Patients can choose any doctor and send a question before creating a new visit

### HTTP Request

`GET
http://localhost:8080/DoctorOnDemand/api/patient/user/doctors 
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




## Get list of messages by user

```shell
curl -H "X-Auth-Token:patientuser@cooldoctors.io:patient:1515429239598:a0e476b75ffbacedd65e555b5304b222" -H "Content-Type:application/json" "https://api.endpoint.eyecarelive.com/DoctorOnDemand/api/patient/followup/getchatuserlist"

```
> The above command returns JSON structured like this:

```json
[{
	"id": "5a2d2c1de4b0e4fa266e02a3",
	"userOne": "5a2c0a69e4b0e4fa266e0180",
	"userTwo": "58e2268be4b0b3b8e551c825",
	"updatedAt": 1512910223997,
	"count": 0,
	"userdetails": {
		"usrOneProfImg": "https://eyes.cooldoctors.io/PRDIMAGE/patient/5a2c0a69e4b0e4fa266e0180/ProfileImage/dashboard2.png",
		"usrTwoProfImg": "https://api.endpoint.eyecarelive.com/PRDIMAGE/doctor/58e2268be4b0b3b8e551c825/ProfileImage/Careers-after-MBA-for-doctor.jpg",
		"usrOneAbtMe": {
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
		"usrTwoAbtMe": {
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
		}
	}
}]

```

> Make sure to replace `X-Auth-Token` with your API key.

List of all the messages in a conversation with a doctor

### HTTP Request

`GET
http://localhost:8080/DoctorOnDemand/api/patient/followup/getchatuserlist
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
Get APi |  It will give the user chat list. | String | Required



### Response

Parameter | Description | Type
--------- | ----------- | ----
ID | This ID is unique chatID in database | String 
userOne | UserOne will be patientID | String 
userTwo | UserTwo will be patientID| String 
updatedAt | Deprecated  | String 
 count| Unread Messages count | String 
userdetails[{}]| UserDetails having patient and doctor profile image | String 
usrOneAbtMe[{}] | This will give the user personal details | String 
usrTwoAbtMe[{}]| This will give the user personal details | String 


`Authorization: X-Auth-Token`

<aside class="notice">
You must replace <code>X-Auth-Token</code> with your personal API key.
</aside>



## Send a new message to a doctor

```shell

curl -H "X-Auth-Token:patientuser@cooldoctors.io:patient:1515429239598:a0e476b75ffbacedd65e555b5304b222" -H "Content-Type:application/json" "https://api.endpoint.eyecarelive.com/DoctorOnDemand/api/patient/followup" -X POST -d '{"content":"Hi Jerry, how are you feeling now.?","senderId":"5a2c0a69e4b0e4fa266e0180","recipientId":"58e2268be4b0b3b8e551c825"}'

```
> The above command returns JSON structured like this:

```json
[{
	"id": "5a2d2c1de4b0e4fa266e02a3",
	"userOne": "5a2c0a69e4b0e4fa266e0180",
	"userTwo": "58e2268be4b0b3b8e551c825",
	"updatedAt": 1512910223997,
	"count": 0,
	"userdetails": {
		"usrOneProfImg": "https://eyes.cooldoctors.io/PRDIMAGE/patient/5a2c0a69e4b0e4fa266e0180/ProfileImage/dashboard2.png",
		"usrTwoProfImg": "https://api.endpoint.eyecarelive.com/PRDIMAGE/doctor/58e2268be4b0b3b8e551c825/ProfileImage/Careers-after-MBA-for-doctor.jpg",
		"usrOneAbtMe": {
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
		"usrTwoAbtMe": {
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
		}
	}
}]

```

> Make sure to replace `X-Auth-Token` with your API key.

Send a new message to a doctor

### HTTP Request

`POST
http://localhost:8080DoctorOnDemand/api/patient/followup/
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
senderId |  In Sender ID need to pass the logged in user ID in sender | String | Required
recipientId | In Recipient need to pass the doctor ID which one selected from the list of doctors API| String | Required
content |  In Content need to write message | String | Required



### Response

Parameter | Description | Type
--------- | ----------- | ----
ID | This ID is unique chatID in database | String 
subject | Deprecated | String 
content | Written message content showing| String 
senderId | Sender ID is patient id  | String 
recipientId| Recipient ID is doctors ID  | String 
parentId| Deprecated | String 
timestamp | Message Time | String 
read_status | Deprecated | String 
appointmentId | If we patient send message on appointment then the Appointment id will return here | String 
senderAboutMe[{}] | Sender about having the sender information| String 
recipientAboutMe[{}] | Recipient about having the Recipient information  | String 
messageType| If that is Appointment wise message then need to pass “withAppointment” & without message “withoutAppointment” | String 
chatId| This will chatID  | String 
createdAt | Deprecated | String 


`Authorization: X-Auth-Token`

<aside class="notice">
You must replace <code>X-Auth-Token</code> with your personal API key.
</aside>


## Send file via messaging to a doctor

```shell

curl -H "X-Auth-Token:patientuser@cooldoctors.io:patient:1515429239598:a0e476b75ffbacedd65e555b5304b222" -H "Content-Type:application/json" "https://api.endpoint.eyecarelive.com/DoctorOnDemand/api/patient/followup" -X POST -d '{"content":"Hi Jerry, how are you feeling now.?","senderId":"5a2c0a69e4b0e4fa266e0180","recipientId":"58e2268be4b0b3b8e551c825"}'

```
> The above command returns JSON structured like this:

```json
{
	"id": "5a2e9137e4b0e4fa266e23ad",
	"subject": null,
	"content": null,
	"senderId": "5a2c0a69e4b0e4fa266e0180",
	"recipientId": "58e2268be4b0b3b8e551c825",
	"parentId": null,
	"timestamp": "2017-12-11 06:07 AM PST",
	"status": null,
	"read_status": false,
	"appointmentId": null,
	"senderAboutMe": {
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
	"symtons": null,
	"fileId": null,
	"fileName": null,
	"filePath": null,
	"contentTypes": null,
	"senderProfileImage": "https://eyes.cooldoctors.io/PRDIMAGE/patient/5a2c0a69e4b0e4fa266e0180/ProfileImage/dashboard2.png",
	"isDoctor": false,
	"recipientAboutMe": {
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
	"recipientProfileImage": "https://api.endpoint.eyecarelive.com/PRDIMAGE/doctor/58e2268be4b0b3b8e551c825/ProfileImage/Careers-after-MBA-for-doctor.jpg",
	"messageType": "withoutAppointment",
	"chatId": "5a2d2c1de4b0e4fa266e02a3",
	"createdAt": "2017-12-11 06:07 AM PST"
}

```

> Make sure to replace `X-Auth-Token` with your API key.

This is two step API. $URL/uploadFollowUpMessageFilesInfoIndividual/ returns a follow-up id#. This id# is then passed to $URL/uploadFollowUpMessageFilesIndividual/{followupId} to send the file to the doctor as a follow-up message.

### HTTP Request

`POST
http://localhost:8080/DoctorOnDemand/api/patient/followup/uploadFollowUpMessageFilesInfoIndividual/
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
senderId |  In Sender ID need to pass the logged in user ID in sender | String | Required
recipientId | In Recipient need to pass the doctor ID which one selected from the list of doctors API| String | Required




### Response

Parameter | Description | Type
--------- | ----------- | ----
ID | This ID is unique chatID in database | String 
subject | Deprecated | String 
content | Written message content showing| String 
senderId | Sender ID is patient id  | String 
recipientId| Recipient ID is doctors ID  | String 
parentId| Deprecated | String 
timestamp | Message Time | String 
read_status | Deprecated | String 
appointmentId | If we patient send message on appointment then the Appointment id will return here | String 
senderAboutMe[{}] | Sender about having the sender information| String 
recipientAboutMe[{}] | Recipient about having the Recipient information  | String 
messageType| If that is Appointment wise message then need to pass “withAppointment” & without message “withoutAppointment” | String 
chatId| This will chatID  | String 
createdAt | Deprecated | String 


`Authorization: X-Auth-Token`

<aside class="notice">
You must replace <code>X-Auth-Token</code> with your personal API key.
</aside>

# 

## Send file via messaging to a doctor

```shell

curl -H "X-Auth-Token:patientuser@cooldoctors.io:patient:1515429239598:a0e476b75ffbacedd65e555b5304b222" -H "Content-Type:multipart/form-data" "https://api.endpoint.eyecarelive.com/DoctorOnDemand/api/patient/followup/uploadFollowUpMessageFilesIndividual/5a2e9137e4b0e4fa266e23ad" -X POST -F file=@/Users/cupertino/Downloads/dash3.png  

```
> The above command returns JSON structured like this:

```json
{
	"id": "5a2e9137e4b0e4fa266e23ad",
	"subject": null,
	"content": null,
	"senderId": "5a2c0a69e4b0e4fa266e0180",
	"recipientId": "58e2268be4b0b3b8e551c825",
	"parentId": null,
	"timestamp": "2017-12-11 06:07 AM PST",
	"status": null,
	"read_status": false,
	"appointmentId": null,
	"senderAboutMe": {
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
	"symtons": null,
	"fileId": null,
	"fileName": null,
	"filePath": null,
	"contentTypes": null,
	"senderProfileImage": "https://eyes.cooldoctors.io/PRDIMAGE/patient/5a2c0a69e4b0e4fa266e0180/ProfileImage/dashboard2.png",
	"isDoctor": false,
	"recipientAboutMe": {
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
	"recipientProfileImage": "https://api.endpoint.eyecarelive.com/PRDIMAGE/doctor/58e2268be4b0b3b8e551c825/ProfileImage/Careers-after-MBA-for-doctor.jpg",
	"messageType": "withoutAppointment",
	"chatId": "5a2d2c1de4b0e4fa266e02a3",
	"createdAt": "2017-12-11 06:07 AM PST"
}

```

> Make sure to replace `X-Auth-Token` with your API key.

This is two step API. $URL/uploadFollowUpMessageFilesInfoIndividual/ returns a follow-up id#. This id# is then passed to $URL/uploadFollowUpMessageFilesIndividual/{followupId} to send the file to the doctor as a follow-up message.

### HTTP Request

`POST
http://localhost:8080/DoctorOnDemand/api/patient/followup/uploadFollowUpMessageFilesIndividual/{followupId}
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
senderId |  In Sender ID need to pass the logged in user ID in sender | String | Required
recipientId | In Recipient need to pass the doctor ID which one selected from the list of doctors API| String | Required
{followupId} |  Need to pass follow-up id in the URL | String | Required
-F file=@/FilePath |  Need to upload file using API | String | Required



### Response

Parameter | Description | Type
--------- | ----------- | ----
ID | This ID is unique chatID in database | String 
subject | Deprecated | String 
content | Written message content showing| String 
senderId | Sender ID is patient id  | String 
recipientId| Recipient ID is doctors ID  | String 
parentId| Deprecated | String 
timestamp | Message Time | String 
read_status | Deprecated | String 
appointmentId | If we patient send message on appointment then the Appointment id will return here | String 
senderAboutMe[{}] | Sender about having the sender information| String 
recipientAboutMe[{}] | Recipient about having the Recipient information  | String 
messageType| If that is Appointment wise message then need to pass “withAppointment” & without message “withoutAppointment” | String 
chatId| This will chatID  | String 
createdAt | Deprecated | String 
fileId | It will return the file ID for get URL of uploaded photo | String


`Authorization: X-Auth-Token`

<aside class="notice">
You must replace <code>X-Auth-Token</code> with your personal API key.
</aside>


## Get view file from messages

```shell
curl -H "X-Auth-Token:patientuser@cooldoctors.io:patient:1515429239598:a0e476b75ffbacedd65e555b5304b222" -H "Content-Type:multipart/form-data" "https://api.endpoint.eyecarelive.com/DoctorOnDemand/api/patient/followup/getUrl/1512909942596/5a2d2c5ce4b0e4fa266e02a6"

```
> The above command returns JSON structured like this:

```json
{
	"url": "https://d5qf5duw6o0fe.cloudfront.net/patient/5a2c0a69e4b0e4fa266e0180/followUpMessage/1512909942474/2_user.png?Expires=1512910336&Signature=b4ykk8mvNCpzaGlwg0smiK4LuM-cQ31brqVJ3JoY-n6JC6yunuoS2bnI7lk~zhGF5wE-PKOGG3eIBryPHwkpZBNSSEWPJn8p8IU1plI3qwGewm85PbLqEzlcIBFUeHqQpuEZLaw8EQMv7jcGDInEgiif4rl7SaFF-IHZ3Ix0YTvmTSxPtquZJ6IX~RSBSAjs~7r7qUR-9vyJXjNyC-Dk-r3nW2aJ6b1yyL0ba9kVX8WhHd3WX9heozx6k9by7I7~V8ObKwc0O5DSB3RaM97917r63-TSQK-c44AFCwHLQLxKdvnWhhda67ZaNcxryG1O7txNRMESq-ZZsZCjIxbn7A__&Key-Pair-Id=APKAJKM62WTRWOS5N27Q"
}

```

> Make sure to replace `X-Auth-Token` with your API key.

This API will return the file URL for view. 

### HTTP Request

`GET
http://localhost:8080/DoctorOnDemand/api/patient/followup/getUrl/1512909942596/5a2d2c5ce4b0e4fa266e02a6
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
{fileID} |  need to pass the file id in the request url| String | Required
{followupID} |  need to pass the follow-up id in the request url | String | Required



### Response

Parameter | Description | Type
--------- | ----------- | ----
url | It will return the link for view the image | String 



`Authorization: X-Auth-Token`

<aside class="notice">
You must replace <code>X-Auth-Token</code> with your personal API key.
</aside>




