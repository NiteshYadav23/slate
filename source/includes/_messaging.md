
# Messaging

## Get Patient's Chat List

```shell
curl -i -H "Content-Type: application/json" -H "X-Auth-Token:patientuser1@eyecarelive.com:patient:1561784861568:d5171513ed94a5fafb354f6f8688b751" -X GET  "https://dev.api.cooldoctors.io:8443/DoctorOnDemand/api/patient/followup/getchatuserlist/v3"


```
> The above command returns JSON structured like this:

```json
[
  {
    "id": "5cf02638f893f4052b1279ce",
    "userOne": "5ceed13cf893f45b5812b8e1",
    "userTwo": "56fb7614e4b0d3123cea4925",
    "updatedAt": 1559242296379,
    "count": 0,
    "userdetails": {
      "usrOneProfImg": null,
      "usrTwoProfImg": "https://s3.amazonaws.com/deveclprofimg/PRDIMAGE/doctor/56fb7614e4b0d3123cea4925/ProfileImage/imgDefault.png",
      "usrOneAbtMe": {
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
      "usrTwoAbtMe": {
        "id": "56fb7614e4b0d3123cea4923",
        "firstName": "Dr. John",
        "lastName": "Gelles",
        "birthDate": "xCbUo9+vCO6W+uI8luz3YA==",
        "address": "8L10iLEjsRBVkFaI1gu4bw==",
        "city": "8L10iLEjsRBVkFaI1gu4bw==",
        "country": "rwq24J1FnEhqovLa/bo5uQ==",
        "pincode": "+ffKFHCfLQG2vGeutdG6BQ==",
        "gender": "male",
        "languagesSpeak": [
          "English",
          "",
          ""
        ],
        "additionalInfo": "Hi I plays cricket",
        "state": "tdK26+Dp5ks9TH9wFlmgDA==",
        "lat": null,
        "lang": null
      }
    },
    "lastMsg": "Testing ",
    "lastMsgTime": "2019-05-30 11:51 AM PDT"
  }
]
```

> Make sure to replace `X-Auth-Token` with your API key.


### HTTP Request

`GET
http://localhost:8080/DoctorOnDemand/api/patient/followup/getchatuserlist/v3
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
URL |  This API no need to pass | String | Required



### Response

Parameter | Description | Type
--------- | ----------- | ----
ID | User's ID | String 
userOne | User one with unique ID | String 
userTwo | User two with unique ID | String 
updatedAt | Update at has the timestamp | String 
count | will show up for unread and read the message for a particular chat | String 
userdetails | This is for the user details of the patient | String 
usrOneAbtMe:[{}]| Dynamic first user data of about me | String 
usrTwoAbtMe:[{}] | Dynamic second user data of about me | String
additionalInfo | Deprecated | String
state | State of the patient | String
lat | Deprecated | String
lang | Deprecated | String
lastMsg | Last messages of chat | String
lastMsgTime | Last message time | String


`Authorization: X-Auth-Token`

<aside class="notice">
You must replace <code>X-Auth-Token</code> with your personal API key.
</aside>


## Get chat for a Particular Doctor

```shell
curl -i -H "Content-Type: application/json" -H "X-Auth-Token:patientuser1@eyecarelive.com:patient:1561784861568:d5171513ed94a5fafb354f6f8688b751" -X GET  "https://dev.api.cooldoctors.io:8443/DoctorOnDemand/api/patient/followup/getmsgbychatid/5cec0646f893f467fffdcb76"

```
> The above command returns JSON structured like this:

```json
[
  {
    "id": "5cec0646f893f467fffdcb77",
    "subject": "My Demo",
    "content": "Hi",
    "senderId": "5cea6d98f893f40a5f0395b1",
    "recipientId": "56fb7614e4b0d3123cea4925",
    "parentId": null,
    "timestamp": "2019-05-27 08:46 AM PDT",
    "status": null,
    "read_status": true,
    "appointmentId": null,
    "senderAboutMe": null,
    "symtons": null,
    "fileId": null,
    "fileName": null,
    "filePath": null,
    "contentTypes": null,
    "senderProfileImage": null,
    "isDoctor": false,
    "recipientAboutMe": null,
    "recipientProfileImage": null,
    "messageType": "withoutAppointment",
    "chatId": "5cec0646f893f467fffdcb76",
    "createdAt": "2019-05-27 08:46 AM PDT",
    "uploadStatus": false,
    "staffId": null,
    "staffAboutMe": null,
    "staffProfileImage": null,
    "staff": false
  }
]
```

> Make sure to replace `X-Auth-Token` with your API key.


### HTTP Request

`GET
http://localhost:8080/DoctorOnDemand/api/patient/followup/getmsgbychatid/{CHAT-ID}/
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
URL |  This API no need to pass | String | Required



### Response

Parameter | Description | Type
--------- | ----------- | ----
ID | Message ID | String 
subject | Generated email address from server | String 
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



## Get CHAT ID by doctor ID

```shell
curl -i -H "Content-Type: application/json" -H "X-Auth-Token:patientuser1@eyecarelive.com:patient:1561784861568:d5171513ed94a5fafb354f6f8688b751" -X GET  "https://dev.api.cooldoctors.io:8443/DoctorOnDemand/api/patient/followup/getchatidbydocis/56fb7614e4b0d3123cea492"

```
> The above command returns JSON structured like this:

```json
{
  "id": "5cf02638f893f4052b1279ce",
  "userOne": "5ceed13cf893f45b5812b8e1",
  "userTwo": "56fb7614e4b0d3123cea4925",
  "updatedAt": 1559242296379,
  "count": 0,
  "userdetails": null,
  "lastMsg": null,
  "lastMsgTime": null
}
```

> Make sure to replace `X-Auth-Token` with your API key.



### HTTP Request

`GET
http://localhost:8080/DoctorOnDemand/api/patient/followup/getchatidbydocis/{DoctorId}/
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
URL |  In this API need to pass the doctor ID in the URL | String | Required



### Response

Parameter | Description | Type
--------- | ----------- | ----
ID | ID of messages | String 
userOne | This will be patient ID  | String 
userTwo | This will be doctor ID | String 
updatedAt | Updated time stamp | String 
userdetails | Deprecated | String 
lastMsg | Deprecated | String 
lastMsgTime | Deprecated | String 


`Authorization: X-Auth-Token`

<aside class="notice">
You must replace <code>X-Auth-Token</code> with your personal API key.
</aside>



## Send Follow Up message to Doctor

```shell
curl -i -H "Content-Type:application/json" -H "x-auth-token:patientuser1@eyecarelive.com:patient:1561784861568:d5171513ed94a5fafb354f6f8688b751" "https://dev.api.cooldoctors.io:8443/DoctorOnDemand/api/patient/followup" -X POST -d '{"subject":null,"content":"Reply message p","senderId":"5ceed13cf893f45b5812b8e1","recipientId":"56fb7614e4b0d3123cea4925","read_status":false,"isDoctor":false}'

```
> The above command returns JSON structured like this:

```json
{
  "id": "5cf243f3f893f42ebcd35688",
  "subject": null,
  "content": "2Uaf9ekG0aDuMY1V8P0dTw==",
  "senderId": "5ceed13cf893f45b5812b8e1",
  "recipientId": "56fb7614e4b0d3123cea4925",
  "parentId": null,
  "timestamp": "2019-06-01 02:22 AM PDT",
  "status": null,
  "read_status": false,
  "appointmentId": null,
  "senderAboutMe": {
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
  "symtons": null,
  "fileId": null,
  "fileName": null,
  "filePath": null,
  "contentTypes": null,
  "senderProfileImage": null,
  "isDoctor": false,
  "recipientAboutMe": {
    "id": "56fb7614e4b0d3123cea4923",
    "firstName": "Dr. John",
    "lastName": "Gelles",
    "birthDate": "xCbUo9+vCO6W+uI8luz3YA==",
    "address": "8L10iLEjsRBVkFaI1gu4bw==",
    "city": "8L10iLEjsRBVkFaI1gu4bw==",
    "country": "rwq24J1FnEhqovLa/bo5uQ==",
    "pincode": "+ffKFHCfLQG2vGeutdG6BQ==",
    "gender": "male",
    "languagesSpeak": [
      "English",
      "",
      ""
    ],
    "additionalInfo": "Hi I plays cricket",
    "state": "tdK26+Dp5ks9TH9wFlmgDA==",
    "lat": null,
    "lang": null
  },
  "recipientProfileImage": "https://s3.amazonaws.com/deveclprofimg/PRDIMAGE/doctor/56fb7614e4b0d3123cea4925/ProfileImage/imgDefault.png",
  "messageType": "withoutAppointment",
  "chatId": "5cf02638f893f4052b1279ce",
  "createdAt": "2019-06-01 02:22 AM PDT",
  "uploadStatus": false,
  "staffId": null,
  "staffAboutMe": null,
  "staffProfileImage": null,
  "staff": false
}

```

> Make sure to replace `X-Auth-Token` with your API key.

Send a new message to a doctor

### HTTP Request

`POST
http://localhost:8080/DoctorOnDemand/api/patient/followup/
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
senderId |  In Sender ID need to pass the logged in user ID in sender | String | Required
recipientId | In Recipient need to pass the doctor ID which one selected from the list of doctors API| String | Required
content |  In Content need to write message | String | Required
subject | Deprecated | String | Optional
read_status | This will always be false | Boolean | Required
isDoctor | Internal use for backend | Boolean | Required


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
messageType | WithoutAppointment or appointment | String
chatId | Chat ID for message | String
createdAt | Created Time | String
uploadStatus | Deprecated | String
staffId | Deprecated | String
staffAboutMe | Deprecated | String
staffProfileImage| Deprecated | String
staff | Deprecated | String


`Authorization: X-Auth-Token`

<aside class="notice">
You must replace <code>X-Auth-Token</code> with your personal API key.
</aside>


## Send file/image to the doctor

```shell

 curl -i -H "Content-Type:application/json" -H "x-auth-token:patientuser1@eyecarelive.com:patient:1561784861568:d5171513ed94a5fafb354f6f8688b751" "https://dev.api.cooldoctors.io:8443/DoctorOnDemand/api/patient/followup/uploadFollowUpMessageFilesInfoIndividual" -X POST -d '{"senderId":"5ceed13cf893f45b5812b8e1","recipientId":"56fb7614e4b0d3123cea4925","read_status":false}'

```
> The above command returns JSON structured like this:

```json
{
  "id": "5cf25d3bf893f42ebcd35a0f",
  "subject": null,
  "content": null,
  "senderId": "5ceed13cf893f45b5812b8e1",
  "recipientId": "56fb7614e4b0d3123cea4925",
  "parentId": null,
  "timestamp": "2019-06-01 04:10 AM PDT",
  "status": null,
  "read_status": false,
  "appointmentId": null,
  "senderAboutMe": {
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
  "symtons": null,
  "fileId": null,
  "fileName": null,
  "filePath": null,
  "contentTypes": null,
  "senderProfileImage": null,
  "isDoctor": false,
  "recipientAboutMe": {
    "id": "56fb7614e4b0d3123cea4923",
    "firstName": "Dr. John",
    "lastName": "Gelles",
    "birthDate": "xCbUo9+vCO6W+uI8luz3YA==",
    "address": "8L10iLEjsRBVkFaI1gu4bw==",
    "city": "8L10iLEjsRBVkFaI1gu4bw==",
    "country": "rwq24J1FnEhqovLa/bo5uQ==",
    "pincode": "+ffKFHCfLQG2vGeutdG6BQ==",
    "gender": "male",
    "languagesSpeak": [
      "English",
      "",
      ""
    ],
    "additionalInfo": "Hi I plays cricket",
    "state": "tdK26+Dp5ks9TH9wFlmgDA==",
    "lat": null,
    "lang": null
  },
  "recipientProfileImage": "https://s3.amazonaws.com/deveclprofimg/PRDIMAGE/doctor/56fb7614e4b0d3123cea4925/ProfileImage/imgDefault.png",
  "messageType": "withoutAppointment",
  "chatId": "5cf02638f893f4052b1279ce",
  "createdAt": "2019-06-01 04:10 AM PDT",
  "uploadStatus": false,
  "staffId": null,
  "staffAboutMe": null,
  "staffProfileImage": null,
  "staff": false
}
```

> Make sure to replace `X-Auth-Token` with your API key.

This is two step API. $URL/uploadFollowUpMessageFilesInfoIndividual/ returns a follow-up id#. This id# is then passed to $URL/uploadFollowUpMessageFilesIndividual/{followupId} to send the file to the doctor as a follow-up message.

### HTTP Request

`POST
http://localhost:8080/DoctorOnDemand/api/patient/followup/uploadFollowUpMessageFilesInfoIndividual
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
senderId |  In Sender ID need to pass the logged in user ID in sender | String | Required
recipientId | In Recipient need to pass the doctor ID which one selected from the list of doctors API| String | Required
read_status | Read messages status | Boolean | Required



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
messageType | WithoutAppointment or appointment | String
chatId | Chat ID for message | String
createdAt | Created Time | String
uploadStatus | Deprecated | String
staffId | Deprecated | String
staffAboutMe | Deprecated | String
staffProfileImage| Deprecated | String
staff | Deprecated | String

`Authorization: X-Auth-Token`

<aside class="notice">
You must replace <code>X-Auth-Token</code> with your personal API key.
</aside>


## Send file via messaging to a doctor

```shell
curl  -i -H "X-Auth-Token:patientuser1@eyecarelive.com:patient:1561784861568:d5171513ed94a5fafb354f6f8688b751" -H "Content-Type:multipart/form-data" "https://dev.api.cooldoctors.io:8443/DoctorOnDemand/api/patient/followup/uploadFollowUpMessageFilesIndividual/5cf25d3bf893f42ebcd35a0f" -X POST -F file=@/Users/admin/Downloads/w3.JPG

```
> The above command returns JSON structured like this:

```json
{
  "id": "5cf25d3bf893f42ebcd35a0f",
  "subject": null,
  "content": null,
  "senderId": "5ceed13cf893f45b5812b8e1",
  "recipientId": "56fb7614e4b0d3123cea4925",
  "parentId": null,
  "timestamp": "2019-06-01 04:10 AM PDT",
  "status": null,
  "read_status": false,
  "appointmentId": null,
  "senderAboutMe": {
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
  "symtons": null,
  "fileId": [
    "1559387619585"
  ],
  "fileName": [
    "w3.JPG"
  ],
  "filePath": [
    "https://s3.amazonaws.com/test-nakul/patient/5ceed13cf893f45b5812b8e1/followUpMessage/1559387619463/w3.JPG"
  ],
  "contentTypes": [
    "image/jpeg"
  ],
  "senderProfileImage": null,
  "isDoctor": false,
  "recipientAboutMe": {
    "id": "56fb7614e4b0d3123cea4923",
    "firstName": "Dr. John",
    "lastName": "Gelles",
    "birthDate": "xCbUo9+vCO6W+uI8luz3YA==",
    "address": "8L10iLEjsRBVkFaI1gu4bw==",
    "city": "8L10iLEjsRBVkFaI1gu4bw==",
    "country": "rwq24J1FnEhqovLa/bo5uQ==",
    "pincode": "+ffKFHCfLQG2vGeutdG6BQ==",
    "gender": "male",
    "languagesSpeak": [
      "English",
      "",
      ""
    ],
    "additionalInfo": "Hi I plays cricket",
    "state": "tdK26+Dp5ks9TH9wFlmgDA==",
    "lat": null,
    "lang": null
  },
  "recipientProfileImage": "https://s3.amazonaws.com/deveclprofimg/PRDIMAGE/doctor/56fb7614e4b0d3123cea4925/ProfileImage/imgDefault.png",
  "messageType": "withoutAppointment",
  "chatId": "5cf02638f893f4052b1279ce",
  "createdAt": "2019-06-01 04:10 AM PDT",
  "uploadStatus": true,
  "staffId": null,
  "staffAboutMe": null,
  "staffProfileImage": null,
  "staff": false
}
```

> Make sure to replace `X-Auth-Token` with your API key.

This is two step API. $URL/uploadFollowUpMessageFilesInfoIndividual/ returns a follow-up id#. This id# is then passed to $URL/uploadFollowUpMessageFilesIndividual/{followupId} to send the file to the doctor as a follow-up message.

### HTTP Request

`POST
http://localhost:8080/DoctorOnDemand/api/patient/followup/uploadFollowUpMessageFilesIndividual
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
senderId |  In Sender ID need to pass the logged in user ID in sender | String | Required
recipientId | In Recipient need to pass the doctor ID which one selected from the list of doctors API| String | Required
Path for file |  Pass the path of file | String | Required



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
messageType | WithoutAppointment or appointment | String
chatId | Chat ID for message | String
createdAt | Created Time | String
uploadStatus | Deprecated | String
staffId | Deprecated | String
staffAboutMe | Deprecated | String
staffProfileImage| Deprecated | String
staff | Deprecated | String


`Authorization: X-Auth-Token`

<aside class="notice">
You must replace <code>X-Auth-Token</code> with your personal API key.
</aside>


## Get view file from messages

```shell
curl -H "X-Auth-Token:patientuser1@eyecarelive.com:patient:1561784861568:d5171513ed94a5fafb354f6f8688b751" -H "Content-Type:multipart/form-data" "https://dev.api.cooldoctors.io:8443/DoctorOnDemand/api/patient/followup/getUrl/1512909942596/5a2d2c5ce4b0e4fa266e02a6"

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




