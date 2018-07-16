# Doctor Messaging

## Get list of messages by patients

```shell
curl -H "X-Auth-Token:doctor@cooldoctors.io:doctor:1515429239598:a0e476b75ffbacedd65e555b5304b222" -H "Content-Type:application/json" "https://api.endpoint.eyecarelive/DoctorOnDemand/api/doctor/followup/getchatuserlist"
```
> The above command returns JSON structured like this:

```json
[
  {
    "id": "5a3b8918e4b096b359a6cbfa",
    "userOne": "5a3b88f0e4b096b359a6cbe4",
    "userTwo": "56fbd63de4b0777c5a04f540",
    "updatedAt": 1513860270001,
    "count": 0,
    "userdetails": {
      "usrOneProfImg": null,
      "usrTwoProfImg": "https://api.endpoint.eyecarelive/PRDIMAGE/doctor/56fbd63de4b0777c5a04f540/ProfileImage/images (18).jpg",
      "usrOneAbtMe": {
        "id": "5a3b88f0e4b096b359a6cbe1",
        "firstName": "Nitin",
        "lastName": "Patil",
        "birthDate": "05/02/1993",
        "address": "pune",
        "city": "pune",
        "country": "USA",
        "pincode": "94649",
        "gender": "Male",
        "languagesSpeak": null,
        "additionalInfo": null,
        "state": "North Carolina"
      },
      "usrTwoAbtMe": {
        "id": "56fbd63de4b0777c5a04f53e",
        "firstName": "Dr. Nitesh",
        "lastName": "Yadav",
        "birthDate": "03/14/2016",
        "address": "1010 W Fremont Ave # 200",
        "city": "Sunnyvale",
        "country": "Indian",
        "pincode": "555555",
        "gender": " Male",
        "languagesSpeak": [
          "English",
          "",
          ""
        ],
        "additionalInfo": null,
        "state": "CA"
      }
    }
  }
]

```

> Make sure to replace `X-Auth-Token` with your API key.

List of all the messages in a conversation with a doctor

### HTTP Request

`POST
http://localhost:8080/DoctorOnDemand/api/doctor/followup/getchatuserlist 
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
Get APi |  It will give the user chat list | Integer | Required



### Response

Parameter | Description | Type
--------- | ----------- | ----
ID | This ID is unique chatID in database | String 
userOne | UserOne will be patientID | String 
userTwo | UserTwo will be patientID | String 
updatedAt | Deprecated | String 
 count| Unread Messages count | String 
userdetails[{}]| UserDetails having patient and doctor profile image | String 
usrOneAbtMe[{}] |This will give the user personal details | String 
usrTwoAbtMe[{}]| This will give the user personal details | String 
 | Same Array response coming for other user after comma. |


`Authorization: X-Auth-Token`

<aside class="notice">
You must replace <code>X-Auth-Token</code> with your personal API key.
</aside>


## Send message


```shell
curl -H "X-Auth-Token:patientuser@cooldoctors.io:doctor:1515429239598:a0e476b75ffbacedd65e555b5304b222" -H "Content-Type:application/json" "http://api.endpoint.eyecarelive/DoctorOnDemand/api/doctor/followup" -X POST -d '{"content":"Hi Jerry, how are you feeling now.?","senderId":"5a2c0a69e4b0e4fa266e0180","recipientId":"58e2268be4b0b3b8e551c825"}'
```
> The above command returns JSON structured like this:

```json
{
  "id": "5a2e876ae4b0e4fa266e226d",
  "subject": null,
  "content": "Hi Jerry, how are you feeling now.?",
  "senderId": "5a2c0a69e4b0e4fa266e0180",
  "recipientId": "58e2268be4b0b3b8e551c825",
  "parentId": null,
  "timestamp": "2017-12-11 05:26 AM PST",
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
  "senderProfileImage": "https://api.endpoint.eyecarelive/PRDIMAGE/doctor/5a2c0a69e4b0e4fa266e0180/ProfileImage/dashboard2.png",
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
    "languagesSpeak": [
      "English",
      "",
      ""
    ],
    "additionalInfo": null,
    "state": "CA"
  },
  "recipientProfileImage": "https://api.endpoint.eyecarelive/PRDIMAGE/doctor/58e2268be4b0b3b8e551c825/ProfileImage/Careers-after-MBA-for-doctor.jpg",
  "messageType": "withoutAppointment",
  "chatId": "5a2d2c1de4b0e4fa266e02a3",
  "createdAt": "2017-12-11 05:26 AM PST"
}
```

> Make sure to replace `X-Auth-Token` with your API key.

Send a new message to a doctor


### HTTP Request

`POST
http://localhost:8080DoctorOnDemand/api/doctor/followup/
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
senderId |  In Sender ID need to pass the logged in user ID in sender | String | Required
recipientId | In Recipient need to pass the doctor ID which one selected from the list of doctors API | String | Required
content | In Content need to write message | String | Required

### Response

Parameter | Description | Type
--------- | ----------- | ----
ID | This ID is database ID | String 
subject | Deprecated | String 
content | Written message content showing | String 
senderId | Sender ID is patient id | String 
 recipientId | Recipient ID is doctors ID  | String 
parentId | Deprecated | String 
timestamp | Message Time | String 
status | Deprecated | String 
 read_status | Message read status | String
appointmentId | If we patient send message on appointment then the Appointment id will return here. | String
senderAboutMe [{}] | Sender about having the sender information | String
recipientAboutMe [{}] | Recipient about having the Recipient information | String
messageType | If that is Appointment wise message then need to pass “withAppointment” & without message “withoutAppointment” | String
chatId | This will chatID | String
createdAt | Deprecated | String


`Authorization: X-Auth-Token`

<aside class="notice">
You must replace <code>X-Auth-Token</code> with your personal API key.
</aside>

## Send file via messaging to a patient 


```shell
 curl -H "X-Auth-Token:patientuser@cooldoctors.io:doctor:1515429239598:a0e476b75ffbacedd65e555b5304b222" -H "Content-Type:application/json" "http://api.endpoint.eyecarelive/DoctorOnDemand/api/doctor/followup/uploadFollowUpMessageFilesInfoIndividual" -X POST -d '{"senderId":"5a2c0a69e4b0e4fa266e0180","recipientId":"58e2268be4b0b3b8e551c825"}'

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
  "senderProfileImage": "https://api.endpoint.eyecarelive/PRDIMAGE/doctor/5a2c0a69e4b0e4fa266e0180/ProfileImage/dashboard2.png",
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
    "languagesSpeak": [
      "English",
      "",
      ""
    ],
    "additionalInfo": null,
    "state": "CA"
  },
  "recipientProfileImage": "https://api.endpoint.eyecarelive/PRDIMAGE/doctor/58e2268be4b0b3b8e551c825/ProfileImage/Careers-after-MBA-for-doctor.jpg",
  "messageType": "withoutAppointment",
  "chatId": "5a2d2c1de4b0e4fa266e02a3",
  "createdAt": "2017-12-11 06:07 AM PST"
}
```



> Make sure to replace `X-Auth-Token` with your API key.

This is two step API. $URL/uploadFollowUpMessageFilesInfoIndividual/ returns a follow-up id#. This id# is then passed to $URL/uploadFollowUpMessageFilesIndividual/{followupId} to send the file to the doctor as a follow-up message.



### HTTP Request

`POST
http://localhost:8080/DoctorOnDemand/api/doctor/followup/uploadFollowUpMessageFilesInfoIndividual/
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
senderId |  Sender ID logged in user | String | Required
recipientId | Recipient ID is doctor ID | String | Required

### Response

Parameter | Description | Type
--------- | ----------- | ----
ID | This ID is database ID | String 
subject | Deprecated | String 
content | Written message content showing | String 
senderId | Sender ID is patient id | String 
 recipientId | Recipient ID is doctors ID  | String 
parentId | Deprecated | String 
timestamp | Message Time | String 
status | Deprecated | String 
 read_status | Message read status | String
appointmentId | If we patient send message on appointment then the Appointment id will return here. | String
senderAboutMe [{}] | Sender about having the sender information | String
recipientAboutMe [{}] | Recipient about having the Recipient information | String
messageType | If that is Appointment wise message then need to pass “withAppointment” & without message “withoutAppointment” | String
chatId | This will chatID | String
createdAt | Deprecated | String
fileId | It will return the file ID for get URL of uploaded photo | String

`Authorization: X-Auth-Token`

<aside class="notice">
You must replace <code>X-Auth-Token</code> with your personal API key.
</aside>

```shell
 curl -H "X-Auth-Token:patientuser@cooldoctors.io:doctor:1515429239598:a0e476b75ffbacedd65e555b5304b222" -H "Content-Type:multipart/form-data" "http://api.endpoint.eyecarelive/DoctorOnDemand/api/doctor/followup/uploadFollowUpMessageFilesIndividual/5a2e9137e4b0e4fa266e23ad" -X POST -F file=@/Users/cupertino/Downloads/dash3.png
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
  "fileId": [
    "1513001430064"
  ],
  "fileName": [
    "dash3.png"
  ],
  "filePath": [
    "https://s3.amazonaws.com/test-nakul/doctor/5a2c0a69e4b0e4fa266e0180/followUpMessage/1513001429942/dash3.png"
  ],
  "contentTypes": [
    "application/octet-stream"
  ],
  "senderProfileImage": "https://api.endpoint.eyecarelive/PRDIMAGE/doctor/5a2c0a69e4b0e4fa266e0180/ProfileImage/dashboard2.png",
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
    "languagesSpeak": [
      "English",
      "",
      ""
    ],
    "additionalInfo": null,
    "state": "CA"
  },
  "recipientProfileImage": "https://api.endpoint.eyecarelive/PRDIMAGE/doctor/58e2268be4b0b3b8e551c825/ProfileImage/Careers-after-MBA-for-doctor.jpg",
  "messageType": "withoutAppointment",
  "chatId": "5a2d2c1de4b0e4fa266e02a3",
  "createdAt": "2017-12-11 06:07 AM PST"
}
```
### HTTP Request

`POST
http://localhost:8080/DoctorOnDemand/api/doctor/followup/uploadFollowUpMessageFilesIndividual/{followupId}
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
{followupId} |  Need to pass follow-up id in the URL | String | Required
-F file=@/FilePath | Need to upload file using API | String | Required

### Response

Parameter | Description | Type
--------- | ----------- | ----
ID | This ID is database ID | String 
subject | Deprecated | String 
content | Written message content showing | String 
senderId | Sender ID is patient id | String 
 recipientId | Recipient ID is doctors ID  | String 
parentId | Deprecated | String 
timestamp | Message Time | String 
status | Deprecated | String 
 read_status | Message read status | String
appointmentId | If we patient send message on appointment then the Appointment id will return here. | String
senderAboutMe [{}] | Sender about having the sender information | String
recipientAboutMe [{}] | Recipient about having the Recipient information | String
messageType | If that is Appointment wise message then need to pass “withAppointment” & without message “withoutAppointment” | String
chatId | This will chatID | String
createdAt | Deprecated | String
fileId | It will return the file ID for get URL of uploaded photo | String

`Authorization: X-Auth-Token`

<aside class="notice">
You must replace <code>X-Auth-Token</code> with your personal API key.
</aside>

## Get view file from messages for doctors

```shell
curl -H "X-Auth-Token:patientuser@cooldoctors.io:doctor:1515429239598:a0e476b75ffbacedd65e555b5304b222" -H "Content-Type:multipart/form-data" "https://api.endpoint.eyecarelive/DoctorOnDemand/api/doctor/followup/getUrl/1512909942596/5a2d2c5ce4b0e4fa266e02a6"

```
> The above command returns JSON structured like this:

```json
{
  "url": "https://d5qf5duw6o0fe.cloudfront.net/doctor/5a2c0a69e4b0e4fa266e0180/followUpMessage/1512909942474/2_user.png?Expires=1512910336&Signature=b4ykk8mvNCpzaGlwg0smiK4LuM-cQ31brqVJ3JoY-n6JC6yunuoS2bnI7lk~zhGF5wE-PKOGG3eIBryPHwkpZBNSSEWPJn8p8IU1plI3qwGewm85PbLqEzlcIBFUeHqQpuEZLaw8EQMv7jcGDInEgiif4rl7SaFF-IHZ3Ix0YTvmTSxPtquZJ6IX~RSBSAjs~7r7qUR-9vyJXjNyC-Dk-r3nW2aJ6b1yyL0ba9kVX8WhHd3WX9heozx6k9by7I7~V8ObKwc0O5DSB3RaM97917r63-TSQK-c44AFCwHLQLxKdvnWhhda67ZaNcxryG1O7txNRMESq-ZZsZCjIxbn7A__&Key-Pair-Id=APKAJKM62WTRWOS5N27Q"
}
```

> Make sure to replace `X-Auth-Token` with your API key.

This API will return the file URL for view. 

### HTTP Request

`POST
http://localhost:8080/DoctorOnDemand/api/doctor/followup/getUrl/1512909942596/5a2d2c5ce4b0e4fa266e02a6
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
{fileID} |  need to pass the file id in the request url | String | Required
{followupID} | need to pass the follow-up id in the request url | String | Required



### Response

Parameter | Description | Type
--------- | ----------- | ----
url | It will return the link for view the image | String 


`Authorization: X-Auth-Token`

<aside class="notice">
You must replace <code>X-Auth-Token</code> with your personal API key.
</aside>


