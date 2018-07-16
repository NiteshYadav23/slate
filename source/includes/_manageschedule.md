
# Manage Schedule


## Create availability

```shell
curl -i -H "Content-Type: application/json" -H "X-Auth-Token:nitesh.yadav@cooldoctors.io:doctor:1515823387217:5beaa02207a3e861e35283011b0dc12a" "http://api.endpoint.eyecarelive.com/DoctorOnDemand/api/doctor/availability" -X POST -d '{"startDate":"2015-06-15 09:44 PM IDT","endDate":"2015-10-15 09:44 PM IDT"}'
 
```
> The above command returns JSON structured like this:

```json
{
  "id": "55dea28ae4b0c34612e032fd",
  "startDate": "2015-06-15 09:44 PM IDT",
  "endDate": "2015-10-15 09:44 PM IDT",
  "doctor": {
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
    "doctorInfo": {
      "id": "55de9ff0e4b0c34612e032fc",
      "educationList": [
        {
          "id": "55de9ff0e4b0c34612e032f7",
          "degree": "BDS",
          "university": "Pune",
          "yearOfPasssing": "2013"
        }
      ],
      "hospitalAttachedWithList": [
        {
          "id": "55de9ff0e4b0c34612e032f8",
          "name": "Pune Sasun hospital",
          "city": "Pune",
          "country": "India"
        }
      ],
      "awardsReceivedList": [
        {
          "id": "55de9ff0e4b0c34612e032f9",
          "name": "Best Doctor",
          "description": "Eye Care",
          "date": "2015-08-27 08:19 AM IDT"
        }
      ],
      "specialities": [
        {
          "id": "55b7802be4b0b393bf91678e",
          "name": "eye care",
          "questionnaire": null,
          "report": null
        }
      ],
      "licencedState": [
        {
          "id": "55de9ff0e4b0c34612e032fa",
          "state": "NY"
        },
        {
          "id": "55de9ff0e4b0c34612e032fb",
          "state": "CA"
        }
      ],
      "registrationNumber": "22222"
    },
    "role": {
      "id": "551ad2ffe4b0b59ff0cceccb",
      "name": "doctor"
    },
    "timezone": null,
    "createdAt": "2015-08-27 08:12 AM IDT",
    "forgotPasswordToken": null,
    "familyMembers": null,
    "parentUser": null,
    "parentUserRelation": null,
    "password": "neethip666",
    "rating": null,
    "preferredPharmacies": null,
    "kandyUserName": null,
    "kandyUserPassword": null,
    "kandyFullUserId": null,
    "oldPassword": null,
    "loginStatus": "Online",
    "stripeCustId": null,
    "profileImagePath": null,
    "isReferredDoctor": null,
    "randomtoken": "ZnwMJq",
    "isEmailVerified": false,
    "invited": false,
    "validated": true,
    "activated": true,
    "managedUser": false
  }
}
```

### HTTP Request

`POST
http://localhost:8080/DoctorOnDemand/api/doctor/availability
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
StartDate | Start date for create availability | String | Required
EndDate | End date for Availability | String | Required

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
Hospital Attached With List :[{}] | Hospital Attached with list | String
Awards Received List | Awards Received List | String
Specialities | Specialities Details | String
Report | Report | String
Role | Role | String


<aside class="info">
Remember - To pass all the required parameters correctly !!
</aside>



## Get Current Weeks Date

```shell
curl -i -H "Content-Type: application/image" -H "X-Auth-Token:nitesh.yadav@cooldoctors.io:doctor:1516431554650:891a3a6e39b7b6e3ab71c1c56e28a7f8" -X GET "http://api.endpoint.eyecarelive.com/DoctorOnDemand/api/doctor/availability/getCurrentWeekDates"

```
> The above command returns JSON structured like this:

```json
[
  "2017-12-17",
  "2017-12-18",
  "2017-12-19",
  "2017-12-20",
  "2017-12-21",
  "2017-12-22",
  "2017-12-23"
]
```

> Make sure to replace `X-Auth-Token` with your API key.

### HTTP Request

`GET
http://localhost:8080/DoctorOnDemand/api/doctor/availability/getCurrentWeekDates
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
Use URL |  Use URL for get the dates | String | Required


### Response

Parameter | Description | Type
--------- | ----------- | ----
Dates[{}] | It will return the dates of current Week | String 


`Authorization: X-Auth-Token`

<aside class="notice">
You must replace <code>X-Auth-Token</code> with your personal API key.
</aside>

## Get Next Week Dates

```shell
curl -i -H "Content-Type: application/image" -H "X-Auth-Token:nitesh.yadav@cooldoctors.io:doctor:1516431554650:891a3a6e39b7b6e3ab71c1c56e28a7f8" -X GET "http://api.endpoint.eyecarelive.com/DoctorOnDemand/api/doctor/availability/getNextWeekDates"


```
> The above command returns JSON structured like this:

```json
[
  "2017-12-24",
  "2017-12-25",
  "2017-12-26",
  "2017-12-27",
  "2017-12-28",
  "2017-12-29",
  "2017-12-30"
]
```

> Make sure to replace `X-Auth-Token` with your API key.

### HTTP Request

`GET
http://localhost:8080/DoctorOnDemand/api/doctor/availability/getNextWeekDates
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
Use URL |  Use URL for get the dates | String | Required


### Response

Parameter | Description | Type
--------- | ----------- | ----
Dates[{}] | It will return the dates of next Week | String 


`Authorization: X-Auth-Token`

<aside class="notice">
You must replace <code>X-Auth-Token</code> with your personal API key.
</aside>

## Get Current Week Availability

```shell
curl -i -H "Content-Type: application/image" -H "X-Auth-Token:nitesh.yadav@cupertinosoft.com:doctor:1516449904639:e8aecb3d4e4e11d6fa2344fb9b628322" -X GET "http://api.endpoint.eyecarelive.com/DoctorOnDemand/api/doctor/availability/getAvailabilityOfCurrentWeek"
```
> The above command returns JSON structured like this:

```json
[
  {
    "id": "5a2e5bdce4b0e4fa266e1683",
    "startDate": "2017-12-17",
    "endDate": null,
    "doctor": {
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
        "languagesSpeak": [
          "English",
          "",
          ""
        ],
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
        "educationList": [
          {
            "id": "59e09cbce4b0a70b0de5b0c3",
            "degree": "Bca",
            "university": "un",
            "yearOfPasssing": "88778"
          }
        ],
        "hospitalAttachedWithList": [
          {
            "id": "59e09cbce4b0a70b0de5b0c4",
            "name": "tt",
            "city": "Pune",
            "country": "India"
          }
        ],
        "awardsReceivedList": [
          {
            "id": "59e09cbce4b0a70b0de5b0c5",
            "name": "q",
            "description": "Description",
            "date": "11/11/1991"
          }
        ],
        "specialities": [
          {
            "id": "55b78065e4b0b393bf91678f",
            "name": "general physician",
            "questionnaire": null,
            "report": null
          }
        ],
        "licencedState": [
          {
            "id": "5665a2cb9a87399fa0b9ba33",
            "state": "AL"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba34",
            "state": "AK"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba35",
            "state": "AZ"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba37",
            "state": "CA"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba40",
            "state": "IL"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba41",
            "state": "IN"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba42",
            "state": "IA"
          }
        ],
        "registrationNumber": "22222",
        "whyCoolDoctors": null,
        "bio": "",
        "profession": "Optometrist",
        "availabilityTimeZone": "Asia/Kolkata",
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
      "preferredPharmacies": null,
      "kandyUserName": "kandyuser2",
      "kandyUserPassword": "demo1234",
      "kandyFullUserId": "kandyuser2@neet.cupertinosoft.com",
      "oldPassword": null,
      "loginStatus": "Online",
      "stripeCustId": null,
      "profileImagePath": "https://api.endpoint.eyecarelive.com/PRDIMAGE/doctor/56fb7614e4b0d3123cea4925/ProfileImage/paulsupe232.png",
      "isReferredDoctor": null,
      "randomtoken": "esnckN",
      "isEmailVerified": false,
      "doctorsGroups": [
        {
          "id": "56d01388e4b0cd1739f0e076",
          "groupName": "Silicon Valley Eye Physicians"
        }
      ],
      "preferredDoctors": [
        "56fbd63de4b0777c5a04f540",
        "595a0d97e4b0c065c25684ea"
      ],
      "isAcceptTC": true,
      "insurenceCards": null,
      "notificationSettings": null,
      "clinics": [
        "58f9d4a7e4b07023de8c0d64"
      ],
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
      "twilioAccessToken": "eyJjdHkiOiJ0d2lsaW8tZnBhO3Y9MSIsInR5cCI6IkpXVCIsImFsZyI6IkhTMjU2In0.eyJpc3MiOiJTS2NmMTBhNzcwZmU1MzI4MDQxYjJkNDFiNjc0ODE0YzBlIiwiZXhwIjoxNTEzNzY5Mjk2LCJncmFudHMiOnsiaWRlbnRpdHkiOiI1NmZiNzYxNGU0YjBkMzEyM2NlYTQ5MjUiLCJ2aWRlbyI6eyJyb29tIjoiNTZmYjc2MTRlNGIwZDMxMjNjZWE0OTI1NTZmYmQ2M2RlNGIwNzc3YzVhMDRmNTQwIn19LCJqdGkiOiJTS2NmMTBhNzcwZmU1MzI4MDQxYjJkNDFiNjc0ODE0YzBlLTE1MTM3NjU3NjAiLCJzdWIiOiJBQ2NhNGYyNmM3ODRhM2U5NWU3NDY3ZjRhZGMwMDMwYjFkIn0.1Xj4UMnl6VddKk--HbVYUCSEq5_wlmH0oRrDjVPFmcM",
      "invited": false,
      "validated": true,
      "activated": true,
      "managedUser": false,
      "addedByCpm": false,
      "pilotDoc": true
    },
    "startTimes": [
      "17",
      "18"
    ],
    "availabilityTimeSlots": [
      {
        "id": "5a2e5bdce4b0e4fa266e167d",
        "startTime": "17",
        "sTime": "2017-12-17 05:30 PM IST",
        "eTime": "2017-12-17 05:40 PM IST",
        "slotNumber": "0",
        "patient": null,
        "visitType": null,
        "appointmentId": null,
        "status": "enable",
        "booked": false
      },
      {
        "id": "5a2e5bdce4b0e4fa266e167e",
        "startTime": "17",
        "sTime": "2017-12-17 05:40 PM IST",
        "eTime": "2017-12-17 05:50 PM IST",
        "slotNumber": "1",
        "patient": null,
        "visitType": null,
        "appointmentId": null,
        "status": "enable",
        "booked": false
      },
      {
        "id": "5a2e5bdce4b0e4fa266e167f",
        "startTime": "17",
        "sTime": "2017-12-17 05:50 PM IST",
        "eTime": "2017-12-17 06:00 PM IST",
        "slotNumber": "2",
        "patient": null,
        "visitType": null,
        "appointmentId": "5a2e65fee4b0e4fa266e1bb5",
        "status": "enable",
        "booked": true
      },
      {
        "id": "5a2e5bdce4b0e4fa266e1680",
        "startTime": "18",
        "sTime": "2017-12-17 06:00 PM IST",
        "eTime": "2017-12-17 06:10 PM IST",
        "slotNumber": "3",
        "patient": {
          "id": "56d43a35e4b03a2da3a131f2",
          "email": "mit4079@gmail.com",
          "pharmacyName": null,
          "pharmacyAddress": null,
          "profileImageId": null,
          "profileImageName": null,
          "aboutMe": {
            "id": "56d43a35e4b03a2da3a131f0",
            "firstName": "mitesh",
            "lastName": "patil",
            "birthDate": "10/20/1984",
            "address": "mitesh",
            "city": "pune",
            "country": "USA",
            "pincode": "40010",
            "gender": "Male",
            "languagesSpeak": null,
            "additionalInfo": null,
            "state": "Arizona"
          },
          "contactInfo": {
            "id": "56d43a35e4b03a2da3a131f1",
            "email": "mit4079@gmail.com",
            "phone": "8806900744",
            "smsNotification": false,
            "countryCode": null,
            "country": null,
            "emlNt": true
          },
          "patientInfo": {
            "id": "5829d506e4b004f0f79c5df4",
            "lifeStyle": {
              "id": "5829d506e4b004f0f79c5df2",
              "medication": "G",
              "alcoholUse": "Yes",
              "allergiesToMedication": "The ",
              "alcoholDrinksPerWeek": "1-6",
              "medicalCondition": "RetinaDisease",
              "allergies": "",
              "vitaminSupplements": "",
              "smoke": "",
              "contactlenses": ""
            },
            "familyHistory": {
              "id": "5829d506e4b004f0f79c5df3",
              "description": null,
              "diseaseRelation": [
                {
                  "conditions": "Cancer",
                  "relationship": "Grand Father"
                },
                {
                  "conditions": "Diabetes",
                  "relationship": "Sister"
                }
              ]
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
          "createdAt": "2016-02-29 04:31 AM PST",
          "forgotPasswordToken": "5828",
          "familyMembers": [
            {
              "id": "592564b0e4b0a6e0d233b106",
              "email": "4G7yFUhb@eyecarelive.com",
              "pharmacyName": null,
              "pharmacyAddress": null,
              "profileImageId": null,
              "profileImageName": null,
              "aboutMe": {
                "id": "592564b0e4b0a6e0d233b104",
                "firstName": "Test",
                "lastName": "User",
                "birthDate": "01/01/1990",
                "address": "Pune",
                "city": "Pune",
                "country": "India",
                "pincode": "411045",
                "gender": "Male",
                "languagesSpeak": null,
                "additionalInfo": null,
                "state": "Mh"
              },
              "contactInfo": {
                "id": "592564b0e4b0a6e0d233b105",
                "email": "mit4079@gmail.com",
                "phone": "123456788922",
                "smsNotification": false,
                "countryCode": null,
                "country": null,
                "emlNt": true
              },
              "patientInfo": {
                "id": "592564dfe4b0a6e0d233b115",
                "lifeStyle": {
                  "id": "592564dfe4b0a6e0d233b113",
                  "medication": "",
                  "alcoholUse": "No",
                  "allergiesToMedication": "",
                  "alcoholDrinksPerWeek": "",
                  "medicalCondition": "",
                  "allergies": "",
                  "vitaminSupplements": "",
                  "smoke": "",
                  "contactlenses": ""
                },
                "familyHistory": {
                  "id": "592564dfe4b0a6e0d233b114",
                  "description": null,
                  "diseaseRelation": []
                }
              },
              "doctorInfo": null,
              "role": {
                "id": "551ad2a4e4b0b59ff0ccecc9",
                "name": "patient"
              },
              "timezone": null,
              "createdAt": "2017-05-24 03:47 AM PDT",
              "forgotPasswordToken": null,
              "familyMembers": null,
              "parentUser": null,
              "parentUserRelation": "Brother",
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
              "doctorsOrg": {
                "id": "59cb542de4b0fa09b42591b5",
                "orgName": "EyecareLive"
              },
              "twilioAccessToken": null,
              "invited": false,
              "validated": true,
              "activated": true,
              "managedUser": true,
              "addedByCpm": false,
              "pilotDoc": true
            }
          ],
          "parentUser": null,
          "parentUserRelation": null,
          "password": null,
          "rating": null,
          "preferredPharmacies": [
            {
              "id": "570fbd67e4b0f71644c1e826",
              "name": "Medicalstore",
              "address": "The Crest",
              "email": null,
              "city": "Pune",
              "state": "Arizona",
              "country": "US",
              "zipCode": "94087",
              "phoneNumber": "8806900740",
              "validated": false
            }
          ],
          "kandyUserName": null,
          "kandyUserPassword": null,
          "kandyFullUserId": null,
          "oldPassword": null,
          "loginStatus": "Online",
          "stripeCustId": "5FCRx5zxyC3FPWxu+t5dN+ICEy4GMn/cugsGDAbj8so=",
          "profileImagePath": "https://demo.cooldoctors.io/PRDIMAGE/doctor/56d43a35e4b03a2da3a131f2/ProfileImage/IMG-20160822-WA0006.jpg",
          "isReferredDoctor": null,
          "randomtoken": "9qJTq3",
          "isEmailVerified": false,
          "doctorsGroups": null,
          "preferredDoctors": [
            "56fb7614e4b0d3123cea4925"
          ],
          "isAcceptTC": false,
          "insurenceCards": [
            {
              "name": "Mycard",
              "files": [
                "1476513111882,https://s3.amazonaws.com/test-nakul/doctor/56d43a35e4b03a2da3a131f2/insurencecard/1476513111882/picture-128647430.jpg",
                "1476513112165,https://s3.amazonaws.com/test-nakul/doctor/56d43a35e4b03a2da3a131f2/insurencecard/1476513112165/picture-1441534918.jpg"
              ],
              "memberId": null,
              "payerId": null
            },
            {
              "name": "Newcard",
              "files": [
                "1476513225315,https://s3.amazonaws.com/test-nakul/doctor/56d43a35e4b03a2da3a131f2/insurencecard/1476513225315/picture2140479387.jpg",
                "1476513225483,https://s3.amazonaws.com/test-nakul/doctor/56d43a35e4b03a2da3a131f2/insurencecard/1476513225483/picture764634243.jpg"
              ],
              "memberId": null,
              "payerId": null
            },
            {
              "name": "Testcard",
              "files": [
                "1476513752614,https://s3.amazonaws.com/test-nakul/doctor/56d43a35e4b03a2da3a131f2/insurencecard/1476513752614/picture-1112636549.jpg",
                "1476513752716,https://s3.amazonaws.com/test-nakul/doctor/56d43a35e4b03a2da3a131f2/insurencecard/1476513752716/picture-223484632.jpg"
              ],
              "memberId": null,
              "payerId": null
            }
          ],
          "notificationSettings": null,
          "clinics": null,
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
          "twilioAccessToken": "eyJjdHkiOiJ0d2lsaW8tZnBhO3Y9MSIsInR5cCI6IkpXVCIsImFsZyI6IkhTMjU2In0.eyJpc3MiOiJTS2NmMTBhNzcwZmU1MzI4MDQxYjJkNDFiNjc0ODE0YzBlIiwiZXhwIjoxNTEzMDAzODk0LCJncmFudHMiOnsiaWRlbnRpdHkiOiI1NmQ0M2EzNWU0YjAzYTJkYTNhMTMxZjIiLCJ2aWRlbyI6eyJyb29tIjoiNTZmYmQ2M2RlNGIwNzc3YzVhMDRmNTQwNTZkNDNhMzVlNGIwM2EyZGEzYTEzMWYyIn19LCJqdGkiOiJTS2NmMTBhNzcwZmU1MzI4MDQxYjJkNDFiNjc0ODE0YzBlLTE1MTMwMDAzMjAiLCJzdWIiOiJBQ2NhNGYyNmM3ODRhM2U5NWU3NDY3ZjRhZGMwMDMwYjFkIn0.UucOp-VpCqlac5L7a8Fp9uXk5oTS1qBxr8-cQhb_BHI",
          "invited": false,
          "validated": true,
          "activated": true,
          "managedUser": false,
          "addedByCpm": false,
          "pilotDoc": true
        },
        "visitType": "normalsymtons",
        "appointmentId": "5a326cc4e4b006dea379f389",
        "status": "enable",
        "booked": true
      },
      {
        "id": "5a2e5bdce4b0e4fa266e1681",
        "startTime": "18",
        "sTime": "2017-12-17 06:10 PM IST",
        "eTime": "2017-12-17 06:20 PM IST",
        "slotNumber": "4",
        "patient": null,
        "visitType": null,
        "appointmentId": null,
        "status": "enable",
        "booked": false
      },
      {
        "id": "5a2e5bdce4b0e4fa266e1682",
        "startTime": "18",
        "sTime": "2017-12-17 06:20 PM IST",
        "eTime": "2017-12-17 06:30 PM IST",
        "slotNumber": "5",
        "patient": null,
        "visitType": null,
        "appointmentId": null,
        "status": "enable",
        "booked": false
      }
    ],
    "status": null
  }
]
```

> Make sure to replace `X-Auth-Token` with your API key. 

### HTTP Request

`GET
http://localhost:8080/DoctorOnDemand/api/doctor/availability/getAvailabilityOfCurrentWeek
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
Use URL |  Use URL to get the dates | String | Required


### Response

Parameter | Description | Type
--------- | ----------- | ----
ID | ID created by database | String 
startDate | Start Date about availability | String
endDate | End Date about availability | String
doctor[{}] | Doctor information  | String
aboutMe[{}] | Doctor’s about information  | String
contactInfo[{}] | Doctor’s contact information | String
patientInfo[{}] | Patient info  Deprecated  | String
doctorInfo[{}] | Doctor’s info  | String
specialities[{}] | Specialities ID always be fixed | String
licencedState[{}] | Licensed states of doctor’s | String
role[{}] | Role ID always be a fixed ID for doctor’s | String
timezone[{}] | Doctor’s Time zone  | String
createdAt[{}] | End Date about availability | String
forgotPasswordToken[{}] | Forgot password token created | String
familyMembers[{}] | Family member data | String
parentUser[{}] | Parent user Deprecated | String
parentUserRelation[{}] | Parent user Deprecated | String
password[{}] | Deprecated | String
rating[{}] | Deprecated | String
preferredPharmacies[{}] | Deprecated | String
profileImagePath | Doctor’s image path | String
randomtoken | Deprecated | String
doctorsGroups[{}] | Doctor’s Group  | String
preferredDoctors[{}] | Deprecated | String
clinics[{}] | Deprecated | String
doctorsOrg[{}] | Deprecated | String
twilioAccessToken | Deprecated | String
startTimes | Deprecated | String
 | availabilityTimeSlot |
id | ID of availability  | String
startTime | Start time  | String
sTime | Stime is date of availability  | String
eTime | Etime is data of availability  | String
slotNumber | Slot number  | String
patient | Deprecated | String
visitType | Deprecated | String
appointmentId | Deprecated | String
status | “Enable” | String
booked | True & false | String
 | Other All parameter which is not mentioned that all “Deprecated” | 

`Authorization: X-Auth-Token`

<aside class="notice">
You must replace <code>X-Auth-Token</code> with your personal API key.
</aside>

## Get Next Week Availability

```shell
curl -i -H "Content-Type: application/image" -H "X-Auth-Token:nitesh.yadav@cupertinosoft.com:doctor:1516449904639:e8aecb3d4e4e11d6fa2344fb9b628322" -X GET "http://api.endpoint.eyecarelive.com/DoctorOnDemand/api/doctor/availability/getAvailabilityOfNextWeek"


```
> The above command returns JSON structured like this:

```json
[
  {
    "id": "5a3ba4c1e4b096b359a6ce1f",
    "startDate": "2017-12-24",
    "endDate": null,
    "doctor": {
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
        "languagesSpeak": [
          "English",
          "",
          ""
        ],
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
        "educationList": [
          {
            "id": "59e09cbce4b0a70b0de5b0c3",
            "degree": "Bca",
            "university": "un",
            "yearOfPasssing": "88778"
          }
        ],
        "hospitalAttachedWithList": [
          {
            "id": "59e09cbce4b0a70b0de5b0c4",
            "name": "tt",
            "city": "Pune",
            "country": "India"
          }
        ],
        "awardsReceivedList": [
          {
            "id": "59e09cbce4b0a70b0de5b0c5",
            "name": "q",
            "description": "Description",
            "date": "11/11/1991"
          }
        ],
        "specialities": [
          {
            "id": "55b78065e4b0b393bf91678f",
            "name": "general physician",
            "questionnaire": null,
            "report": null
          }
        ],
        "licencedState": [
          {
            "id": "5665a2cb9a87399fa0b9ba33",
            "state": "AL"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba34",
            "state": "AK"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba35",
            "state": "AZ"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba37",
            "state": "CA"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba40",
            "state": "IL"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba41",
            "state": "IN"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba42",
            "state": "IA"
          }
        ],
        "registrationNumber": "22222",
        "whyCoolDoctors": null,
        "bio": "",
        "profession": "Optometrist",
        "availabilityTimeZone": "Asia/Kolkata",
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
      "preferredPharmacies": null,
      "kandyUserName": "kandyuser2",
      "kandyUserPassword": "demo1234",
      "kandyFullUserId": "kandyuser2@neet.cupertinosoft.com",
      "oldPassword": null,
      "loginStatus": "Online",
      "stripeCustId": null,
      "profileImagePath": "https://api.endpoint.eyecarelive.com/PRDIMAGE/doctor/56fb7614e4b0d3123cea4925/ProfileImage/paulsupe232.png",
      "isReferredDoctor": null,
      "randomtoken": "esnckN",
      "isEmailVerified": false,
      "doctorsGroups": [
        {
          "id": "56d01388e4b0cd1739f0e076",
          "groupName": "Silicon Valley Eye Physicians"
        }
      ],
      "preferredDoctors": [
        "56fbd63de4b0777c5a04f540",
        "595a0d97e4b0c065c25684ea"
      ],
      "isAcceptTC": true,
      "insurenceCards": null,
      "notificationSettings": null,
      "clinics": [
        "58f9d4a7e4b07023de8c0d64"
      ],
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
      "twilioAccessToken": "eyJjdHkiOiJ0d2lsaW8tZnBhO3Y9MSIsInR5cCI6IkpXVCIsImFsZyI6IkhTMjU2In0.eyJpc3MiOiJTS2NmMTBhNzcwZmU1MzI4MDQxYjJkNDFiNjc0ODE0YzBlIiwiZXhwIjoxNTEzNzY5Mjk2LCJncmFudHMiOnsiaWRlbnRpdHkiOiI1NmZiNzYxNGU0YjBkMzEyM2NlYTQ5MjUiLCJ2aWRlbyI6eyJyb29tIjoiNTZmYjc2MTRlNGIwZDMxMjNjZWE0OTI1NTZmYmQ2M2RlNGIwNzc3YzVhMDRmNTQwIn19LCJqdGkiOiJTS2NmMTBhNzcwZmU1MzI4MDQxYjJkNDFiNjc0ODE0YzBlLTE1MTM3NjU3NjAiLCJzdWIiOiJBQ2NhNGYyNmM3ODRhM2U5NWU3NDY3ZjRhZGMwMDMwYjFkIn0.1Xj4UMnl6VddKk--HbVYUCSEq5_wlmH0oRrDjVPFmcM",
      "invited": false,
      "validated": true,
      "activated": true,
      "managedUser": false,
      "addedByCpm": false,
      "pilotDoc": true
    },
    "startTimes": null,
    "availabilityTimeSlots": null,
    "status": null
  },
  {
    "id": "5a3ba4c1e4b096b359a6ce26",
    "startDate": "2017-12-25",
    "endDate": null,
    "doctor": {
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
        "languagesSpeak": [
          "English",
          "",
          ""
        ],
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
        "educationList": [
          {
            "id": "59e09cbce4b0a70b0de5b0c3",
            "degree": "Bca",
            "university": "un",
            "yearOfPasssing": "88778"
          }
        ],
        "hospitalAttachedWithList": [
          {
            "id": "59e09cbce4b0a70b0de5b0c4",
            "name": "tt",
            "city": "Pune",
            "country": "India"
          }
        ],
        "awardsReceivedList": [
          {
            "id": "59e09cbce4b0a70b0de5b0c5",
            "name": "q",
            "description": "Description",
            "date": "11/11/1991"
          }
        ],
        "specialities": [
          {
            "id": "55b78065e4b0b393bf91678f",
            "name": "general physician",
            "questionnaire": null,
            "report": null
          }
        ],
        "licencedState": [
          {
            "id": "5665a2cb9a87399fa0b9ba33",
            "state": "AL"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba34",
            "state": "AK"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba35",
            "state": "AZ"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba37",
            "state": "CA"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba40",
            "state": "IL"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba41",
            "state": "IN"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba42",
            "state": "IA"
          }
        ],
        "registrationNumber": "22222",
        "whyCoolDoctors": null,
        "bio": "",
        "profession": "Optometrist",
        "availabilityTimeZone": "Asia/Kolkata",
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
      "preferredPharmacies": null,
      "kandyUserName": "kandyuser2",
      "kandyUserPassword": "demo1234",
      "kandyFullUserId": "kandyuser2@neet.cupertinosoft.com",
      "oldPassword": null,
      "loginStatus": "Online",
      "stripeCustId": null,
      "profileImagePath": "https://api.endpoint.eyecarelive.com/PRDIMAGE/doctor/56fb7614e4b0d3123cea4925/ProfileImage/paulsupe232.png",
      "isReferredDoctor": null,
      "randomtoken": "esnckN",
      "isEmailVerified": false,
      "doctorsGroups": [
        {
          "id": "56d01388e4b0cd1739f0e076",
          "groupName": "Silicon Valley Eye Physicians"
        }
      ],
      "preferredDoctors": [
        "56fbd63de4b0777c5a04f540",
        "595a0d97e4b0c065c25684ea"
      ],
      "isAcceptTC": true,
      "insurenceCards": null,
      "notificationSettings": null,
      "clinics": [
        "58f9d4a7e4b07023de8c0d64"
      ],
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
      "twilioAccessToken": "eyJjdHkiOiJ0d2lsaW8tZnBhO3Y9MSIsInR5cCI6IkpXVCIsImFsZyI6IkhTMjU2In0.eyJpc3MiOiJTS2NmMTBhNzcwZmU1MzI4MDQxYjJkNDFiNjc0ODE0YzBlIiwiZXhwIjoxNTEzNzY5Mjk2LCJncmFudHMiOnsiaWRlbnRpdHkiOiI1NmZiNzYxNGU0YjBkMzEyM2NlYTQ5MjUiLCJ2aWRlbyI6eyJyb29tIjoiNTZmYjc2MTRlNGIwZDMxMjNjZWE0OTI1NTZmYmQ2M2RlNGIwNzc3YzVhMDRmNTQwIn19LCJqdGkiOiJTS2NmMTBhNzcwZmU1MzI4MDQxYjJkNDFiNjc0ODE0YzBlLTE1MTM3NjU3NjAiLCJzdWIiOiJBQ2NhNGYyNmM3ODRhM2U5NWU3NDY3ZjRhZGMwMDMwYjFkIn0.1Xj4UMnl6VddKk--HbVYUCSEq5_wlmH0oRrDjVPFmcM",
      "invited": false,
      "validated": true,
      "activated": true,
      "managedUser": false,
      "addedByCpm": false,
      "pilotDoc": true
    },
    "startTimes": [
      "06",
      "07"
    ],
    "availabilityTimeSlots": [
      {
        "id": "5a3ba4c1e4b096b359a6ce20",
        "startTime": "06",
        "sTime": "2017-12-26 06:30 AM IST",
        "eTime": "2017-12-26 06:40 AM IST",
        "slotNumber": "0",
        "patient": null,
        "visitType": null,
        "appointmentId": null,
        "status": "enable",
        "booked": false
      },
      {
        "id": "5a3ba4c1e4b096b359a6ce21",
        "startTime": "06",
        "sTime": "2017-12-26 06:40 AM IST",
        "eTime": "2017-12-26 06:50 AM IST",
        "slotNumber": "1",
        "patient": null,
        "visitType": null,
        "appointmentId": null,
        "status": "enable",
        "booked": false
      },
      {
        "id": "5a3ba4c1e4b096b359a6ce22",
        "startTime": "06",
        "sTime": "2017-12-26 06:50 AM IST",
        "eTime": "2017-12-26 07:00 AM IST",
        "slotNumber": "2",
        "patient": null,
        "visitType": null,
        "appointmentId": null,
        "status": "enable",
        "booked": false
      },
      {
        "id": "5a3ba4c1e4b096b359a6ce23",
        "startTime": "07",
        "sTime": "2017-12-26 07:00 AM IST",
        "eTime": "2017-12-26 07:10 AM IST",
        "slotNumber": "3",
        "patient": null,
        "visitType": null,
        "appointmentId": null,
        "status": "enable",
        "booked": false
      },
      {
        "id": "5a3ba4c1e4b096b359a6ce24",
        "startTime": "07",
        "sTime": "2017-12-26 07:10 AM IST",
        "eTime": "2017-12-26 07:20 AM IST",
        "slotNumber": "4",
        "patient": null,
        "visitType": null,
        "appointmentId": null,
        "status": "enable",
        "booked": false
      },
      {
        "id": "5a3ba4c1e4b096b359a6ce25",
        "startTime": "07",
        "sTime": "2017-12-26 07:20 AM IST",
        "eTime": "2017-12-26 07:30 AM IST",
        "slotNumber": "5",
        "patient": null,
        "visitType": null,
        "appointmentId": null,
        "status": "enable",
        "booked": false
      }
    ],
    "status": null
  },
  {
    "id": "5a3ba4c1e4b096b359a6ce27",
    "startDate": "2017-12-26",
    "endDate": null,
    "doctor": {
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
        "languagesSpeak": [
          "English",
          "",
          ""
        ],
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
        "educationList": [
          {
            "id": "59e09cbce4b0a70b0de5b0c3",
            "degree": "Bca",
            "university": "un",
            "yearOfPasssing": "88778"
          }
        ],
        "hospitalAttachedWithList": [
          {
            "id": "59e09cbce4b0a70b0de5b0c4",
            "name": "tt",
            "city": "Pune",
            "country": "India"
          }
        ],
        "awardsReceivedList": [
          {
            "id": "59e09cbce4b0a70b0de5b0c5",
            "name": "q",
            "description": "Description",
            "date": "11/11/1991"
          }
        ],
        "specialities": [
          {
            "id": "55b78065e4b0b393bf91678f",
            "name": "general physician",
            "questionnaire": null,
            "report": null
          }
        ],
        "licencedState": [
          {
            "id": "5665a2cb9a87399fa0b9ba33",
            "state": "AL"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba34",
            "state": "AK"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba35",
            "state": "AZ"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba37",
            "state": "CA"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba40",
            "state": "IL"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba41",
            "state": "IN"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba42",
            "state": "IA"
          }
        ],
        "registrationNumber": "22222",
        "whyCoolDoctors": null,
        "bio": "",
        "profession": "Optometrist",
        "availabilityTimeZone": "Asia/Kolkata",
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
      "preferredPharmacies": null,
      "kandyUserName": "kandyuser2",
      "kandyUserPassword": "demo1234",
      "kandyFullUserId": "kandyuser2@neet.cupertinosoft.com",
      "oldPassword": null,
      "loginStatus": "Online",
      "stripeCustId": null,
      "profileImagePath": "https://api.endpoint.eyecarelive.com/PRDIMAGE/doctor/56fb7614e4b0d3123cea4925/ProfileImage/paulsupe232.png",
      "isReferredDoctor": null,
      "randomtoken": "esnckN",
      "isEmailVerified": false,
      "doctorsGroups": [
        {
          "id": "56d01388e4b0cd1739f0e076",
          "groupName": "Silicon Valley Eye Physicians"
        }
      ],
      "preferredDoctors": [
        "56fbd63de4b0777c5a04f540",
        "595a0d97e4b0c065c25684ea"
      ],
      "isAcceptTC": true,
      "insurenceCards": null,
      "notificationSettings": null,
      "clinics": [
        "58f9d4a7e4b07023de8c0d64"
      ],
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
      "twilioAccessToken": "eyJjdHkiOiJ0d2lsaW8tZnBhO3Y9MSIsInR5cCI6IkpXVCIsImFsZyI6IkhTMjU2In0.eyJpc3MiOiJTS2NmMTBhNzcwZmU1MzI4MDQxYjJkNDFiNjc0ODE0YzBlIiwiZXhwIjoxNTEzNzY5Mjk2LCJncmFudHMiOnsiaWRlbnRpdHkiOiI1NmZiNzYxNGU0YjBkMzEyM2NlYTQ5MjUiLCJ2aWRlbyI6eyJyb29tIjoiNTZmYjc2MTRlNGIwZDMxMjNjZWE0OTI1NTZmYmQ2M2RlNGIwNzc3YzVhMDRmNTQwIn19LCJqdGkiOiJTS2NmMTBhNzcwZmU1MzI4MDQxYjJkNDFiNjc0ODE0YzBlLTE1MTM3NjU3NjAiLCJzdWIiOiJBQ2NhNGYyNmM3ODRhM2U5NWU3NDY3ZjRhZGMwMDMwYjFkIn0.1Xj4UMnl6VddKk--HbVYUCSEq5_wlmH0oRrDjVPFmcM",
      "invited": false,
      "validated": true,
      "activated": true,
      "managedUser": false,
      "addedByCpm": false,
      "pilotDoc": true
    },
    "startTimes": null,
    "availabilityTimeSlots": null,
    "status": null
  },
  {
    "id": "5a3ba4c1e4b096b359a6ce28",
    "startDate": "2017-12-27",
    "endDate": null,
    "doctor": {
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
        "languagesSpeak": [
          "English",
          "",
          ""
        ],
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
        "educationList": [
          {
            "id": "59e09cbce4b0a70b0de5b0c3",
            "degree": "Bca",
            "university": "un",
            "yearOfPasssing": "88778"
          }
        ],
        "hospitalAttachedWithList": [
          {
            "id": "59e09cbce4b0a70b0de5b0c4",
            "name": "tt",
            "city": "Pune",
            "country": "India"
          }
        ],
        "awardsReceivedList": [
          {
            "id": "59e09cbce4b0a70b0de5b0c5",
            "name": "q",
            "description": "Description",
            "date": "11/11/1991"
          }
        ],
        "specialities": [
          {
            "id": "55b78065e4b0b393bf91678f",
            "name": "general physician",
            "questionnaire": null,
            "report": null
          }
        ],
        "licencedState": [
          {
            "id": "5665a2cb9a87399fa0b9ba33",
            "state": "AL"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba34",
            "state": "AK"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba35",
            "state": "AZ"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba37",
            "state": "CA"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba40",
            "state": "IL"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba41",
            "state": "IN"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba42",
            "state": "IA"
          }
        ],
        "registrationNumber": "22222",
        "whyCoolDoctors": null,
        "bio": "",
        "profession": "Optometrist",
        "availabilityTimeZone": "Asia/Kolkata",
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
      "preferredPharmacies": null,
      "kandyUserName": "kandyuser2",
      "kandyUserPassword": "demo1234",
      "kandyFullUserId": "kandyuser2@neet.cupertinosoft.com",
      "oldPassword": null,
      "loginStatus": "Online",
      "stripeCustId": null,
      "profileImagePath": "https://api.endpoint.eyecarelive.com/PRDIMAGE/doctor/56fb7614e4b0d3123cea4925/ProfileImage/paulsupe232.png",
      "isReferredDoctor": null,
      "randomtoken": "esnckN",
      "isEmailVerified": false,
      "doctorsGroups": [
        {
          "id": "56d01388e4b0cd1739f0e076",
          "groupName": "Silicon Valley Eye Physicians"
        }
      ],
      "preferredDoctors": [
        "56fbd63de4b0777c5a04f540",
        "595a0d97e4b0c065c25684ea"
      ],
      "isAcceptTC": true,
      "insurenceCards": null,
      "notificationSettings": null,
      "clinics": [
        "58f9d4a7e4b07023de8c0d64"
      ],
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
      "twilioAccessToken": "eyJjdHkiOiJ0d2lsaW8tZnBhO3Y9MSIsInR5cCI6IkpXVCIsImFsZyI6IkhTMjU2In0.eyJpc3MiOiJTS2NmMTBhNzcwZmU1MzI4MDQxYjJkNDFiNjc0ODE0YzBlIiwiZXhwIjoxNTEzNzY5Mjk2LCJncmFudHMiOnsiaWRlbnRpdHkiOiI1NmZiNzYxNGU0YjBkMzEyM2NlYTQ5MjUiLCJ2aWRlbyI6eyJyb29tIjoiNTZmYjc2MTRlNGIwZDMxMjNjZWE0OTI1NTZmYmQ2M2RlNGIwNzc3YzVhMDRmNTQwIn19LCJqdGkiOiJTS2NmMTBhNzcwZmU1MzI4MDQxYjJkNDFiNjc0ODE0YzBlLTE1MTM3NjU3NjAiLCJzdWIiOiJBQ2NhNGYyNmM3ODRhM2U5NWU3NDY3ZjRhZGMwMDMwYjFkIn0.1Xj4UMnl6VddKk--HbVYUCSEq5_wlmH0oRrDjVPFmcM",
      "invited": false,
      "validated": true,
      "activated": true,
      "managedUser": false,
      "addedByCpm": false,
      "pilotDoc": true
    },
    "startTimes": null,
    "availabilityTimeSlots": null,
    "status": null
  },
  {
    "id": "5a3ba4c1e4b096b359a6ce29",
    "startDate": "2017-12-28",
    "endDate": null,
    "doctor": {
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
        "languagesSpeak": [
          "English",
          "",
          ""
        ],
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
        "educationList": [
          {
            "id": "59e09cbce4b0a70b0de5b0c3",
            "degree": "Bca",
            "university": "un",
            "yearOfPasssing": "88778"
          }
        ],
        "hospitalAttachedWithList": [
          {
            "id": "59e09cbce4b0a70b0de5b0c4",
            "name": "tt",
            "city": "Pune",
            "country": "India"
          }
        ],
        "awardsReceivedList": [
          {
            "id": "59e09cbce4b0a70b0de5b0c5",
            "name": "q",
            "description": "Description",
            "date": "11/11/1991"
          }
        ],
        "specialities": [
          {
            "id": "55b78065e4b0b393bf91678f",
            "name": "general physician",
            "questionnaire": null,
            "report": null
          }
        ],
        "licencedState": [
          {
            "id": "5665a2cb9a87399fa0b9ba33",
            "state": "AL"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba34",
            "state": "AK"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba35",
            "state": "AZ"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba37",
            "state": "CA"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba40",
            "state": "IL"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba41",
            "state": "IN"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba42",
            "state": "IA"
          }
        ],
        "registrationNumber": "22222",
        "whyCoolDoctors": null,
        "bio": "",
        "profession": "Optometrist",
        "availabilityTimeZone": "Asia/Kolkata",
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
      "preferredPharmacies": null,
      "kandyUserName": "kandyuser2",
      "kandyUserPassword": "demo1234",
      "kandyFullUserId": "kandyuser2@neet.cupertinosoft.com",
      "oldPassword": null,
      "loginStatus": "Online",
      "stripeCustId": null,
      "profileImagePath": "https://api.endpoint.eyecarelive.com/PRDIMAGE/doctor/56fb7614e4b0d3123cea4925/ProfileImage/paulsupe232.png",
      "isReferredDoctor": null,
      "randomtoken": "esnckN",
      "isEmailVerified": false,
      "doctorsGroups": [
        {
          "id": "56d01388e4b0cd1739f0e076",
          "groupName": "Silicon Valley Eye Physicians"
        }
      ],
      "preferredDoctors": [
        "56fbd63de4b0777c5a04f540",
        "595a0d97e4b0c065c25684ea"
      ],
      "isAcceptTC": true,
      "insurenceCards": null,
      "notificationSettings": null,
      "clinics": [
        "58f9d4a7e4b07023de8c0d64"
      ],
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
      "twilioAccessToken": "eyJjdHkiOiJ0d2lsaW8tZnBhO3Y9MSIsInR5cCI6IkpXVCIsImFsZyI6IkhTMjU2In0.eyJpc3MiOiJTS2NmMTBhNzcwZmU1MzI4MDQxYjJkNDFiNjc0ODE0YzBlIiwiZXhwIjoxNTEzNzY5Mjk2LCJncmFudHMiOnsiaWRlbnRpdHkiOiI1NmZiNzYxNGU0YjBkMzEyM2NlYTQ5MjUiLCJ2aWRlbyI6eyJyb29tIjoiNTZmYjc2MTRlNGIwZDMxMjNjZWE0OTI1NTZmYmQ2M2RlNGIwNzc3YzVhMDRmNTQwIn19LCJqdGkiOiJTS2NmMTBhNzcwZmU1MzI4MDQxYjJkNDFiNjc0ODE0YzBlLTE1MTM3NjU3NjAiLCJzdWIiOiJBQ2NhNGYyNmM3ODRhM2U5NWU3NDY3ZjRhZGMwMDMwYjFkIn0.1Xj4UMnl6VddKk--HbVYUCSEq5_wlmH0oRrDjVPFmcM",
      "invited": false,
      "validated": true,
      "activated": true,
      "managedUser": false,
      "addedByCpm": false,
      "pilotDoc": true
    },
    "startTimes": null,
    "availabilityTimeSlots": null,
    "status": null
  },
  {
    "id": "5a3ba4c1e4b096b359a6ce2a",
    "startDate": "2017-12-29",
    "endDate": null,
    "doctor": {
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
        "languagesSpeak": [
          "English",
          "",
          ""
        ],
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
        "educationList": [
          {
            "id": "59e09cbce4b0a70b0de5b0c3",
            "degree": "Bca",
            "university": "un",
            "yearOfPasssing": "88778"
          }
        ],
        "hospitalAttachedWithList": [
          {
            "id": "59e09cbce4b0a70b0de5b0c4",
            "name": "tt",
            "city": "Pune",
            "country": "India"
          }
        ],
        "awardsReceivedList": [
          {
            "id": "59e09cbce4b0a70b0de5b0c5",
            "name": "q",
            "description": "Description",
            "date": "11/11/1991"
          }
        ],
        "specialities": [
          {
            "id": "55b78065e4b0b393bf91678f",
            "name": "general physician",
            "questionnaire": null,
            "report": null
          }
        ],
        "licencedState": [
          {
            "id": "5665a2cb9a87399fa0b9ba33",
            "state": "AL"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba34",
            "state": "AK"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba35",
            "state": "AZ"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba37",
            "state": "CA"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba40",
            "state": "IL"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba41",
            "state": "IN"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba42",
            "state": "IA"
          }
        ],
        "registrationNumber": "22222",
        "whyCoolDoctors": null,
        "bio": "",
        "profession": "Optometrist",
        "availabilityTimeZone": "Asia/Kolkata",
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
      "preferredPharmacies": null,
      "kandyUserName": "kandyuser2",
      "kandyUserPassword": "demo1234",
      "kandyFullUserId": "kandyuser2@neet.cupertinosoft.com",
      "oldPassword": null,
      "loginStatus": "Online",
      "stripeCustId": null,
      "profileImagePath": "https://api.endpoint.eyecarelive.com/PRDIMAGE/doctor/56fb7614e4b0d3123cea4925/ProfileImage/paulsupe232.png",
      "isReferredDoctor": null,
      "randomtoken": "esnckN",
      "isEmailVerified": false,
      "doctorsGroups": [
        {
          "id": "56d01388e4b0cd1739f0e076",
          "groupName": "Silicon Valley Eye Physicians"
        }
      ],
      "preferredDoctors": [
        "56fbd63de4b0777c5a04f540",
        "595a0d97e4b0c065c25684ea"
      ],
      "isAcceptTC": true,
      "insurenceCards": null,
      "notificationSettings": null,
      "clinics": [
        "58f9d4a7e4b07023de8c0d64"
      ],
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
      "twilioAccessToken": "eyJjdHkiOiJ0d2lsaW8tZnBhO3Y9MSIsInR5cCI6IkpXVCIsImFsZyI6IkhTMjU2In0.eyJpc3MiOiJTS2NmMTBhNzcwZmU1MzI4MDQxYjJkNDFiNjc0ODE0YzBlIiwiZXhwIjoxNTEzNzY5Mjk2LCJncmFudHMiOnsiaWRlbnRpdHkiOiI1NmZiNzYxNGU0YjBkMzEyM2NlYTQ5MjUiLCJ2aWRlbyI6eyJyb29tIjoiNTZmYjc2MTRlNGIwZDMxMjNjZWE0OTI1NTZmYmQ2M2RlNGIwNzc3YzVhMDRmNTQwIn19LCJqdGkiOiJTS2NmMTBhNzcwZmU1MzI4MDQxYjJkNDFiNjc0ODE0YzBlLTE1MTM3NjU3NjAiLCJzdWIiOiJBQ2NhNGYyNmM3ODRhM2U5NWU3NDY3ZjRhZGMwMDMwYjFkIn0.1Xj4UMnl6VddKk--HbVYUCSEq5_wlmH0oRrDjVPFmcM",
      "invited": false,
      "validated": true,
      "activated": true,
      "managedUser": false,
      "addedByCpm": false,
      "pilotDoc": true
    },
    "startTimes": null,
    "availabilityTimeSlots": null,
    "status": null
  },
  {
    "id": "5a3ba4c1e4b096b359a6ce2b",
    "startDate": "2017-12-30",
    "endDate": null,
    "doctor": {
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
        "languagesSpeak": [
          "English",
          "",
          ""
        ],
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
        "educationList": [
          {
            "id": "59e09cbce4b0a70b0de5b0c3",
            "degree": "Bca",
            "university": "un",
            "yearOfPasssing": "88778"
          }
        ],
        "hospitalAttachedWithList": [
          {
            "id": "59e09cbce4b0a70b0de5b0c4",
            "name": "tt",
            "city": "Pune",
            "country": "India"
          }
        ],
        "awardsReceivedList": [
          {
            "id": "59e09cbce4b0a70b0de5b0c5",
            "name": "q",
            "description": "Description",
            "date": "11/11/1991"
          }
        ],
        "specialities": [
          {
            "id": "55b78065e4b0b393bf91678f",
            "name": "general physician",
            "questionnaire": null,
            "report": null
          }
        ],
        "licencedState": [
          {
            "id": "5665a2cb9a87399fa0b9ba33",
            "state": "AL"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba34",
            "state": "AK"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba35",
            "state": "AZ"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba37",
            "state": "CA"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba40",
            "state": "IL"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba41",
            "state": "IN"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba42",
            "state": "IA"
          }
        ],
        "registrationNumber": "22222",
        "whyCoolDoctors": null,
        "bio": "",
        "profession": "Optometrist",
        "availabilityTimeZone": "Asia/Kolkata",
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
      "preferredPharmacies": null,
      "kandyUserName": "kandyuser2",
      "kandyUserPassword": "demo1234",
      "kandyFullUserId": "kandyuser2@neet.cupertinosoft.com",
      "oldPassword": null,
      "loginStatus": "Online",
      "stripeCustId": null,
      "profileImagePath": "https://api.endpoint.eyecarelive.com/PRDIMAGE/doctor/56fb7614e4b0d3123cea4925/ProfileImage/paulsupe232.png",
      "isReferredDoctor": null,
      "randomtoken": "esnckN",
      "isEmailVerified": false,
      "doctorsGroups": [
        {
          "id": "56d01388e4b0cd1739f0e076",
          "groupName": "Silicon Valley Eye Physicians"
        }
      ],
      "preferredDoctors": [
        "56fbd63de4b0777c5a04f540",
        "595a0d97e4b0c065c25684ea"
      ],
      "isAcceptTC": true,
      "insurenceCards": null,
      "notificationSettings": null,
      "clinics": [
        "58f9d4a7e4b07023de8c0d64"
      ],
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
      "twilioAccessToken": "eyJjdHkiOiJ0d2lsaW8tZnBhO3Y9MSIsInR5cCI6IkpXVCIsImFsZyI6IkhTMjU2In0.eyJpc3MiOiJTS2NmMTBhNzcwZmU1MzI4MDQxYjJkNDFiNjc0ODE0YzBlIiwiZXhwIjoxNTEzNzY5Mjk2LCJncmFudHMiOnsiaWRlbnRpdHkiOiI1NmZiNzYxNGU0YjBkMzEyM2NlYTQ5MjUiLCJ2aWRlbyI6eyJyb29tIjoiNTZmYjc2MTRlNGIwZDMxMjNjZWE0OTI1NTZmYmQ2M2RlNGIwNzc3YzVhMDRmNTQwIn19LCJqdGkiOiJTS2NmMTBhNzcwZmU1MzI4MDQxYjJkNDFiNjc0ODE0YzBlLTE1MTM3NjU3NjAiLCJzdWIiOiJBQ2NhNGYyNmM3ODRhM2U5NWU3NDY3ZjRhZGMwMDMwYjFkIn0.1Xj4UMnl6VddKk--HbVYUCSEq5_wlmH0oRrDjVPFmcM",
      "invited": false,
      "validated": true,
      "activated": true,
      "managedUser": false,
      "addedByCpm": false,
      "pilotDoc": true
    },
    "startTimes": null,
    "availabilityTimeSlots": null,
    "status": null
  }
]
```

> Make sure to replace `X-Auth-Token` with your API key.

### HTTP Request

`GET
http://localhost:8080/DoctorOnDemand/api/doctor/availability/getAvailabilityOfNextWeek
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
Use URL |  Use URL to get the dates | String | Required


### Response

Parameter | Description | Type
--------- | ----------- | ----
ID | ID created by database | String 
startDate | Start Date about availability | String
endDate | End Date about availability | String
doctor[{}] | Doctor information  | String
aboutMe[{}] | Doctor’s about information  | String
contactInfo[{}] | Doctor’s contact information | String
patientInfo[{}] | Patient info  Deprecated  | String
doctorInfo[{}] | Doctor’s info  | String
specialities[{}] | Specialities ID always be fixed | String
licencedState[{}] | Licensed states of doctor’s | String
role[{}] | Role ID always be a fixed ID for doctor’s | String
timezone[{}] | Doctor’s Time zone  | String
createdAt[{}] | End Date about availability | String
forgotPasswordToken[{}] | Forgot password token created | String
familyMembers[{}] | Family member data | String
parentUser[{}] | Parent user Deprecated | String
parentUserRelation[{}] | Parent user Deprecated | String
password[{}] | Deprecated | String
rating[{}] | Deprecated | String
preferredPharmacies[{}] | Deprecated | String
profileImagePath | Doctor’s image path | String
randomtoken | Deprecated | String
doctorsGroups[{}] | Doctor’s Group  | String
preferredDoctors[{}] | Deprecated | String
clinics[{}] | Deprecated | String
doctorsOrg[{}] | Deprecated | String
twilioAccessToken | Deprecated | String
startTimes | Deprecated | String
 | availabilityTimeSlot |
id | ID of availability  | String
startTime | Start time  | String
sTime | Stime is date of availability  | String
eTime | Etime is data of availability  | String
slotNumber | Slot number  | String
patient | Deprecated | String
visitType | Deprecated | String
appointmentId | Deprecated | String
status | “Enable” | String
booked | True & false | String
 | Other All parameter which is not mentioned that all “Deprecated” | 


`Authorization: X-Auth-Token`

<aside class="notice">
You must replace <code>X-Auth-Token</code> with your personal API key.
</aside>

## Add Doctor’s Availability

```shell
curl -i -H "Content-Type: application/json" -H "X-Auth-Token:nitesh.yadav@cooldoctors.io:doctor:1516451737683:59dd0d65a2e932543b28a07d541ee17f" -X POST "http://api.endpoint.eyecarelive.com/DoctorOnDemand/api/doctor/availability" -d '[{"startDate":"2017-12-17"},{"startDate":"2017-12-18"},{"startDate":"2017-12-19"},{"startDate":"2017-12-20"},{"startDate":"2017-12-21","startTimes":["12"]},{"startDate":"2017-12-22"},{"startDate":"2017-12-23"}]'


```
> The above command returns JSON structured like this:

```json
[
  {
    "id": "5a3baaf5e4b096b359a6cf40",
    "startDate": "2017-12-17",
    "endDate": null,
    "doctor": {
      "id": "56fbd63de4b0777c5a04f540",
      "email": "nitesh.yadav@cooldoctors.io",
      "pharmacyName": null,
      "pharmacyAddress": null,
      "profileImageId": null,
      "profileImageName": null,
      "aboutMe": {
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
      },
      "contactInfo": {
        "id": "56fbd63de4b0777c5a04f53f",
        "email": "nitesh.yadav@cooldoctors.io",
        "phone": "88069007404",
        "smsNotification": false,
        "countryCode": "+91",
        "country": "USA",
        "emlNt": false
      },
      "patientInfo": null,
      "doctorInfo": {
        "id": "5a2f6d76e4b0e4fa266e293f",
        "educationList": [
          {
            "id": "5a2f6d76e4b0e4fa266e293c",
            "degree": "BDS",
            "university": "Pune",
            "yearOfPasssing": "2013"
          }
        ],
        "hospitalAttachedWithList": [
          {
            "id": "5a2f6d76e4b0e4fa266e293d",
            "name": "Pune Sasun hospital",
            "city": "Pune",
            "country": "India"
          }
        ],
        "awardsReceivedList": [
          {
            "id": "5a2f6d76e4b0e4fa266e293e",
            "name": "Best Doctor",
            "description": "Eye Care",
            "date": "2015-08-27 08:19 AM IDT"
          }
        ],
        "specialities": [
          {
            "id": "55b7802be4b0b393bf91678e",
            "name": "eye care",
            "questionnaire": null,
            "report": null
          }
        ],
        "licencedState": [
          {
            "id": "5665a2cb9a87399fa0b9ba34",
            "state": "AK"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba35",
            "state": "AZ"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba36",
            "state": "AR"
          }
        ],
        "registrationNumber": "22222",
        "whyCoolDoctors": null,
        "bio": "sdfsdf",
        "profession": " Ophthalmologist",
        "availabilityTimeZone": "Africa/Algiers",
        "npi": "123456789"
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
      "createdAt": "2016-03-30 06:35 AM PDT",
      "forgotPasswordToken": "DG@NtS",
      "familyMembers": null,
      "parentUser": null,
      "parentUserRelation": null,
      "password": "Neet@7777",
      "rating": null,
      "preferredPharmacies": null,
      "kandyUserName": "kandyuser1",
      "kandyUserPassword": "demo1234",
      "kandyFullUserId": "kandyuser1@neet.cupertinosoft.com",
      "oldPassword": null,
      "loginStatus": "Online",
      "stripeCustId": null,
      "profileImagePath": "https://api.endpoint.eyecarelive.com/PRDIMAGE/doctor/56fbd63de4b0777c5a04f540/ProfileImage/images (18).jpg",
      "isReferredDoctor": null,
      "randomtoken": "hwaFEz",
      "isEmailVerified": false,
      "doctorsGroups": null,
      "preferredDoctors": [
        "593510a7e4b0e5fde2c12f99",
        "56fb7614e4b0d3123cea4925"
      ],
      "isAcceptTC": true,
      "insurenceCards": null,
      "notificationSettings": null,
      "clinics": [
        "58c7fed2e4b07aabf7bf76fb",
        "58f9d4a7e4b07023de8c0d64"
      ],
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
      "twilioAccessToken": "eyJjdHkiOiJ0d2lsaW8tZnBhO3Y9MSIsInR5cCI6IkpXVCIsImFsZyI6IkhTMjU2In0.eyJpc3MiOiJTS2NmMTBhNzcwZmU1MzI4MDQxYjJkNDFiNjc0ODE0YzBlIiwiZXhwIjoxNTEzNzY5Mjk0LCJncmFudHMiOnsiaWRlbnRpdHkiOiI1NmZiZDYzZGU0YjA3NzdjNWEwNGY1NDAiLCJ2aWRlbyI6eyJyb29tIjoiNTZmYjc2MTRlNGIwZDMxMjNjZWE0OTI1NTZmYmQ2M2RlNGIwNzc3YzVhMDRmNTQwIn19LCJqdGkiOiJTS2NmMTBhNzcwZmU1MzI4MDQxYjJkNDFiNjc0ODE0YzBlLTE1MTM3NjU3NjAiLCJzdWIiOiJBQ2NhNGYyNmM3ODRhM2U5NWU3NDY3ZjRhZGMwMDMwYjFkIn0.f_STYfV7t5Ir6cUlgXDEYzD7VIowP4Wj-XAZXofcsvE",
      "invited": false,
      "validated": true,
      "activated": true,
      "managedUser": false,
      "addedByCpm": false,
      "pilotDoc": true
    },
    "startTimes": null,
    "availabilityTimeSlots": null,
    "status": null
  },
  {
    "id": "5a3baaf5e4b096b359a6cf41",
    "startDate": "2017-12-18",
    "endDate": null,
    "doctor": {
      "id": "56fbd63de4b0777c5a04f540",
      "email": "nitesh.yadav@cooldoctors.io",
      "pharmacyName": null,
      "pharmacyAddress": null,
      "profileImageId": null,
      "profileImageName": null,
      "aboutMe": {
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
      },
      "contactInfo": {
        "id": "56fbd63de4b0777c5a04f53f",
        "email": "nitesh.yadav@cooldoctors.io",
        "phone": "88069007404",
        "smsNotification": false,
        "countryCode": "+91",
        "country": "USA",
        "emlNt": false
      },
      "patientInfo": null,
      "doctorInfo": {
        "id": "5a2f6d76e4b0e4fa266e293f",
        "educationList": [
          {
            "id": "5a2f6d76e4b0e4fa266e293c",
            "degree": "BDS",
            "university": "Pune",
            "yearOfPasssing": "2013"
          }
        ],
        "hospitalAttachedWithList": [
          {
            "id": "5a2f6d76e4b0e4fa266e293d",
            "name": "Pune Sasun hospital",
            "city": "Pune",
            "country": "India"
          }
        ],
        "awardsReceivedList": [
          {
            "id": "5a2f6d76e4b0e4fa266e293e",
            "name": "Best Doctor",
            "description": "Eye Care",
            "date": "2015-08-27 08:19 AM IDT"
          }
        ],
        "specialities": [
          {
            "id": "55b7802be4b0b393bf91678e",
            "name": "eye care",
            "questionnaire": null,
            "report": null
          }
        ],
        "licencedState": [
          {
            "id": "5665a2cb9a87399fa0b9ba34",
            "state": "AK"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba35",
            "state": "AZ"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba36",
            "state": "AR"
          }
        ],
        "registrationNumber": "22222",
        "whyCoolDoctors": null,
        "bio": "sdfsdf",
        "profession": " Ophthalmologist",
        "availabilityTimeZone": "Africa/Algiers",
        "npi": "123456789"
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
      "createdAt": "2016-03-30 06:35 AM PDT",
      "forgotPasswordToken": "DG@NtS",
      "familyMembers": null,
      "parentUser": null,
      "parentUserRelation": null,
      "password": "Neet@7777",
      "rating": null,
      "preferredPharmacies": null,
      "kandyUserName": "kandyuser1",
      "kandyUserPassword": "demo1234",
      "kandyFullUserId": "kandyuser1@neet.cupertinosoft.com",
      "oldPassword": null,
      "loginStatus": "Online",
      "stripeCustId": null,
      "profileImagePath": "https://api.endpoint.eyecarelive.com/PRDIMAGE/doctor/56fbd63de4b0777c5a04f540/ProfileImage/images (18).jpg",
      "isReferredDoctor": null,
      "randomtoken": "hwaFEz",
      "isEmailVerified": false,
      "doctorsGroups": null,
      "preferredDoctors": [
        "593510a7e4b0e5fde2c12f99",
        "56fb7614e4b0d3123cea4925"
      ],
      "isAcceptTC": true,
      "insurenceCards": null,
      "notificationSettings": null,
      "clinics": [
        "58c7fed2e4b07aabf7bf76fb",
        "58f9d4a7e4b07023de8c0d64"
      ],
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
      "twilioAccessToken": "eyJjdHkiOiJ0d2lsaW8tZnBhO3Y9MSIsInR5cCI6IkpXVCIsImFsZyI6IkhTMjU2In0.eyJpc3MiOiJTS2NmMTBhNzcwZmU1MzI4MDQxYjJkNDFiNjc0ODE0YzBlIiwiZXhwIjoxNTEzNzY5Mjk0LCJncmFudHMiOnsiaWRlbnRpdHkiOiI1NmZiZDYzZGU0YjA3NzdjNWEwNGY1NDAiLCJ2aWRlbyI6eyJyb29tIjoiNTZmYjc2MTRlNGIwZDMxMjNjZWE0OTI1NTZmYmQ2M2RlNGIwNzc3YzVhMDRmNTQwIn19LCJqdGkiOiJTS2NmMTBhNzcwZmU1MzI4MDQxYjJkNDFiNjc0ODE0YzBlLTE1MTM3NjU3NjAiLCJzdWIiOiJBQ2NhNGYyNmM3ODRhM2U5NWU3NDY3ZjRhZGMwMDMwYjFkIn0.f_STYfV7t5Ir6cUlgXDEYzD7VIowP4Wj-XAZXofcsvE",
      "invited": false,
      "validated": true,
      "activated": true,
      "managedUser": false,
      "addedByCpm": false,
      "pilotDoc": true
    },
    "startTimes": null,
    "availabilityTimeSlots": null,
    "status": null
  },
  {
    "id": "5a3baaf5e4b096b359a6cf42",
    "startDate": "2017-12-19",
    "endDate": null,
    "doctor": {
      "id": "56fbd63de4b0777c5a04f540",
      "email": "nitesh.yadav@cooldoctors.io",
      "pharmacyName": null,
      "pharmacyAddress": null,
      "profileImageId": null,
      "profileImageName": null,
      "aboutMe": {
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
      },
      "contactInfo": {
        "id": "56fbd63de4b0777c5a04f53f",
        "email": "nitesh.yadav@cooldoctors.io",
        "phone": "88069007404",
        "smsNotification": false,
        "countryCode": "+91",
        "country": "USA",
        "emlNt": false
      },
      "patientInfo": null,
      "doctorInfo": {
        "id": "5a2f6d76e4b0e4fa266e293f",
        "educationList": [
          {
            "id": "5a2f6d76e4b0e4fa266e293c",
            "degree": "BDS",
            "university": "Pune",
            "yearOfPasssing": "2013"
          }
        ],
        "hospitalAttachedWithList": [
          {
            "id": "5a2f6d76e4b0e4fa266e293d",
            "name": "Pune Sasun hospital",
            "city": "Pune",
            "country": "India"
          }
        ],
        "awardsReceivedList": [
          {
            "id": "5a2f6d76e4b0e4fa266e293e",
            "name": "Best Doctor",
            "description": "Eye Care",
            "date": "2015-08-27 08:19 AM IDT"
          }
        ],
        "specialities": [
          {
            "id": "55b7802be4b0b393bf91678e",
            "name": "eye care",
            "questionnaire": null,
            "report": null
          }
        ],
        "licencedState": [
          {
            "id": "5665a2cb9a87399fa0b9ba34",
            "state": "AK"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba35",
            "state": "AZ"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba36",
            "state": "AR"
          }
        ],
        "registrationNumber": "22222",
        "whyCoolDoctors": null,
        "bio": "sdfsdf",
        "profession": " Ophthalmologist",
        "availabilityTimeZone": "Africa/Algiers",
        "npi": "123456789"
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
      "createdAt": "2016-03-30 06:35 AM PDT",
      "forgotPasswordToken": "DG@NtS",
      "familyMembers": null,
      "parentUser": null,
      "parentUserRelation": null,
      "password": "Neet@7777",
      "rating": null,
      "preferredPharmacies": null,
      "kandyUserName": "kandyuser1",
      "kandyUserPassword": "demo1234",
      "kandyFullUserId": "kandyuser1@neet.cupertinosoft.com",
      "oldPassword": null,
      "loginStatus": "Online",
      "stripeCustId": null,
      "profileImagePath": "https://api.endpoint.eyecarelive.com/PRDIMAGE/doctor/56fbd63de4b0777c5a04f540/ProfileImage/images (18).jpg",
      "isReferredDoctor": null,
      "randomtoken": "hwaFEz",
      "isEmailVerified": false,
      "doctorsGroups": null,
      "preferredDoctors": [
        "593510a7e4b0e5fde2c12f99",
        "56fb7614e4b0d3123cea4925"
      ],
      "isAcceptTC": true,
      "insurenceCards": null,
      "notificationSettings": null,
      "clinics": [
        "58c7fed2e4b07aabf7bf76fb",
        "58f9d4a7e4b07023de8c0d64"
      ],
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
      "twilioAccessToken": "eyJjdHkiOiJ0d2lsaW8tZnBhO3Y9MSIsInR5cCI6IkpXVCIsImFsZyI6IkhTMjU2In0.eyJpc3MiOiJTS2NmMTBhNzcwZmU1MzI4MDQxYjJkNDFiNjc0ODE0YzBlIiwiZXhwIjoxNTEzNzY5Mjk0LCJncmFudHMiOnsiaWRlbnRpdHkiOiI1NmZiZDYzZGU0YjA3NzdjNWEwNGY1NDAiLCJ2aWRlbyI6eyJyb29tIjoiNTZmYjc2MTRlNGIwZDMxMjNjZWE0OTI1NTZmYmQ2M2RlNGIwNzc3YzVhMDRmNTQwIn19LCJqdGkiOiJTS2NmMTBhNzcwZmU1MzI4MDQxYjJkNDFiNjc0ODE0YzBlLTE1MTM3NjU3NjAiLCJzdWIiOiJBQ2NhNGYyNmM3ODRhM2U5NWU3NDY3ZjRhZGMwMDMwYjFkIn0.f_STYfV7t5Ir6cUlgXDEYzD7VIowP4Wj-XAZXofcsvE",
      "invited": false,
      "validated": true,
      "activated": true,
      "managedUser": false,
      "addedByCpm": false,
      "pilotDoc": true
    },
    "startTimes": null,
    "availabilityTimeSlots": null,
    "status": null
  },
  {
    "id": "5a3baaf5e4b096b359a6cf43",
    "startDate": "2017-12-20",
    "endDate": null,
    "doctor": {
      "id": "56fbd63de4b0777c5a04f540",
      "email": "nitesh.yadav@cooldoctors.io",
      "pharmacyName": null,
      "pharmacyAddress": null,
      "profileImageId": null,
      "profileImageName": null,
      "aboutMe": {
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
      },
      "contactInfo": {
        "id": "56fbd63de4b0777c5a04f53f",
        "email": "nitesh.yadav@cooldoctors.io",
        "phone": "88069007404",
        "smsNotification": false,
        "countryCode": "+91",
        "country": "USA",
        "emlNt": false
      },
      "patientInfo": null,
      "doctorInfo": {
        "id": "5a2f6d76e4b0e4fa266e293f",
        "educationList": [
          {
            "id": "5a2f6d76e4b0e4fa266e293c",
            "degree": "BDS",
            "university": "Pune",
            "yearOfPasssing": "2013"
          }
        ],
        "hospitalAttachedWithList": [
          {
            "id": "5a2f6d76e4b0e4fa266e293d",
            "name": "Pune Sasun hospital",
            "city": "Pune",
            "country": "India"
          }
        ],
        "awardsReceivedList": [
          {
            "id": "5a2f6d76e4b0e4fa266e293e",
            "name": "Best Doctor",
            "description": "Eye Care",
            "date": "2015-08-27 08:19 AM IDT"
          }
        ],
        "specialities": [
          {
            "id": "55b7802be4b0b393bf91678e",
            "name": "eye care",
            "questionnaire": null,
            "report": null
          }
        ],
        "licencedState": [
          {
            "id": "5665a2cb9a87399fa0b9ba34",
            "state": "AK"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba35",
            "state": "AZ"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba36",
            "state": "AR"
          }
        ],
        "registrationNumber": "22222",
        "whyCoolDoctors": null,
        "bio": "sdfsdf",
        "profession": " Ophthalmologist",
        "availabilityTimeZone": "Africa/Algiers",
        "npi": "123456789"
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
      "createdAt": "2016-03-30 06:35 AM PDT",
      "forgotPasswordToken": "DG@NtS",
      "familyMembers": null,
      "parentUser": null,
      "parentUserRelation": null,
      "password": "Neet@7777",
      "rating": null,
      "preferredPharmacies": null,
      "kandyUserName": "kandyuser1",
      "kandyUserPassword": "demo1234",
      "kandyFullUserId": "kandyuser1@neet.cupertinosoft.com",
      "oldPassword": null,
      "loginStatus": "Online",
      "stripeCustId": null,
      "profileImagePath": "https://api.endpoint.eyecarelive.com/PRDIMAGE/doctor/56fbd63de4b0777c5a04f540/ProfileImage/images (18).jpg",
      "isReferredDoctor": null,
      "randomtoken": "hwaFEz",
      "isEmailVerified": false,
      "doctorsGroups": null,
      "preferredDoctors": [
        "593510a7e4b0e5fde2c12f99",
        "56fb7614e4b0d3123cea4925"
      ],
      "isAcceptTC": true,
      "insurenceCards": null,
      "notificationSettings": null,
      "clinics": [
        "58c7fed2e4b07aabf7bf76fb",
        "58f9d4a7e4b07023de8c0d64"
      ],
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
      "twilioAccessToken": "eyJjdHkiOiJ0d2lsaW8tZnBhO3Y9MSIsInR5cCI6IkpXVCIsImFsZyI6IkhTMjU2In0.eyJpc3MiOiJTS2NmMTBhNzcwZmU1MzI4MDQxYjJkNDFiNjc0ODE0YzBlIiwiZXhwIjoxNTEzNzY5Mjk0LCJncmFudHMiOnsiaWRlbnRpdHkiOiI1NmZiZDYzZGU0YjA3NzdjNWEwNGY1NDAiLCJ2aWRlbyI6eyJyb29tIjoiNTZmYjc2MTRlNGIwZDMxMjNjZWE0OTI1NTZmYmQ2M2RlNGIwNzc3YzVhMDRmNTQwIn19LCJqdGkiOiJTS2NmMTBhNzcwZmU1MzI4MDQxYjJkNDFiNjc0ODE0YzBlLTE1MTM3NjU3NjAiLCJzdWIiOiJBQ2NhNGYyNmM3ODRhM2U5NWU3NDY3ZjRhZGMwMDMwYjFkIn0.f_STYfV7t5Ir6cUlgXDEYzD7VIowP4Wj-XAZXofcsvE",
      "invited": false,
      "validated": true,
      "activated": true,
      "managedUser": false,
      "addedByCpm": false,
      "pilotDoc": true
    },
    "startTimes": null,
    "availabilityTimeSlots": null,
    "status": null
  },
  {
    "id": "5a3baaf5e4b096b359a6cf4a",
    "startDate": "2017-12-21",
    "endDate": null,
    "doctor": {
      "id": "56fbd63de4b0777c5a04f540",
      "email": "nitesh.yadav@cooldoctors.io",
      "pharmacyName": null,
      "pharmacyAddress": null,
      "profileImageId": null,
      "profileImageName": null,
      "aboutMe": {
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
      },
      "contactInfo": {
        "id": "56fbd63de4b0777c5a04f53f",
        "email": "nitesh.yadav@cooldoctors.io",
        "phone": "88069007404",
        "smsNotification": false,
        "countryCode": "+91",
        "country": "USA",
        "emlNt": false
      },
      "patientInfo": null,
      "doctorInfo": {
        "id": "5a2f6d76e4b0e4fa266e293f",
        "educationList": [
          {
            "id": "5a2f6d76e4b0e4fa266e293c",
            "degree": "BDS",
            "university": "Pune",
            "yearOfPasssing": "2013"
          }
        ],
        "hospitalAttachedWithList": [
          {
            "id": "5a2f6d76e4b0e4fa266e293d",
            "name": "Pune Sasun hospital",
            "city": "Pune",
            "country": "India"
          }
        ],
        "awardsReceivedList": [
          {
            "id": "5a2f6d76e4b0e4fa266e293e",
            "name": "Best Doctor",
            "description": "Eye Care",
            "date": "2015-08-27 08:19 AM IDT"
          }
        ],
        "specialities": [
          {
            "id": "55b7802be4b0b393bf91678e",
            "name": "eye care",
            "questionnaire": null,
            "report": null
          }
        ],
        "licencedState": [
          {
            "id": "5665a2cb9a87399fa0b9ba34",
            "state": "AK"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba35",
            "state": "AZ"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba36",
            "state": "AR"
          }
        ],
        "registrationNumber": "22222",
        "whyCoolDoctors": null,
        "bio": "sdfsdf",
        "profession": " Ophthalmologist",
        "availabilityTimeZone": "Africa/Algiers",
        "npi": "123456789"
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
      "createdAt": "2016-03-30 06:35 AM PDT",
      "forgotPasswordToken": "DG@NtS",
      "familyMembers": null,
      "parentUser": null,
      "parentUserRelation": null,
      "password": "Neet@7777",
      "rating": null,
      "preferredPharmacies": null,
      "kandyUserName": "kandyuser1",
      "kandyUserPassword": "demo1234",
      "kandyFullUserId": "kandyuser1@neet.cupertinosoft.com",
      "oldPassword": null,
      "loginStatus": "Online",
      "stripeCustId": null,
      "profileImagePath": "https://api.endpoint.eyecarelive.com/PRDIMAGE/doctor/56fbd63de4b0777c5a04f540/ProfileImage/images (18).jpg",
      "isReferredDoctor": null,
      "randomtoken": "hwaFEz",
      "isEmailVerified": false,
      "doctorsGroups": null,
      "preferredDoctors": [
        "593510a7e4b0e5fde2c12f99",
        "56fb7614e4b0d3123cea4925"
      ],
      "isAcceptTC": true,
      "insurenceCards": null,
      "notificationSettings": null,
      "clinics": [
        "58c7fed2e4b07aabf7bf76fb",
        "58f9d4a7e4b07023de8c0d64"
      ],
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
      "twilioAccessToken": "eyJjdHkiOiJ0d2lsaW8tZnBhO3Y9MSIsInR5cCI6IkpXVCIsImFsZyI6IkhTMjU2In0.eyJpc3MiOiJTS2NmMTBhNzcwZmU1MzI4MDQxYjJkNDFiNjc0ODE0YzBlIiwiZXhwIjoxNTEzNzY5Mjk0LCJncmFudHMiOnsiaWRlbnRpdHkiOiI1NmZiZDYzZGU0YjA3NzdjNWEwNGY1NDAiLCJ2aWRlbyI6eyJyb29tIjoiNTZmYjc2MTRlNGIwZDMxMjNjZWE0OTI1NTZmYmQ2M2RlNGIwNzc3YzVhMDRmNTQwIn19LCJqdGkiOiJTS2NmMTBhNzcwZmU1MzI4MDQxYjJkNDFiNjc0ODE0YzBlLTE1MTM3NjU3NjAiLCJzdWIiOiJBQ2NhNGYyNmM3ODRhM2U5NWU3NDY3ZjRhZGMwMDMwYjFkIn0.f_STYfV7t5Ir6cUlgXDEYzD7VIowP4Wj-XAZXofcsvE",
      "invited": false,
      "validated": true,
      "activated": true,
      "managedUser": false,
      "addedByCpm": false,
      "pilotDoc": true
    },
    "startTimes": [
      "20"
    ],
    "availabilityTimeSlots": [
      {
        "id": "5a3baaf5e4b096b359a6cf44",
        "startTime": "20",
        "sTime": "2017-12-21 08:00 PM UTC",
        "eTime": "2017-12-21 08:10 PM UTC",
        "slotNumber": "0",
        "patient": null,
        "visitType": null,
        "appointmentId": null,
        "status": "enable",
        "booked": false
      },
      {
        "id": "5a3baaf5e4b096b359a6cf45",
        "startTime": "20",
        "sTime": "2017-12-21 08:10 PM UTC",
        "eTime": "2017-12-21 08:20 PM UTC",
        "slotNumber": "1",
        "patient": null,
        "visitType": null,
        "appointmentId": null,
        "status": "enable",
        "booked": false
      },
      {
        "id": "5a3baaf5e4b096b359a6cf46",
        "startTime": "20",
        "sTime": "2017-12-21 08:20 PM UTC",
        "eTime": "2017-12-21 08:30 PM UTC",
        "slotNumber": "2",
        "patient": null,
        "visitType": null,
        "appointmentId": null,
        "status": "enable",
        "booked": false
      },
      {
        "id": "5a3baaf5e4b096b359a6cf47",
        "startTime": "20",
        "sTime": "2017-12-21 08:30 PM UTC",
        "eTime": "2017-12-21 08:40 PM UTC",
        "slotNumber": "3",
        "patient": null,
        "visitType": null,
        "appointmentId": null,
        "status": "enable",
        "booked": false
      },
      {
        "id": "5a3baaf5e4b096b359a6cf48",
        "startTime": "20",
        "sTime": "2017-12-21 08:40 PM UTC",
        "eTime": "2017-12-21 08:50 PM UTC",
        "slotNumber": "4",
        "patient": null,
        "visitType": null,
        "appointmentId": null,
        "status": "enable",
        "booked": false
      },
      {
        "id": "5a3baaf5e4b096b359a6cf49",
        "startTime": "20",
        "sTime": "2017-12-21 08:50 PM UTC",
        "eTime": "2017-12-21 09:00 PM UTC",
        "slotNumber": "5",
        "patient": null,
        "visitType": null,
        "appointmentId": null,
        "status": "enable",
        "booked": false
      }
    ],
    "status": null
  },
  {
    "id": "5a3baaf5e4b096b359a6cf4b",
    "startDate": "2017-12-22",
    "endDate": null,
    "doctor": {
      "id": "56fbd63de4b0777c5a04f540",
      "email": "nitesh.yadav@cooldoctors.io",
      "pharmacyName": null,
      "pharmacyAddress": null,
      "profileImageId": null,
      "profileImageName": null,
      "aboutMe": {
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
      },
      "contactInfo": {
        "id": "56fbd63de4b0777c5a04f53f",
        "email": "nitesh.yadav@cooldoctors.io",
        "phone": "88069007404",
        "smsNotification": false,
        "countryCode": "+91",
        "country": "USA",
        "emlNt": false
      },
      "patientInfo": null,
      "doctorInfo": {
        "id": "5a2f6d76e4b0e4fa266e293f",
        "educationList": [
          {
            "id": "5a2f6d76e4b0e4fa266e293c",
            "degree": "BDS",
            "university": "Pune",
            "yearOfPasssing": "2013"
          }
        ],
        "hospitalAttachedWithList": [
          {
            "id": "5a2f6d76e4b0e4fa266e293d",
            "name": "Pune Sasun hospital",
            "city": "Pune",
            "country": "India"
          }
        ],
        "awardsReceivedList": [
          {
            "id": "5a2f6d76e4b0e4fa266e293e",
            "name": "Best Doctor",
            "description": "Eye Care",
            "date": "2015-08-27 08:19 AM IDT"
          }
        ],
        "specialities": [
          {
            "id": "55b7802be4b0b393bf91678e",
            "name": "eye care",
            "questionnaire": null,
            "report": null
          }
        ],
        "licencedState": [
          {
            "id": "5665a2cb9a87399fa0b9ba34",
            "state": "AK"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba35",
            "state": "AZ"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba36",
            "state": "AR"
          }
        ],
        "registrationNumber": "22222",
        "whyCoolDoctors": null,
        "bio": "sdfsdf",
        "profession": " Ophthalmologist",
        "availabilityTimeZone": "Africa/Algiers",
        "npi": "123456789"
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
      "createdAt": "2016-03-30 06:35 AM PDT",
      "forgotPasswordToken": "DG@NtS",
      "familyMembers": null,
      "parentUser": null,
      "parentUserRelation": null,
      "password": "Neet@7777",
      "rating": null,
      "preferredPharmacies": null,
      "kandyUserName": "kandyuser1",
      "kandyUserPassword": "demo1234",
      "kandyFullUserId": "kandyuser1@neet.cupertinosoft.com",
      "oldPassword": null,
      "loginStatus": "Online",
      "stripeCustId": null,
      "profileImagePath": "https://api.endpoint.eyecarelive.com/PRDIMAGE/doctor/56fbd63de4b0777c5a04f540/ProfileImage/images (18).jpg",
      "isReferredDoctor": null,
      "randomtoken": "hwaFEz",
      "isEmailVerified": false,
      "doctorsGroups": null,
      "preferredDoctors": [
        "593510a7e4b0e5fde2c12f99",
        "56fb7614e4b0d3123cea4925"
      ],
      "isAcceptTC": true,
      "insurenceCards": null,
      "notificationSettings": null,
      "clinics": [
        "58c7fed2e4b07aabf7bf76fb",
        "58f9d4a7e4b07023de8c0d64"
      ],
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
      "twilioAccessToken": "eyJjdHkiOiJ0d2lsaW8tZnBhO3Y9MSIsInR5cCI6IkpXVCIsImFsZyI6IkhTMjU2In0.eyJpc3MiOiJTS2NmMTBhNzcwZmU1MzI4MDQxYjJkNDFiNjc0ODE0YzBlIiwiZXhwIjoxNTEzNzY5Mjk0LCJncmFudHMiOnsiaWRlbnRpdHkiOiI1NmZiZDYzZGU0YjA3NzdjNWEwNGY1NDAiLCJ2aWRlbyI6eyJyb29tIjoiNTZmYjc2MTRlNGIwZDMxMjNjZWE0OTI1NTZmYmQ2M2RlNGIwNzc3YzVhMDRmNTQwIn19LCJqdGkiOiJTS2NmMTBhNzcwZmU1MzI4MDQxYjJkNDFiNjc0ODE0YzBlLTE1MTM3NjU3NjAiLCJzdWIiOiJBQ2NhNGYyNmM3ODRhM2U5NWU3NDY3ZjRhZGMwMDMwYjFkIn0.f_STYfV7t5Ir6cUlgXDEYzD7VIowP4Wj-XAZXofcsvE",
      "invited": false,
      "validated": true,
      "activated": true,
      "managedUser": false,
      "addedByCpm": false,
      "pilotDoc": true
    },
    "startTimes": null,
    "availabilityTimeSlots": null,
    "status": null
  },
  {
    "id": "5a3baaf5e4b096b359a6cf4c",
    "startDate": "2017-12-23",
    "endDate": null,
    "doctor": {
      "id": "56fbd63de4b0777c5a04f540",
      "email": "nitesh.yadav@cooldoctors.io",
      "pharmacyName": null,
      "pharmacyAddress": null,
      "profileImageId": null,
      "profileImageName": null,
      "aboutMe": {
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
      },
      "contactInfo": {
        "id": "56fbd63de4b0777c5a04f53f",
        "email": "nitesh.yadav@cooldoctors.io",
        "phone": "88069007404",
        "smsNotification": false,
        "countryCode": "+91",
        "country": "USA",
        "emlNt": false
      },
      "patientInfo": null,
      "doctorInfo": {
        "id": "5a2f6d76e4b0e4fa266e293f",
        "educationList": [
          {
            "id": "5a2f6d76e4b0e4fa266e293c",
            "degree": "BDS",
            "university": "Pune",
            "yearOfPasssing": "2013"
          }
        ],
        "hospitalAttachedWithList": [
          {
            "id": "5a2f6d76e4b0e4fa266e293d",
            "name": "Pune Sasun hospital",
            "city": "Pune",
            "country": "India"
          }
        ],
        "awardsReceivedList": [
          {
            "id": "5a2f6d76e4b0e4fa266e293e",
            "name": "Best Doctor",
            "description": "Eye Care",
            "date": "2015-08-27 08:19 AM IDT"
          }
        ],
        "specialities": [
          {
            "id": "55b7802be4b0b393bf91678e",
            "name": "eye care",
            "questionnaire": null,
            "report": null
          }
        ],
        "licencedState": [
          {
            "id": "5665a2cb9a87399fa0b9ba34",
            "state": "AK"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba35",
            "state": "AZ"
          },
          {
            "id": "5665a2cb9a87399fa0b9ba36",
            "state": "AR"
          }
        ],
        "registrationNumber": "22222",
        "whyCoolDoctors": null,
        "bio": "sdfsdf",
        "profession": " Ophthalmologist",
        "availabilityTimeZone": "Africa/Algiers",
        "npi": "123456789"
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
      "createdAt": "2016-03-30 06:35 AM PDT",
      "forgotPasswordToken": "DG@NtS",
      "familyMembers": null,
      "parentUser": null,
      "parentUserRelation": null,
      "password": "Neet@7777",
      "rating": null,
      "preferredPharmacies": null,
      "kandyUserName": "kandyuser1",
      "kandyUserPassword": "demo1234",
      "kandyFullUserId": "kandyuser1@neet.cupertinosoft.com",
      "oldPassword": null,
      "loginStatus": "Online",
      "stripeCustId": null,
      "profileImagePath": "https://api.endpoint.eyecarelive.com/PRDIMAGE/doctor/56fbd63de4b0777c5a04f540/ProfileImage/images (18).jpg",
      "isReferredDoctor": null,
      "randomtoken": "hwaFEz",
      "isEmailVerified": false,
      "doctorsGroups": null,
      "preferredDoctors": [
        "593510a7e4b0e5fde2c12f99",
        "56fb7614e4b0d3123cea4925"
      ],
      "isAcceptTC": true,
      "insurenceCards": null,
      "notificationSettings": null,
      "clinics": [
        "58c7fed2e4b07aabf7bf76fb",
        "58f9d4a7e4b07023de8c0d64"
      ],
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
      "twilioAccessToken": "eyJjdHkiOiJ0d2lsaW8tZnBhO3Y9MSIsInR5cCI6IkpXVCIsImFsZyI6IkhTMjU2In0.eyJpc3MiOiJTS2NmMTBhNzcwZmU1MzI4MDQxYjJkNDFiNjc0ODE0YzBlIiwiZXhwIjoxNTEzNzY5Mjk0LCJncmFudHMiOnsiaWRlbnRpdHkiOiI1NmZiZDYzZGU0YjA3NzdjNWEwNGY1NDAiLCJ2aWRlbyI6eyJyb29tIjoiNTZmYjc2MTRlNGIwZDMxMjNjZWE0OTI1NTZmYmQ2M2RlNGIwNzc3YzVhMDRmNTQwIn19LCJqdGkiOiJTS2NmMTBhNzcwZmU1MzI4MDQxYjJkNDFiNjc0ODE0YzBlLTE1MTM3NjU3NjAiLCJzdWIiOiJBQ2NhNGYyNmM3ODRhM2U5NWU3NDY3ZjRhZGMwMDMwYjFkIn0.f_STYfV7t5Ir6cUlgXDEYzD7VIowP4Wj-XAZXofcsvE",
      "invited": false,
      "validated": true,
      "activated": true,
      "managedUser": false,
      "addedByCpm": false,
      "pilotDoc": true
    },
    "startTimes": null,
    "availabilityTimeSlots": null,
    "status": null
  }
]
```

> Make sure to replace `X-Auth-Token` with your API key.

### HTTP Request

`POST
http://localhost:8080/DoctorOnDemand/api/doctor/availability
`
### Query Parameters

Parameter |  Description | Type | Optional/Required
--------- | ------------ | ---- | ----------------
startDate |  Get first 7 dates of currect/next week then select the date. | String | Required
startTimes | After selecting date pass time slot | String | Required

### Response

Parameter | Description | Type
--------- | ----------- | ----
ID | ID created by database | String 
startDate | Start Date about availability | String
endDate | End Date about availability | String
doctor[{}] | Doctor information  | String
aboutMe[{}] | Doctor’s about information  | String
contactInfo[{}] | Doctor’s contact information | String
patientInfo[{}] | Patient info  Deprecated  | String
doctorInfo[{}] | Doctor’s info  | String
specialities[{}] | Specialities ID always be fixed | String
licencedState[{}] | Licensed states of doctor’s | String
role[{}] | Role ID always be a fixed ID for doctor’s | String
timezone[{}] | Doctor’s Time zone  | String
createdAt[{}] | End Date about availability | String
forgotPasswordToken[{}] | Forgot password token created | String
familyMembers[{}] | Family member data | String
parentUser[{}] | Parent user Deprecated | String
parentUserRelation[{}] | Parent user Deprecated | String
password[{}] | Deprecated | String
rating[{}] | Deprecated | String
preferredPharmacies[{}] | Deprecated | String
profileImagePath | Doctor’s image path | String
randomtoken | Deprecated | String
doctorsGroups[{}] | Doctor’s Group  | String
preferredDoctors[{}] | Deprecated | String
clinics[{}] | Deprecated | String
doctorsOrg[{}] | Deprecated | String
twilioAccessToken | Deprecated | String
startTimes | Deprecated | String
 | availabilityTimeSlot |
id | ID of availability  | String
startTime | Start time  | String
sTime | Stime is date of availability  | String
eTime | Etime is data of availability  | String
slotNumber | Slot number  | String
patient | Deprecated | String
visitType | Deprecated | String
appointmentId | Deprecated | String
status | “Enable” | String
booked | True & false | String
 | Other All parameter which is not mentioned that all “Deprecated” | 


`Authorization: X-Auth-Token`

<aside class="notice">
You must replace <code>X-Auth-Token</code> with your personal API key.
</aside>

